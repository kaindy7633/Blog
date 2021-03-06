> gulp 现在是越来越流行了。它可以做的事情实在是太多了，比如，拼接 js 文件，压缩图片。

在这个教程里，你会了解怎么使用`gulp.js`来实现一个应用了内置的`livereload`功能的本地 web 服务。

## 以前的实现方式

假设我们要开发一个单页应用。这个 app 的入口是 index.html。我们的目标是可以让浏览器通过 localhost 来访问这个页面。以前，你需要安装一个 Apache 或者 Nginx 这样的服务器软件来实现这样的功能。

## 更棒的实现方式

时至今日，javascript 无所不能了，就要称霸天下了，甚至它都可以去实现一个 web 服务。这篇文章里，我们就要用一个 gulp 的插件，人称`gulp-connect`。用这个插件来实现一个 WEB 服务。

接下来的篇幅，我们就要来为我们的单页应用来配置一个本地服务。

开始下文之前，我假定你已经把准备工作都已经做好了，比如 gulpfile 文件已建好！

第一步，安装
第一步，我们要来安装下`gulp-connect`插件
安装的命令如下：

```bash
npm install --save-dev gulp-connect
```

小提示：`npm install --save-dev` 可以简写为`npm i -D`

现在，我们来定义 web 服务，gulpfile.js 的代码如下

```javascript
var gulp = require("gulp"),
  connect = require("gulp-connect");

gulp.task("webserver", function () {
  connect.server();
});

gulp.task("default", ["webserver"]);
```

只要在终端执行 gulp 命令，然后在浏览器地址栏输入 localhost:8080 就可以看到 index.html 啦。
localhost:8080 所指向的就是 gulpfile 文件所在的那一级目录。
在终端输入 ctrl+c 会结束当前任务。

### 加入`livereload`的支持

创建一个基础的 web 服务很简单，是不是？那现在我们继续来把`livereload`加入 web 服务中。

我们需要做两件事情：
首先，告诉 web 服务启动的时候运行`livereload`。
其次，在页面有更新的时候通知`livereload`刷新页面。

第一步很简单是不是，我们只要将`livereload`的属性设置为`true`，将 webserver 这个任务写成下面的样子。

```javascript
gulp.task("webtask", function () {
  connect.server({
    livereload: true,
  });
});
```

第二步的话就取决于你具体的实例了。比如说，我们要将 less 文件自动编译成 css 样式表，并让其被浏览器识别。

我们来将这个例子分步处理下：

首先，需要一个'watcher'，用来监控 less 文件的变化，监控到变化后这个'watcher'就会去触发 less 的编译器，将其输出为一个 css 文件。之后这个 css 文件有更新了之后就会去通知 livereload，让其刷新页面。

在这个例子里面，还需要用到`gulp-less`插件。
插件的安装命令如下

```bash
npm install --save-dev gulp-less
```

gulp 里已经有了`watch`这个方法，可以来充当'watcher'

我们的文档结构大致可以如下：

.
├── node_modules
│ └── ...
├── styles
│ └── main.less
├── gulpfile.js
├── index.html
└── package.json

watch 任务执行的时候，gulp.js 监听 styles 文件夹里 less 文件的所有改动，当有改动的时候就会触发 less 任务。每一次编译之后，结果会自动返回给浏览器。

`gulpfile.js`文件的代码如下所示（作者允许将下列代码使用于你自己的项目）：

```javascript
var gulp = require("gulp"),
  connect = require("gulp-connect"),
  less = require("gulp-less");

gulp.task("webserver", function () {
  connect.server({
    livereload: true,
  });
});

gulp.task("less", function () {
  gulp
    .src("styles/main.less")
    .pipe(less())
    .pipe(gulp.dest(styles))
    .pipe(connect.reload());
});

gulp.task("watch", function () {
  gulp.watch("style/*.less", ["less"]);
});

gulp.task("default", ["less", "webserver", "watch"]);
```

现在我们重新在终端执行 gulp，然后再在浏览器打开 localhost:8080。
做完这些，我们就可以试着在 style 文件夹的 less 文件里做一些改动。它会立即编译并刷新浏览器。
看吧，这样我们并不需要依赖什么浏览器插件，就可以实现页面的自动刷新啦！

### 一些小小调整

注意，我们之前写的`gulpfile.js`文件只是一个小小的示例用于示范怎么来实现一个运用了`livereload`的 web 服务。

我非常建议大家可以把将其他 gulp 插件一起玩起来。

你也可以试着重新修改下你写的各个 task 的结构，用一用不是 gulp 内置的 watch 方法，这个方法可以只监控有改动的文件。这个对于以后你如果使用更大的代码库来说尤为重要。

我们来看一看对于以上实现 web 服务的另一个方案。

### 更换 Hostname 和 Port

`gulp-connect`插件本身有很多可选的配置。

比如说，你可以更改 web 服务的端口号或者`hostname`。你甚至可以用一个你习惯使用的`hostname`配上 80 端口（默认的是 localhost:8080）

代码如下：

```javascript
connect.server({
  port: 80,
  host: "gulp.dev",
});
```

进行了这个配置之后，我们要在 hosts 文件里面加上 gulp.dev,然后运行`sudo gulp`，因为要使用 80 端口的话，是需要管理员权限的。

### 一些进阶特性

你可以同时启动多个 web server。这个很有用的。比如说，如果你要同时启动一个开发和一个测试的服务。

`gulp-connect`也可以设置多个根目录。

比如，你要用`coffeescript`，然后将压缩过得 js 文件放到一个临时的文件夹，那就可以在根目录 root 中加上这个临时的文件夹而不去影响原来的源文件夹。

在 GitHub 上你可以获得更多的示例，链接如下：
https://github.com/AveVlad/gulp-connect

### 重构我们的代码

在以上的例子中，我们只是写了一个小小的将 less 编译成 css 文件，并让其立即体现在浏览器中的例子。

虽然它奏效了，但是我们可以做的更好。

当把编译和`livereload`混合起来用的时候，可能会有一些问题。

所以，我们将他们拆分开来并用`watch`来监控。

为此，就需要用到上面提到的`gulp-watch`插件。

我们可以再加入一个`coffeeScript`的编译步骤。这个增加的步骤会使我们的新结构更加清晰。

安装新插件的命令

```bash
npm install --save-dev gulp-watch gulp-coffee
```

在`gulpfile.js`文件的最顶部引用这两个插件。在下面的步骤中，我假设你已经在 scripts 文件夹里有了以.coffee 为后缀的文件。

重写的`gulpfile`文件，如下所示：

```javascript
var gulp = require('gulp'),
connect = require('gulp-connect'),
watch = require('gulp-watch'),
coffee = require('gulp-coffee'),
less = require('gulp-less');

gulp.task('webserver',function(){
    connect.server({
        live reload:true,
        root:['.','.tmp']
    });
});

gulp.task('livereload',function(){
    gulp.src(['.tmp/styles/*.css','.tmp/scripts/*.js'])
    .pipe(watch()) //注意此处的watch是gulp-watch插件
    .pipe(connect.reload());
});

gulp.task('coffee',function(){
    gulp.src('scripts/*.coffee')
    .pipe(coffee())
    .pipe(dest('.tmp/scripts'));
});
gulp.task('less',function(){
    gulp.src('styles/main.less')
    .pipe(less())
    .pipe(gulp.dest('.tmp/styles'));
});

gulp.task('watch',function(){
    gulp.watch('style/*.less',['less']);
    gulp.watch('scripts/*.coffee',['coffee']);
})

gulp.task('default',['less','coffee','watch','webserver','livereload']);
```

最大的变化，是增加的`livereload`任务。这个任务仅仅是监听了编译之后的文件，然后如果有变化就刷新浏览器。

`watch()`方法可以仅仅只重新加载有变化的文件。

gulp 自带的`gulp.watch()会`将整个项目都重新加载。

因为添加了`livereload`这个任务，我们就不需要在每一步的编译之后都加上`.pipe(connect.reload())`了。

所以，我们把每个任务按照他们各自关注的点分开定义，这样对于项目开发来说比较好。

同时，我们也发现，编译之后的文件不再保存至他们各自的文件夹去了。现在它们存储在一个临时文件夹.tmp 中。文件夹的内容就是生成的文件，它们存储在临时文件夹，不再去污染 scripts 和 styles 文件夹。我们也建议不要将临时文件夹加入版本控制系统。

我们要做的就是把临时文件夹也视为一个根目录

代码如下

```javascript
root: [".", ".tmp"];
```

这边经过我的测试，经过编译之后会自动生成.tmp 文件夹，这个文件夹里有一个 styles 文件夹存储 css 文件有一个 scripts 文件夹存储 js 文件。

然后我们的版本控制系统是 git，那么在`.gitignore`文件里就要写上.tmp，不要让.tmp 这个临时文件夹加入版本控制系统。

因为在本地预览，这样 html 就得要能获取到 css 和 js 文件，那么就在 root 里把.tmp 也设置为根目录。这样 gulp 执行的时候，就能读取到 css 和 js 文件啦~

提交 git 的话，就提交 html,styles folder,scripts folder.

协同开发者如果 clone 的话，再执行下 gulp 就会再次生成临时文件夹，进行预览。

### 总结

现在，你已经可以用`gulp`来构建一个本地 web 服务了。

你也可以尝试和其他 gulp 插件配合使用，来构建或者测试一个单页应用。

这里的 web 服务仅仅是本地服务，如果你要作为生产，就得要用一些类似 Nginx 或者 CDN 这样的高效解决方案。

Grunt 及类似的项目都可以实现以上的功能，gulp 只是提供了一个比较简便的方法来实现这个功能。
