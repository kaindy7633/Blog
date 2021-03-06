<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->


- [GoLang 极速入门](#golang-%E6%9E%81%E9%80%9F%E5%85%A5%E9%97%A8)
  - [变量定义](#%E5%8F%98%E9%87%8F%E5%AE%9A%E4%B9%89)
    - [第一种 ：一行一个变量，静态语言最基本常用的方式](#%E7%AC%AC%E4%B8%80%E7%A7%8D-%E4%B8%80%E8%A1%8C%E4%B8%80%E4%B8%AA%E5%8F%98%E9%87%8F%E9%9D%99%E6%80%81%E8%AF%AD%E8%A8%80%E6%9C%80%E5%9F%BA%E6%9C%AC%E5%B8%B8%E7%94%A8%E7%9A%84%E6%96%B9%E5%BC%8F)
    - [第二种：多个变量一起声明，声明组](#%E7%AC%AC%E4%BA%8C%E7%A7%8D%E5%A4%9A%E4%B8%AA%E5%8F%98%E9%87%8F%E4%B8%80%E8%B5%B7%E5%A3%B0%E6%98%8E%E5%A3%B0%E6%98%8E%E7%BB%84)
    - [第三种：短声明，只能在函数内](#%E7%AC%AC%E4%B8%89%E7%A7%8D%E7%9F%AD%E5%A3%B0%E6%98%8E%E5%8F%AA%E8%83%BD%E5%9C%A8%E5%87%BD%E6%95%B0%E5%86%85)
    - [第四种：一行声明和初始化多个变量](#%E7%AC%AC%E5%9B%9B%E7%A7%8D%E4%B8%80%E8%A1%8C%E5%A3%B0%E6%98%8E%E5%92%8C%E5%88%9D%E5%A7%8B%E5%8C%96%E5%A4%9A%E4%B8%AA%E5%8F%98%E9%87%8F)
    - [第五种：通过 new 创建指针变量](#%E7%AC%AC%E4%BA%94%E7%A7%8D%E9%80%9A%E8%BF%87-new-%E5%88%9B%E5%BB%BA%E6%8C%87%E9%92%88%E5%8F%98%E9%87%8F)
    - [第六种：make 函数创建 slice、map 或 chan 类型变量](#%E7%AC%AC%E5%85%AD%E7%A7%8Dmake-%E5%87%BD%E6%95%B0%E5%88%9B%E5%BB%BA-slicemap-%E6%88%96-chan-%E7%B1%BB%E5%9E%8B%E5%8F%98%E9%87%8F)
  - [数据类型：整型与浮点型](#%E6%95%B0%E6%8D%AE%E7%B1%BB%E5%9E%8B%E6%95%B4%E5%9E%8B%E4%B8%8E%E6%B5%AE%E7%82%B9%E5%9E%8B)
    - [整型](#%E6%95%B4%E5%9E%8B)
    - [浮点型](#%E6%B5%AE%E7%82%B9%E5%9E%8B)
  - [数据类型：byte、rune 与 string](#%E6%95%B0%E6%8D%AE%E7%B1%BB%E5%9E%8Bbyterune-%E4%B8%8E-string)
    - [byte 与 rune](#byte-%E4%B8%8E-rune)
    - [字符串](#%E5%AD%97%E7%AC%A6%E4%B8%B2)
  - [数据类型：数组与切片](#%E6%95%B0%E6%8D%AE%E7%B1%BB%E5%9E%8B%E6%95%B0%E7%BB%84%E4%B8%8E%E5%88%87%E7%89%87)
    - [数组](#%E6%95%B0%E7%BB%84)
    - [切片](#%E5%88%87%E7%89%87)
  - [数据类型：字典与布尔类型](#%E6%95%B0%E6%8D%AE%E7%B1%BB%E5%9E%8B%E5%AD%97%E5%85%B8%E4%B8%8E%E5%B8%83%E5%B0%94%E7%B1%BB%E5%9E%8B)
    - [字典](#%E5%AD%97%E5%85%B8)
    - [声明初始化字典](#%E5%A3%B0%E6%98%8E%E5%88%9D%E5%A7%8B%E5%8C%96%E5%AD%97%E5%85%B8)
    - [字典的相关操作](#%E5%AD%97%E5%85%B8%E7%9A%84%E7%9B%B8%E5%85%B3%E6%93%8D%E4%BD%9C)
      - [添加元素](#%E6%B7%BB%E5%8A%A0%E5%85%83%E7%B4%A0)
      - [更新元素](#%E6%9B%B4%E6%96%B0%E5%85%83%E7%B4%A0)
      - [读取元素](#%E8%AF%BB%E5%8F%96%E5%85%83%E7%B4%A0)
      - [删除元素](#%E5%88%A0%E9%99%A4%E5%85%83%E7%B4%A0)
      - [判断 `key` 是否存在](#%E5%88%A4%E6%96%AD-key-%E6%98%AF%E5%90%A6%E5%AD%98%E5%9C%A8)
      - [循环字典](#%E5%BE%AA%E7%8E%AF%E5%AD%97%E5%85%B8)
    - [布尔类型](#%E5%B8%83%E5%B0%94%E7%B1%BB%E5%9E%8B)
  - [数据类型：指针](#%E6%95%B0%E6%8D%AE%E7%B1%BB%E5%9E%8B%E6%8C%87%E9%92%88)
    - [什么是指针](#%E4%BB%80%E4%B9%88%E6%98%AF%E6%8C%87%E9%92%88)
    - [指针的创建](#%E6%8C%87%E9%92%88%E7%9A%84%E5%88%9B%E5%BB%BA)
    - [指针的类型](#%E6%8C%87%E9%92%88%E7%9A%84%E7%B1%BB%E5%9E%8B)
    - [指针的零值](#%E6%8C%87%E9%92%88%E7%9A%84%E9%9B%B6%E5%80%BC)
    - [指针与切片](#%E6%8C%87%E9%92%88%E4%B8%8E%E5%88%87%E7%89%87)
  - [面向对象编程：结构体与继承](#%E9%9D%A2%E5%90%91%E5%AF%B9%E8%B1%A1%E7%BC%96%E7%A8%8B%E7%BB%93%E6%9E%84%E4%BD%93%E4%B8%8E%E7%BB%A7%E6%89%BF)
    - [什么是结构体？](#%E4%BB%80%E4%B9%88%E6%98%AF%E7%BB%93%E6%9E%84%E4%BD%93)
    - [定义结构体](#%E5%AE%9A%E4%B9%89%E7%BB%93%E6%9E%84%E4%BD%93)
    - [定义方法](#%E5%AE%9A%E4%B9%89%E6%96%B9%E6%B3%95)
    - [方法的参数传递方式](#%E6%96%B9%E6%B3%95%E7%9A%84%E5%8F%82%E6%95%B0%E4%BC%A0%E9%80%92%E6%96%B9%E5%BC%8F)
    - [结构体实现 “继承”](#%E7%BB%93%E6%9E%84%E4%BD%93%E5%AE%9E%E7%8E%B0-%E7%BB%A7%E6%89%BF)
    - [内部方法与外部方法](#%E5%86%85%E9%83%A8%E6%96%B9%E6%B3%95%E4%B8%8E%E5%A4%96%E9%83%A8%E6%96%B9%E6%B3%95)
  - [理解 Go 里的函数](#%E7%90%86%E8%A7%A3-go-%E9%87%8C%E7%9A%84%E5%87%BD%E6%95%B0)
    - [关于函数](#%E5%85%B3%E4%BA%8E%E5%87%BD%E6%95%B0)
    - [函数的声明](#%E5%87%BD%E6%95%B0%E7%9A%84%E5%A3%B0%E6%98%8E)
    - [函数实现可变参数](#%E5%87%BD%E6%95%B0%E5%AE%9E%E7%8E%B0%E5%8F%AF%E5%8F%98%E5%8F%82%E6%95%B0)
    - [多个可变参数函数传递参数](#%E5%A4%9A%E4%B8%AA%E5%8F%AF%E5%8F%98%E5%8F%82%E6%95%B0%E5%87%BD%E6%95%B0%E4%BC%A0%E9%80%92%E5%8F%82%E6%95%B0)
    - [函数的返回值](#%E5%87%BD%E6%95%B0%E7%9A%84%E8%BF%94%E5%9B%9E%E5%80%BC)
    - [方法与函数](#%E6%96%B9%E6%B3%95%E4%B8%8E%E5%87%BD%E6%95%B0)
    - [匿名函数的使用](#%E5%8C%BF%E5%90%8D%E5%87%BD%E6%95%B0%E7%9A%84%E4%BD%BF%E7%94%A8)
  - [语言流程控制：if-else​](#%E8%AF%AD%E8%A8%80%E6%B5%81%E7%A8%8B%E6%8E%A7%E5%88%B6if-else%E2%80%8B)
    - [条件语句模型](#%E6%9D%A1%E4%BB%B6%E8%AF%AD%E5%8F%A5%E6%A8%A1%E5%9E%8B)
    - [单分支判断](#%E5%8D%95%E5%88%86%E6%94%AF%E5%88%A4%E6%96%AD)
    - [多分支判断](#%E5%A4%9A%E5%88%86%E6%94%AF%E5%88%A4%E6%96%AD)
    - [高级写法](#%E9%AB%98%E7%BA%A7%E5%86%99%E6%B3%95)
  - [语言流程控制：switch-case](#%E8%AF%AD%E8%A8%80%E6%B5%81%E7%A8%8B%E6%8E%A7%E5%88%B6switch-case)
    - [语句模型](#%E8%AF%AD%E5%8F%A5%E6%A8%A1%E5%9E%8B)
    - [最简单的示例](#%E6%9C%80%E7%AE%80%E5%8D%95%E7%9A%84%E7%A4%BA%E4%BE%8B)
    - [一个 case 多个条件](#%E4%B8%80%E4%B8%AA-case-%E5%A4%9A%E4%B8%AA%E6%9D%A1%E4%BB%B6)
    - [case 条件常量不能重复](#case-%E6%9D%A1%E4%BB%B6%E5%B8%B8%E9%87%8F%E4%B8%8D%E8%83%BD%E9%87%8D%E5%A4%8D)
    - [switch 后可接函数](#switch-%E5%90%8E%E5%8F%AF%E6%8E%A5%E5%87%BD%E6%95%B0)
    - [switch 可不接表达式](#switch-%E5%8F%AF%E4%B8%8D%E6%8E%A5%E8%A1%A8%E8%BE%BE%E5%BC%8F)
    - [switch 的穿透能力](#switch-%E7%9A%84%E7%A9%BF%E9%80%8F%E8%83%BD%E5%8A%9B)
  - [语言流程控制：for 循环](#%E8%AF%AD%E8%A8%80%E6%B5%81%E7%A8%8B%E6%8E%A7%E5%88%B6for-%E5%BE%AA%E7%8E%AF)
    - [语句模型](#%E8%AF%AD%E5%8F%A5%E6%A8%A1%E5%9E%8B-1)
  - [语言流程控制：goto](#%E8%AF%AD%E8%A8%80%E6%B5%81%E7%A8%8B%E6%8E%A7%E5%88%B6goto)
    - [基本模型](#%E5%9F%BA%E6%9C%AC%E6%A8%A1%E5%9E%8B)
    - [最简单的示例](#%E6%9C%80%E7%AE%80%E5%8D%95%E7%9A%84%E7%A4%BA%E4%BE%8B-1)
    - [如何使用？](#%E5%A6%82%E4%BD%95%E4%BD%BF%E7%94%A8)
    - [注意事项](#%E6%B3%A8%E6%84%8F%E4%BA%8B%E9%A1%B9)
  - [语言流程控制：defer 延迟调用](#%E8%AF%AD%E8%A8%80%E6%B5%81%E7%A8%8B%E6%8E%A7%E5%88%B6defer-%E5%BB%B6%E8%BF%9F%E8%B0%83%E7%94%A8)
    - [延迟调用](#%E5%BB%B6%E8%BF%9F%E8%B0%83%E7%94%A8)
    - [即时求值的变量快照](#%E5%8D%B3%E6%97%B6%E6%B1%82%E5%80%BC%E7%9A%84%E5%8F%98%E9%87%8F%E5%BF%AB%E7%85%A7)
    - [多个 defer 反序调用](#%E5%A4%9A%E4%B8%AA-defer-%E5%8F%8D%E5%BA%8F%E8%B0%83%E7%94%A8)
    - [defer 与 return 孰先孰后](#defer-%E4%B8%8E-return-%E5%AD%B0%E5%85%88%E5%AD%B0%E5%90%8E)
    - [为什么要有 defer？](#%E4%B8%BA%E4%BB%80%E4%B9%88%E8%A6%81%E6%9C%89-defer)
  - [面向对象编程：接口与多态](#%E9%9D%A2%E5%90%91%E5%AF%B9%E8%B1%A1%E7%BC%96%E7%A8%8B%E6%8E%A5%E5%8F%A3%E4%B8%8E%E5%A4%9A%E6%80%81)
    - [接口是什么？](#%E6%8E%A5%E5%8F%A3%E6%98%AF%E4%BB%80%E4%B9%88)
      - [如何定义接口](#%E5%A6%82%E4%BD%95%E5%AE%9A%E4%B9%89%E6%8E%A5%E5%8F%A3)
      - [如何实现接口](#%E5%A6%82%E4%BD%95%E5%AE%9E%E7%8E%B0%E6%8E%A5%E5%8F%A3)
      - [接口实现多态](#%E6%8E%A5%E5%8F%A3%E5%AE%9E%E7%8E%B0%E5%A4%9A%E6%80%81)
  - [关键字：make 和 new 的区别](#%E5%85%B3%E9%94%AE%E5%AD%97make-%E5%92%8C-new-%E7%9A%84%E5%8C%BA%E5%88%AB)
    - [`new` 函数](#new-%E5%87%BD%E6%95%B0)
    - [make 函数](#make-%E5%87%BD%E6%95%B0)
    - [总结](#%E6%80%BB%E7%BB%93)
  - [Go 的语句块与作用域](#go-%E7%9A%84%E8%AF%AD%E5%8F%A5%E5%9D%97%E4%B8%8E%E4%BD%9C%E7%94%A8%E5%9F%9F)
    - [显示语句块与隐式语句块](#%E6%98%BE%E7%A4%BA%E8%AF%AD%E5%8F%A5%E5%9D%97%E4%B8%8E%E9%9A%90%E5%BC%8F%E8%AF%AD%E5%8F%A5%E5%9D%97)
    - [四种作用域的理解](#%E5%9B%9B%E7%A7%8D%E4%BD%9C%E7%94%A8%E5%9F%9F%E7%9A%84%E7%90%86%E8%A7%A3)
    - [静态作用域与动态作用域](#%E9%9D%99%E6%80%81%E4%BD%9C%E7%94%A8%E5%9F%9F%E4%B8%8E%E5%8A%A8%E6%80%81%E4%BD%9C%E7%94%A8%E5%9F%9F)
  - [学习 Go 协程：goroutine](#%E5%AD%A6%E4%B9%A0-go-%E5%8D%8F%E7%A8%8Bgoroutine)
    - [协程的初步使用](#%E5%8D%8F%E7%A8%8B%E7%9A%84%E5%88%9D%E6%AD%A5%E4%BD%BF%E7%94%A8)
    - [多个协程的效果](#%E5%A4%9A%E4%B8%AA%E5%8D%8F%E7%A8%8B%E7%9A%84%E6%95%88%E6%9E%9C)
  - [Go 协程：详解信道/通道](#go-%E5%8D%8F%E7%A8%8B%E8%AF%A6%E8%A7%A3%E4%BF%A1%E9%81%93%E9%80%9A%E9%81%93)
    - [前言](#%E5%89%8D%E8%A8%80)
    - [信道的定义与使用](#%E4%BF%A1%E9%81%93%E7%9A%84%E5%AE%9A%E4%B9%89%E4%B8%8E%E4%BD%BF%E7%94%A8)
    - [信道的容量与长度](#%E4%BF%A1%E9%81%93%E7%9A%84%E5%AE%B9%E9%87%8F%E4%B8%8E%E9%95%BF%E5%BA%A6)
    - [缓冲信道与无缓冲信道](#%E7%BC%93%E5%86%B2%E4%BF%A1%E9%81%93%E4%B8%8E%E6%97%A0%E7%BC%93%E5%86%B2%E4%BF%A1%E9%81%93)
    - [双向信道与单向信道](#%E5%8F%8C%E5%90%91%E4%BF%A1%E9%81%93%E4%B8%8E%E5%8D%95%E5%90%91%E4%BF%A1%E9%81%93)
    - [遍历信道](#%E9%81%8D%E5%8E%86%E4%BF%A1%E9%81%93)
    - [用信道来做锁](#%E7%94%A8%E4%BF%A1%E9%81%93%E6%9D%A5%E5%81%9A%E9%94%81)
  - [几个信道死锁经典错误案例详解](#%E5%87%A0%E4%B8%AA%E4%BF%A1%E9%81%93%E6%AD%BB%E9%94%81%E7%BB%8F%E5%85%B8%E9%94%99%E8%AF%AF%E6%A1%88%E4%BE%8B%E8%AF%A6%E8%A7%A3)
    - [错误示例一](#%E9%94%99%E8%AF%AF%E7%A4%BA%E4%BE%8B%E4%B8%80)
    - [错误示例二](#%E9%94%99%E8%AF%AF%E7%A4%BA%E4%BE%8B%E4%BA%8C)
    - [错误示例三](#%E9%94%99%E8%AF%AF%E7%A4%BA%E4%BE%8B%E4%B8%89)
  - [Go 协程：WaitGroup](#go-%E5%8D%8F%E7%A8%8Bwaitgroup)
    - [使用信道来标记完成](#%E4%BD%BF%E7%94%A8%E4%BF%A1%E9%81%93%E6%9D%A5%E6%A0%87%E8%AE%B0%E5%AE%8C%E6%88%90)
    - [使用 WaitGroup](#%E4%BD%BF%E7%94%A8-waitgroup)
  - [Go协程：互斥锁和读写锁](#go%E5%8D%8F%E7%A8%8B%E4%BA%92%E6%96%A5%E9%94%81%E5%92%8C%E8%AF%BB%E5%86%99%E9%94%81)
    - [互斥锁 ：Mutex](#%E4%BA%92%E6%96%A5%E9%94%81-mutex)
    - [读写锁：RWMutex](#%E8%AF%BB%E5%86%99%E9%94%81rwmutex)
  - [Go里的异常处理：panic 和 recover](#go%E9%87%8C%E7%9A%84%E5%BC%82%E5%B8%B8%E5%A4%84%E7%90%86panic-%E5%92%8C-recover)
    - [触发panic](#%E8%A7%A6%E5%8F%91panic)
    - [捕获 panic](#%E6%8D%95%E8%8E%B7-panic)
    - [无法跨协程](#%E6%97%A0%E6%B3%95%E8%B7%A8%E5%8D%8F%E7%A8%8B)
    - [总结](#%E6%80%BB%E7%BB%93-1)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

# GoLang 极速入门

## 变量定义

如果你是`Python`、`PHP` 或 `Ruby` 等动态语言开发者，也许会不太理解声明这个过程，在动态语言中，基本是直接拿来就用，也不用声明类型啥的。但 `Go` 语言是和 `C` 一样的静态类型语言，编译时会检查变量的类型，所以变量必须有具体的类型。

变量在使用前，需要先声明。声明会有类型或推导出类型，这就约定了该变量只能赋该类型的值。（接口是另外一种形式）

声明或定义一般有以下六种方法，其中前面两种也可用于常量，只要替换关键字 `var -> const` 即可。

### 第一种 ：一行一个变量，静态语言最基本常用的方式

```go
var <name> <type>
```

其中 `var` 是关键字（固定不变），`name` 是变量名，`type` 是类型。`Node/JS` 开发者，对于 `type` 外，其他应该挺熟悉的。

使用 `var` ，虽然只指定了类型，但是 `Go` 会所有类型都有默认值，比如 `string` 类型会初始化为空字符串，`int` 类型会初始化为 `0`，`float` 会初始化为 `0.0`，`bool` 会初始化为 `false`，引用和指针类型就初始化为 `nil` 等。

若要在声明时，顺便也初始化，可以这样写

```go
var name sting = "Go编程时光发布在Go语言中文网"
```

以上例子的完整代码如下（为了不写重复性的代码，后续不再贴完整代码，只贴关键代码）

```go
package main

import "fmt"

func main()  {
    var name string = "Go编程时光发布在Go语言中文网"
    fmt.Println(name)
}
```

从右值（等号右边的值，`rvalue`）来看，明显是个 `string` 类型。因此也可以将其简化为

```go
var name = "Go编程时光发布在Go语言中文网"
```

这叫做**类型推导**。

若你的右值带有小数点，在不指定类型的情况下，编译器会将你的这个变量声明为 `float64`。如果你不需要这么高的精度可以指定类型：

```go
var rate float32 0.89
```

### 第二种：多个变量一起声明，声明组

声明多个变量，除了可以按照上面写成多行之外，还可以写成下面这样

```go
var (
    name string
    age int
    gender string
)
```

### 第三种：短声明，只能在函数内

使用 `:=` （推导声明写法或短类型声明法：编译器会自动根据右值类型推断出左值的对应类型。），可以声明一个变量，并对其进行（显式）初始化。

```go
name := "Go编程时光发布在Go语言中文网"

// 等价于
var name string = "Go编程时光发布在Go语言中文网"

// 等价于
var name = "Go编程时光发布在Go语言中文网"
```

但这种方法有个限制就是，只能用于函数内部

### 第四种：一行声明和初始化多个变量

```go
name, age := "Go编程时光发布在Go语言中文网", 28
```

这种方法，也经常用于变量的交换。之前常见的面试题，如何不用中间变量交换两个整数变量，在 `Go` 中直接搞定。

```go
var a int = 100
var b int = 200
b, a = a, b
```

### 第五种：通过 new 创建指针变量

先简单介绍下指针的相关内容。

一般变量分为两种 普通变量 和 指针变量

普通变量，存放的是数据本身，而指针变量存放的是数据的地址。

如下代码，`age` 是一个普通变量，存放的内容是 `28`，而 `ptr` 是 存放变量 `age` 值的内存地址：`0xc000010098`

```go
package main

import "fmt"

func main()  {
    var age int = 28
    var ptr = &age  // &后面接变量名，表示取出该变量的内存地址
    fmt.Println("age: ", age)
    fmt.Println("ptr: ", ptr)
}

// age:  28
// ptr:  0xc000010098
```

而这里要说的 `new` 函数，是 `Go` 里的一个内建函数。

使用表达式 `new(Type)` 将创建一个 `Type` 类型的匿名变量，初始化为 `Type` 类型的零值，然后返回变量地址，返回的指针类型为 `*Type`。

```go
package main

import "fmt"

func main()  {
    ptr := new(int)
    fmt.Println("ptr address: ", ptr)
    fmt.Println("ptr value: ", *ptr)  // * 后面接指针变量，表示从内存地址中取出值
}

// ptr address:  0xc000010098
// ptr value:  0
```

用 `new` 创建变量和普通变量声明语句方式创建变量没有什么区别，除了不需要声明一个临时变量的名字外，我们还可以在表达式中使用 `new(Type)` 。换言之，`new` 函数类似是一种语法糖，而不是一个新的基础概念。

如下两种写法，可以说是等价的

```go
// 使用 new
func newInt() *int {
    return new(int)
}

// 使用传统的方式
func newInt() *int {
    var dummy int
    return &dummy
}
```

### 第六种：make 函数创建 slice、map 或 chan 类型变量

```go
var slice = make([]int, 8)
var m = make(map[string]int)
var c = make(chan int)
```

`slice`、`map` 和 `chan` 是 `Go` 中的引用类型，它们的创建和初始化，一般使用 `make`。特别的，`chan` 只能用 `make`。`slice` 和 `map` 还可以简单的方式：

```go
slice := []int{0, 0}
m := map[string]int{}
```

以上不管哪种方法，变量/常量都只能声明一次，声明多次，编译就会报错。

但也有例外，这就要说到一个特殊变量：匿名变量，也称作占位符，或者空白标识符，用下划线表示。

匿名变量，优点有三：

- 不分配内存，不占用内存空间

- 不需要你为命名无用的变量名而纠结

- 多次声明不会有任何问题

通常我们用匿名接收 必须接收，但是又不会用到的值，可以理解为垃圾桶。

```go
func GetData() (int, int) {
    return 100, 200
}
func main(){
    a, _ := GetData()
    _, b := GetData()
    fmt.Println(a, b)
}
```

## 数据类型：整型与浮点型

### 整型

`Go` 语言中，整数类型可以再细分成 `10` 个类型，为了方便大家学习，我将这些类型整理成一张表格。

![](../images/golang_640.png)

`int` 和 `uint` 的区别就在于一个 `u`，有 `u` 说明是无符号，没有 `u` 代表有符号。

解释这个符号的区别

以 `int8` 和 `uint8` 举例，`8` 代表 `8` 个`bit`，能表示的数值个数有 `2^8 = 256`。

`uint8` 是无符号，能表示的都是正数，`0-255`，刚好 `256` 个数。

`int8` 是有符号，既可以正数，也可以负数，那怎么办？对半分呗，`-128-127`，也刚好 `256` 个数。

`int8` `int16` `int32` `int64` 这几个类型的最后都有一个数值，这表明了它们能表示的数值个数是固定的。

而 `int` 没有并没有指定它的位数，说明它的大小，是可以变化的，那根据什么变化呢？

当你在 32 位的系统下，`int` 和 `uint` 都占用 4 个字节，也就是 32 位。

若你在 64 位的系统下，`int` 和 `uint` 都占用 8 个字节，也就是 64 位。

出于这个原因，在某些场景下，你应当避免使用 `int` 和 `uint` ，而使用更加精确的 `int32` 和 `int64`，比如在二进制传输、读写文件的结构描述（为了保持文件的结构不会受到不同编译目标平台字节长度的影响）

不同进制的表示方法

出于习惯，在初始化数据类型为整形的变量时，我们会使用 10 进制的表示法，因为它最直观，比如这样，表示整数 10.

```go
var num int = 10
```

不过，你要清楚，你一样可以使用其他进制来表示一个整数，这里以比较常用的 2 进制、8 进制和 16 进制举例。

2 进制：以 `0b` 或 `0B` 为前缀

```go
var num01 int = 0b1100
```

8 进制：以 `0o` 或者 `0O` 为前缀

```go
var num02 int = 0o14
```

16 进制：以 `0x` 为前缀

```go
var num03 int = 0xC
```

下面用一段代码分别使用二进制、8 进制、16 进制来表示 10 进制的数值：12

```go
package main

import (
    "fmt"
)

func main() {
    var num01 int = 0b1100
    var num02 int = 0o14
    var num03 int = 0xC

    fmt.Printf("2进制数 %b 表示的是: %d \n", num01, num01)
    fmt.Printf("8进制数 %o 表示的是: %d \n", num02, num02)
    fmt.Printf("16进制数 %X 表示的是: %d \n", num03, num03)
}

// 2进制数 1100 表示的是: 12
// 8进制数 14 表示的是: 12
// 16进制数 C 表示的是: 12
```

以上代码用过了 `fmt` 包的格式化功能，你可以参考这里去看上面的代码

- `%b` 表示为二进制
- `%c` 该值对应的 `unicode` 码值
- `%d` 表示为十进制
- `%o` 表示为八进制
- `%q` 该值对应的单引号括起来的 `go` 语法字符字面值，必要时会采用安全的转义表示
- `%x` 表示为十六进制，使用 `a`- `f`
- `%X` 表示为十六进制，使用 `A` - `F`
- `%U` 表示为 `Unicode` 格式：U+1234，等价于"U+%04X"

### 浮点型

浮点数类型的值一般由整数部分、小数点“.”和小数部分组成。

其中，整数部分和小数部分均由 10 进制表示法表示。不过还有另一种表示方法。那就是在其中加入指数部分。指数部分由“E”或“e”以及一个带正负号的 10 进制数组成。比如，3.7E-2 表示浮点数 0.037。又比如，3.7E+1 表示浮点数 37。

有时候，浮点数类型值的表示也可以被简化。比如，37.0 可以被简化为 37。又比如，0.037 可以被简化为.037。

有一点需要注意，在 `Go` 语言里，浮点数的相关部分只能由 10 进制表示法表示，而不能由 8 进制表示法或 16 进制表示法表示。比如，03.7 表示的一定是浮点数 3.7。

`Go`语言中提供了两种精度的浮点数 `float32` 和 `float64`。

`float32`，也即我们常说的单精度，存储占用 4 个字节，也即 4\*8=32 位，其中 1 位用来符号，8 位用来指数，剩下的 23 位表示尾数

![](../images/golang极速入门_2.webp)

`float64`，也即我们熟悉的双精度，存储占用 8 个字节，也即 8\*8=64 位，其中 1 位用来符号，11 位用来指数，剩下的 52 位表示尾数

![](../images/golang极速入门_3.webp)

那么精度是什么意思？有效位有多少位？

精度主要取决于尾数部分的位数。

对于 `float32`（单精度）来说，表示尾数的为 23 位，除去全部为 0 的情况以外，最小为 2^-23，约等于 1.19\*10^-7，所以 float 小数部分只能精确到后面 6 位，加上小数点前的一位，即有效数字为 7 位。

同理 `float64`（单精度）的尾数部分为 52 位，最小为 2^-52，约为 2.22\*10^-16，所以精确到小数点后 15 位，加上小数点前的一位，有效位数为 16 位。

通过以上，可以总结出以下几点：

1. `float32` 和 `float64` 可以表示的数值很多

浮点数类型的取值范围可以从很微小到很巨大。浮点数取值范围的极限值可以在 `math` 包中找到：

常量 `math.MaxFloat32` 表示 `float32` 能取到的最大数值，大约是 3.4e38；

常量 `math.MaxFloat64` 表示 `float64` 能取到的最大数值，大约是 1.8e308；

`float32` 和 `float64` 能表示的最小值分别为 1.4e-45 和 4.9e-324。

2. 数值很大但精度有限

人家虽然能表示的数值很大，但精度位却没有那么大。

`float32` 的精度只能提供大约 6 个十进制数（表示后科学计数法后，小数点后 6 位）的精度

`float64` 的精度能提供大约 15 个十进制数（表示后科学计数法后，小数点后 15 位）的精度

这里的精度是什么意思呢？

比如 10000018 这个数，用 `float32` 的类型来表示的话，由于其有效位是 7 位，将 10000018 表示成科学计数法，就是 1.0000018 \* 10^7，能精确到小数点后面 6 位。

此时用科学计数法表示后，小数点后有 7 位，刚刚满足我们的精度要求，意思是什么呢？此时你对这个数进行+1 或者-1 等数学运算，都能保证计算结果是精确的

```go
package main

import "fmt"

var myfloat float32 = 10000018

func main()  {
    fmt.Println("myfloat: ", myfloat)
    fmt.Println("myfloat: ", myfloat+1)
}

// myfloat:  1.0000018e+07
// myfloat:  1.0000019e+07
```

上面举了一个刚好满足精度要求数据的临界情况，为了做对比，下面也举一个刚好不满足精度要求的例子。只要给这个数值多加一位数就行了。

换成 100000187，同样使用 `float32`类型，表示成科学计数法，由于精度有限，表示的时候小数点后面 7 位是准确的，但若是对其进行数学运算，由于第八位无法表示，所以运算后第七位的值，就会变得不精确。

这里我们写个代码来验证一下，按照我们的理解下面 `myfloat01 = 100000182` ，对其+5 操作后，应该等于 `myfloat02 = 100000187`，

```go
import "fmt"

var myfloat01 float32 = 100000182
var myfloat02 float32 = 100000187

func main() {
    fmt.Println("myfloat: ", myfloat01)
    fmt.Println("myfloat: ", myfloat01+5)
    fmt.Println(myfloat02 == myfloat01+5)
}
```

但是由于其类型是 `float32`，精度不足，导致最后比较的结果是不相等（从小数点后第七位开始不精确）

```go
// myfloat:  1.00000184e+08
// myfloat:  1.0000019e+08
// false
```

由于精度的问题，就会出现这种很怪异的现象，`myfloat == myfloat +1` 会返回 `true` 。

## 数据类型：byte、rune 与 string

### byte 与 rune

`byte`，占用 1 个节字，就 8 个比特位，所以它和 `uint8` 类型本质上没有区别，它表示的是 `ACSII` 表中的一个字符。

如下这段代码，分别定义了 `byte` 类型和 `uint8` 类型的变量 `a` 和 `b`

```go
import "fmt"

func main() {
    var a byte = 65
    // 8进制写法: var c byte = '\101'     其中 \ 是固定前缀
    // 16进制写法: var c byte = '\x41'    其中 \x 是固定前缀

    var b uint8 = 66
    fmt.Printf("a 的值: %c \nb 的值: %c", a, b)
    // 或者使用 string 函数
    // fmt.Println("a 的值: ", string(a)," \nb 的值: ", string(b))
}
```

在 `ASCII` 表中，由于字母 `A` 的 `ASCII` 的编号为 65 ，字母 `B` 的 `ASCII` 编号为 66，所以上面的代码也可以写成这样

```go
import "fmt"

func main() {
    var a byte = 'A'
    var b uint8 = 'B'
    fmt.Printf("a 的值: %c \nb 的值: %c", a, b)
}
```

他们的输出结果都是一样的。

`rune`，占用 4 个字节，共 32 位比特位，所以它和 `uint32` 本质上也没有区别。它表示的是一个 `Unicode` 字符（`Unicode` 是一个可以表示世界范围内的绝大部分字符的编码规范）。

```go
import (
    "fmt"
    "unsafe"
)

func main() {
    var a byte = 'A'
    var b rune = 'B'
    fmt.Printf("a 占用 %d 个字节数\nb 占用 %d 个字节数", unsafe.Sizeof(a), unsafe.Sizeof(b))
}

// a 占用 1 个字节数
// b 占用 4 个字节数
```

由于 `byte` 类型能表示的值是有限，只有 2^8=256 个。所以如果你想表示中文的话，你只能使用 `rune` 类型。

```go
var name rune = '中'
```

或许你已经发现，上面我们在定义字符时，不管是 `byte` 还是 `rune` ，我都是使用单引号，而没使用双引号。

对于从 `Python` 转过来的人，这里一定要注意了，在 `Go` 中单引号与双引号并不是等价的。

单引号用来表示字符，在上面的例子里，如果你使用双引号，就意味着你要定义一个字符串，赋值时与前面声明的前面会不一致，这样在编译的时候就会出错。

```bash
cannot use "A" (type string) as type byte in assignment
```

上面我说了，`byte` 和 `uint8` 没有区别，`rune` 和 `uint32` 没有区别，那为什么还要多出 `byte` 和 `rune` 类型呢？多乱呀。

理由很简单，因为 `uint8` 和 `uint32` ，直观上让人以为这是一个数值，但是实际上，它也可以表示一个字符，所以为了消除这种直观错觉，就诞生了 `byte` 和 `rune` 这两个别名类型。

### 字符串

字符串，可以说是大家很熟悉的数据类型之一。定义方法很简单

```go
var mystr string = "hello"
```

上面说的 `byte` 和 `rune` 都是字符类型，若多个字符放在一起，就组成了字符串，也就是这里要说的 `string` 类型。

比如 `hello` ，对照 `ASCII` 编码表，每个字母对应的编号是：104,101,108,108,111

```go
import (
    "fmt"
)

func main() {
    var mystr01 sting = "hello"
    var mystr02 [5]byte = [5]byte{104, 101, 108, 108, 111}
    fmt.Printf("mystr01: %s\n", mystr01)
    fmt.Printf("mystr02: %s", mystr02)
}
```

输出如下，`mystr01` 和 `mystr02` 输出一样，说明了 `string` 的本质，其实是一个 `byte` 数组

```go
// mystr01: hello
// mystr02: hello
```

通过以上学习，我们知道字符分为 `byte` 和 `rune`，占用的大小不同。

这里来考一下大家，hello,中国 占用几个字节？

要回答这个问题，你得知道 `Go` 语言的 `string` 是用 `uft-8` 进行编码的，英文字母占用一个字节，而中文字母占用 3 个字节，所以 hello,中国 的长度为 5+1+（3＊2)= 12 个字节。

```go
import (
    "fmt"
)

func main() {
    var country string = "hello,中国"
    fmt.Println(len(country))
}
// 输出 12
```

## 数据类型：数组与切片

### 数组

数组是一个由固定长度的特定类型元素组成的序列，一个数组可以由零个或多个元素组成。因为数组的长度是固定的，所以在 `Go` 语言中很少直接使用数组。

声明数组，并给该数组里的每个元素赋值（索引值的最小有效值和其他大多数语言一样是 0，不是 1）

```go
// [3] 里的3 表示该数组的元素个数
var arr [3]int
arr[0] = 1
arr[1] = 2
arr[2] = 3
```

声明并直接初始化数组

```go
// 第一种方法
var arr [3]int = [3]int{1,2,3}

// 第二种方法
arr := [3]int{1,2,3}
```

上面的 3 表示数组的元素个数 ，万一你哪天想往该数组中增加元素，你得对应修改这个数字，为了避免这种硬编码，你可以这样写，使用 `...` 让 `Go` 语言自己根据实际情况来分配空间。

```go
arr := [...]int{1,2,3}
```

`[3]int` 和 `[4]int` 虽然都是数组，但他们却是不同的类型，使用 `fmt` 的 `%T` 可以查得，如果使用 `==` 来比较，答案会是 `false`

```go
import (
    "fmt"
)

func main() {
    arr01 := [...]int{1, 2, 3}
    arr02 := [...]int{1, 2, 3, 4}
    fmt.Printf("%d 的类型是: %T\n", arr01, arr01)
    fmt.Printf("%d 的类型是: %T", arr02, arr02)
}

// [1 2 3] 的类型是: [3]int
// [1 2 3 4] 的类型是: [4]int
```

如果你觉得每次写 `[3]int` 有点麻烦，你可以为 `[3]int` 定义一个类型字面量，也就是别名类型。

使用 `type` 关键字可以定义一个类型字面量，后面只要你想定义一个容器大小为 3，元素类型为 `int` 的数组 ，都可以使用这个别名类型。

```go
import (
    "fmt"
)

func main() {
    type arr3 [3]int

    myarr := arr3{1,2,3}
    fmt.Printf("%d 的类型是: %T", myarr, myarr)
}

// [1 2 3] 的类型是: main.arr3
```

### 切片

切片（`Slice`）与数组一样，也是可以容纳若干类型相同的元素的容器。与数组不同的是，无法通过切片类型来确定其值的长度。每个切片值都会将数组作为其底层数据结构。我们也把这样的数组称为切片的底层数组。

切片是对数组的一个连续片段的引用，所以切片是一个引用类型，这个片段可以是整个数组，也可以是由起始和终止索引标识的一些项的子集，需要注意的是，终止索引标识的项不包括在切片内（意思是这是个左闭右开的区间）

```go
import (
    "fmt"
)

func main() {
    myarr := [...]int{1, 2, 3}
    fmt.Printf("%d 的类型是: %T", myarr[0:2], myarr[0:2])
}

// [1 2] 的类型是: []int
```

切片的构造，有三种方式

1、对数组进行片段截取（上面例子已经展示：`myarr[0:2]`，0 是索引起始值，2 是索引终止值，区间左闭右开）

从头声明赋值（例子如下）

```go
// 声明字符串切片
var strList []string

// 声明整型切片
var numList []int

// 声明一个空切片
var numListEmpty = []int{}
```

2、使用 `make` 函数构造，`make` 函数的格式：`make( []Type, size, cap )`

这个函数刚好指出了，一个切片具备的三个属性：类型（`Type`），长度（`size`），容量（`cap`）

```go
import (
   "fmt"
)

func main() {
   a := make([]int, 2)
   b := make([]int, 2, 10)
   fmt.Println(a, b)
   fmt.Println(len(a), len(b))
   fmt.Println(cap(a), cap(b))
}

// [0 0] [0 0]
// 2 2
// 2 10
```

由于切片是引用类型，所以你不对它进行赋值的话，它的零值（默认值）是 `nil`

```go
var myarr []int
fmt.Println(myarr == nil)
// true
```

数组与切片有相同点，它们都是可以容纳若干类型相同的元素的容器

也有不同点，数组的容器大小固定，而切片本身是引用类型，它更像是 `Python` 中的 `list` ，我们可以对它 `append` 进行元素的添加。

```go
import (
    "fmt"
)

func main() {
    myarr := []int{1}
    // 追加一个元素
    myarr = append(myarr, 2)
    // 追加多个元素
    myarr = append(myarr, 3, 4)
    // 追加一个切片, ... 表示解包，不能省略
    myarr = append(myarr, []int{7, 8}...)
    // 在第一个位置插入元素
    myarr = append([]int{0}, myarr...)
    // 在中间插入一个切片(两个元素)
    myarr = append(myarr[:5], append([]int{5,6}, myarr[5:]...)...)
    fmt.Println(myarr)
}

// [0 1 2 3 4 5 6 7 8]
```

## 数据类型：字典与布尔类型

### 字典

字典（`Map` 类型），是由若干个 `key:value` 这样的键值对映射组合在一起的数据结构。

它是哈希表的一个实现，这就要求它的每个映射里的`key`，都是唯一的，可以使用 `==` 和 `!=` 来进行判等操作，换句话说就是 `key` 必须是可哈希的。

什么叫可哈希的？简单来说，一个不可变对象，都可以用一个哈希值来唯一表示，这样的不可变对象，比如字符串类型的对象（可以说除了切片、 字典，函数之外的其他内建类型都算）。

意思就是，你的 `key` 不能是切片，不能是字典，不能是函数。

字典由 `key` 和 `value` 组成，它们各自有各自的类型。

在声明字典时，必须指定好你的 `key` 和 `value` 是什么类型的，然后使用 `map` 关键字来告诉 `Go` 这是一个字典。

```go
map[KEY_TYPE]VALUE_TYPE
```

### 声明初始化字典

三种声明并初始化字典的方法

```go
// 第一种方法
var scores map[string]int = map[string]int{"english": 80, "chinese": 85}

// 第二种方法
scores := map[string]int{"english": 80, "chinese": 85}

// 第三种方法
scores := make(map[string]int)

// scores["english"] = 80
// scores["chinese"] = 85
```

要注意的是，第一种方法如果拆分成多步（声明、初始化、再赋值），和其他两种有很大的不一样了，相对会比较麻烦（具体请看注释）。

```go
import "fmt"

func main() {
    // 声明一个名为 score 的字典
    var scores map[string]int

    // 未初始化的 score 的零值为nil，无法直接进行赋值
    if scores == nil {
        // 需要使用 make 函数先对其初始化
        scores = make(map[string]int)
    }

    // 经过初始化后，就可以直接赋值
    scores["chinese"] = 90
    fmt.Println(scores)
}
```

### 字典的相关操作

#### 添加元素

```go
scores["math"] = 95
```

#### 更新元素

若 `key` 已存在，则直接更新 `value`

```go
scores["math"] = 100
```

#### 读取元素

直接使用 `[key]` 即可 ，如果 `key` 不存在，也不报错，会返回其 `value-type` 的零值。

```go
fmt.Println(scores["math"])
```

#### 删除元素

使用 `delete` 函数，如果 `key` 不存在，`delete` 函数会静默处理，不会报错。

```go
delete(scores, "math")
```

当访问一个不存在的 `key` 时，并不会直接报错，而是会返回这个 `value` 的零值，如果 `value` 的类型是 `int`，就返回 0。

```go
package main

import "fmt"

func main() {
    scores := make(map[string]int)
    fmt.Println(scores["english"]) // 输出 0
}
```

#### 判断 `key` 是否存在

当 `key` 不存在，会返回 `value-type` 的零值 ，所以你不能通过返回的结果是否是零值来判断对应的 `key` 是否存在，因为 `key` 对应的 `value` 值可能恰好就是零值。

其实字典的下标读取可以返回两个值，使用第二个返回值都表示对应的 `key` 是否存在，若存在 `ok` 为 `true`，若不存在，则 `ok` 为 `false`

```go
import "fmt"

func main() {
    scores := map[string]int{"english": 80, "chinese": 85}
    math, ok := scores["math"]
    if ok {
        fmt.Printf("math 的值是: %d", math)
    } else {
        fmt.Println("math 不存在")
    }
}
```

我们将上面的代码再优化一下

```go
import "fmt"

func main() {
    scores := map[string]int{"english": 80, "chinese": 85}
    if math, ok := scores["math"]; ok {
        fmt.Printf("math 的值是: %d", math)
    } else {
        fmt.Println("math 不存在")
    }
}
```

#### 循环字典

`Go` 语言中没有提供类似 `Python` 的 `keys()` 和 `values()` 这样方便的函数，想要获取，你得自己循环。

循环还分三种

- 获取 `key` 和 `value`

```go
import "fmt"

func main() {
    scores := map[string]int{"english": 80, "chinese": 85}

    for subject, score := range scores {
        fmt.Printf("key: %s, value: %d\n", subject, scores)
    }
}
```

- 只获取 `key`，这里注意不用占用符。

```go
import "fmt"

func main() {
    scores := map[string]int{"english": 80, "chinese": 85}

    for subject := range scores {
        fmt.Printf("key: %s\n", subject)
    }
}
```

- 只获取 `value`，用一个占位符替代。

```go
import "fmt"

func main() {
    scores := map[string]int{"english": 80, "chinese": 85}

    for _, score := range scores {
        fmt.Printf("value: %d\n", score)
    }
}
```

### 布尔类型

关于布尔值，无非就两个值：`true` 和 `false`。只是这两个值，在不同的语言里可能不同。

在 `Go` 中，真值用 `true` 表示，不但不与 1 相等，并且更加严格，不同类型无法进行比较，而假值用 `false` 表示，同样与 0 无法比较。

`Go` 中确实不如 `Python` 那样灵活，`bool` 与 `int` 不能直接转换，如果要转换，需要你自己实现函数。

`bool` 转 `int`

```go
func bool2int(b bool) int {
    if b {
        return 1
    }
    return 0
}
```

`int` 转 `bool`

```go
func int2bool(i int) bool {
    return i != 0
}
```

在 `Go` 中使用 `!` 符号取反值

```go
import "fmt"

var male bool = true
func main()  {
    fmt.Println( !male == false)
    // 或者
    fmt.Println( male != false)
}

// output: true
```

在 `Go` 语言中，则使用 `&&` 表示且，用 `||` 表示或，并且有短路行为（即左边表达式已经可以确认整个表达式的值，那么右边将不会再被求值。

```go
import "fmt"

var age int = 15
var gender string = "male"
func main()  {
    //  && 两边的表达式都会执行
    fmt.Println( age > 18 && gender == "male")
    // gender == "male" 并不会执行
    fmt.Println( age > 18 || gender == "male")
}

// output: false
// output: true
```

## 数据类型：指针

### 什么是指针

当我们定义一个变量 `name`

```go
var name string = "Go编程时光"
```

此时，`name` 是变量名，它只是编程语言中方便程序员编写和理解代码的一个标签。

当我们访问这个标签时，机算机会返回给我们它指向的内存地址里存储的值：`Go编程时光`。

出于某些需要，我们会将这个内存地址赋值给另一个变量名，通常叫做 `ptr`（`pointer` 的简写），而这个变量，我们称之为指针变量。

换句话说，指针变量（一个标签）的值是指针，也就是内存地址。

根据变量指向的值，是否是内存地址，我把变量分为两种：

- 普通变量：存数据值本身

- 指针变量：存值的内存地址

### 指针的创建

指针创建有三种方法

- 第一种方法: 先定义对应的变量，再通过变量取得内存地址，创建指针

```go
// 定义普通变量
aint := 1
// 定义指针变量
ptr := &aint
```

- 第二种方法: 先创建指针，分配好内存后，再给指针指向的内存地址写入对应的值。

```go
// 创建指针
astr := new(string)
// 给指针赋值
*astr = "Go编程时光"
```

- 第三种方法: 先声明一个指针变量，再从其他变量取得内存地址赋值给它

```go
aint := 1
var bint *int  // 声明一个指针
bint = &aint   // 初始化
```

上面的三段代码中，指针的操作都离不开这两个符号：

`&` ：从一个普通变量中取得内存地址

`*` ：当 `*` 在赋值操作值的右边，是从一个指针变量中取得变量值，当 `*` 在赋值操作值的左边，是指该指针指向的变量

通过下面这段代码，你可以熟悉这两个符号的用法

```go
package main

import "fmt"

func main() {
    aint := 1     // 定义普通变量
    ptr := &aint  // 定义指针变量
    fmt.Println("普通变量存储的是：", aint)
    fmt.Println("普通变量存储的是：", *ptr)
    fmt.Println("指针变量存储的是：", &aint)
    fmt.Println("指针变量存储的是：", ptr)
}

// 普通变量存储的是：1
// 普通变量存储的是：1
// 指针变量存储的是： 0xc0000100a0
// 指针变量存储的是： 0xc0000100a0
```

要想打印指针指向的内存地址，方法有两种

```go
// 第一种
fmt.Printf("%p", ptr)

// 第二种
fmt.Println(ptr)
```

### 指针的类型

我们知道字符串的类型是 `string`，整型是 `int`，那么指针如何表示呢？

写段代码试验一下就知道了

```go
package main

import "fmt"

func main() {
    astr := "hello"
    aint := 1
    abool := false
    arune := 'a'
    afloat := 1.2

    fmt.Printf("astr 指针类型是：%T\n", &astr)
    fmt.Printf("aint 指针类型是：%T\n", &aint)
    fmt.Printf("abool 指针类型是：%T\n", &abool)
    fmt.Printf("arune 指针类型是：%T\n", &arune)
    fmt.Printf("afloat 指针类型是：%T\n", &afloat)
}

// astr 指针类型是：*string
// aint 指针类型是：*int
// abool 指针类型是：*bool
// arune 指针类型是：*int32
// afloat 指针类型是：*float64
```

可以发现用 `*+` 所指向变量值的数据类型，就是对应的指针类型。

所以若我们定义一个只接收指针类型的参数的函数，可以这么写

```go
func mytest(ptr *int)  {
    fmt.Println(*ptr)
}
```

### 指针的零值

当指针声明后，没有进行初始化，其零值是 `nil`。

```go
func main() {
    a := 25
    var b *int  // 声明一个指针

    if b == nil {
        fmt.Println(b)
        b = &a  // 初始化：将a的内存地址给b
        fmt.Println(b)
    }
}

// <nil>
// 0xc0000100a0
```

### 指针与切片

切片与指针一样，都是引用类型。

如果我们想通过一个函数改变一个数组的值，有两种方法

- 将这个数组的切片做为参数传给函数

- 将这个数组的指针做为参数传给函数

尽管二者都可以实现我们的目的，但是按照 `Go` 语言的使用习惯，建议使用第一种方法，因为第一种方法，写出来的代码会更加简洁，易读。具体你可以参数下面两种方法的代码实现

```go
// 使用切片
func modify(sls []int) {
    sls[0] = 90
}

func main() {
    a := [3]int{89, 90, 91}
    modify(a[:])
    fmt.Println(a)
}
```

```go
// 使用指针
func modify(arr *[3]int) {
    (*arr)[0] = 90
}

func main() {
    a := [3]int{89, 90, 91}
    modify(&a)
    fmt.Println(a)
}
```

## 面向对象编程：结构体与继承

### 什么是结构体？

在之前学过的数据类型中，数组与切片，只能存储同一类型的变量。若要存储多个类型的变量，就需要用到结构体，它是将多个容易类型的命令变量组合在一起的聚合数据类型。

每个变量都成为该结构体的成员变量。

可以理解为 `Go` 语言的结构体 `struct` 和其他语言的 `class` 有相等的地位，但是 `Go` 语言放弃大量面向对象的特性，所有的 `Go` 语言类型除了指针类型外，都可以有自己的方法,提高了可扩展性。

在 `Go` 语言中没有 `class` 类的概念，只有 `struct` 结构体的概念，因此也没有继承。

### 定义结构体

声明结构体

```go
type 结构体名 struct {
    属性名   属性类型
    属性名   属性类型
    ...
}
```

比如我要定义一个可以存储个人资料名为 `Profile` 的结构体，可以这么写

```go
type Profile struct {
    name   string
    age    int
    gender string
    mother *Profile // 指针
    father *Profile // 指针
}
```

### 定义方法

在 `Go` 语言中，我们无法在结构体内定义方法，那如何给一个结构体定义方法呢，答案是可以使用组合函数的方式来定义结构体方法。它和普通函数的定义方式有些不一样，比如下面这个方法

```go
func (person Profile) FmtProfile() {
    fmt.Printf("名字：%s\n", person.name)
    fmt.Printf("年龄：%d\n", person.age)
    fmt.Printf("性别：%s\n", person.gender)
}
```

其中 `fmt_profile` 是方法名，而(`person Profile`) ：表示将 `fmt_profile` 方法与 `Profile` 的实例绑定。我们把 `Profile` 称为方法的接收者，而 `person` 表示实例本身，在方法内可以使用 `person.属性名` 的方法来访问实例属性。

完整代码如下：

```go
package main

import "fmt"

// 定义一个名为Profile 的结构体
type Profile struct {
    name   string
    age    int
    gender string
    mother *Profile // 指针
    father *Profile // 指针
}

// 定义一个与 Profile 的绑定的方法
func (person Profile) FmtProfile() {
    fmt.Printf("名字：%s\n", person.name)
    fmt.Printf("年龄：%d\n", person.age)
    fmt.Printf("性别：%s\n", person.gender)
}

func main() {
    // 实例化
    myself := Profile{name: "小明", age: 24, gender: "male"}
    // 调用函数
    myself.FmtProfile()
}

// 名字：小明
// 年龄：24
// 性别：male
```

### 方法的参数传递方式

上面定义方法的方式叫当你想要在方法内改变实例的属性的时候，必须使用指针做为方法的接收者。

```go
package main

import "fmt"

// 声明一个 Profile 的结构体
type Profile struct {
    name   string
    age    int
    gender string
    mother *Profile // 指针
    father *Profile // 指针
}

// 重点在于这个星号: *
func (person *Profile) increase_age() {
    person.age += 1
}

func main() {
    myself := Profile{name: "小明", age: 24, gender: "male"}
    fmt.Printf("当前年龄：%d\n", myself.age)
    myself.increase_age()
    fmt.Printf("当前年龄：%d", myself.age)
}

// 当前年龄：24
// 当前年龄：25
```

可以看到在方法内部对 `age` 的修改已经生效。你可以尝试去掉 `*`，使用值做为方法接收者，看看 `age` 是否会发生改变。

至此，我们知道了两种定义方法的方式：

- 以值做为方法接收者

- 以指针做为方法接收者

那我们如何进行选择呢？以下几种情况，应当直接使用指针做为方法的接收者。

- 你需要在方法内部改变结构体内容的时候

- 出于性能的问题，当结构体过大的时候

有些情况下，以值或指针做为接收者都可以，但是考虑到代码一致性，建议都使用**指针做为接收者**。

不管你使用哪种方法定义方法，指针实例对象、值实例对象都可以直接调用，而没有什么约束。这一点 `Go` 语言做得非常好。

### 结构体实现 “继承”

为什么标题的继承，加了双引号，因为 `Go` 语言本身并不支持继承。

但我们可以使用组合的方法，实现类似继承的效果。

在生活中，组合的例子非常多，比如一台电脑，是由机身外壳，主板，CPU，内存等零部件组合在一起，最后才有了我们用的电脑。

同样的，在 `Go` 语言中，把一个结构体嵌入到另一个结构体的方法，称之为组合。

现在这里有一个表示公司（`company`）的结构体，还有一个表示公司职员（`staff`）的结构体。

```go
type company struct {
    companyName string
    companyAddr string
}

type staff struct {
    name string
    age int
    gender string
    position string
}
```

若要将公司信息与公司职员关联起来，一般都会想到将 `company` 结构体的内容照抄到 `staff` 里。

```go
type staff struct {
    name string
    age int
    gender string
    companyName string
    companyAddr string
    position string
}
```

虽然在实现上并没有什么问题，但在你对同一公司的多个 `staff` 初始化的时候，都得重复初始化相同的公司信息，这做得并不好，借鉴继承的思想，我们可以将公司的属性都“继承”过来。

但是在 `Go` 中没有类的概念，只有组合，你可以将 `company` 这个 结构体嵌入到 `staff` 中，做为 `staff` 的一个匿名字段，`staff` 就直接拥有了 `company` 的所有属性了。

```go
type staff struct {
    name string
    age int
    gender string
    position string
    company   // 匿名字段
}
```

来写个完整的程序验证一下。

```go
package main

import "fmt"

type company struct {
    companyName string
    companyAddr string
}

type staff struct {
    name string
    age int
    gender string
    position string
    company
}

func main()  {
    myCom := company{
        companyName: "Tencent",
        companyAddr: "深圳市南山区",
    }
    staffInfo := staff{
        name:     "小明",
        age:      28,
        gender:   "男",
        position: "云计算开发工程师",
        company: myCom,
    }

    fmt.Printf("%s 在 %s 工作\n", staffInfo.name, staffInfo.companyName)
    fmt.Printf("%s 在 %s 工作\n", staffInfo.name, staffInfo.company.companyName)
}

// 小明 在 Tencent 工作
// 小明 在 Tencent 工作
```

### 内部方法与外部方法

在 `Go` 语言中，函数名的首字母大小写非常重要，它被来实现控制对方法的访问权限。

当方法的首字母为大写时，这个方法对于所有包都是 `Public`，其他包可以随意调用

当方法的首字母为小写时，这个方法是 `Private`，其他包是无法访问的。

## 理解 Go 里的函数

### 关于函数

函数是基于功能或逻辑进行封装的可复用的代码结构。将一段功能复杂、很长的一段代码封装成多个代码片段（即函数），有助于提高代码可读性和可维护性。

在 `Go` 语言中，函数可以分为两种：

- 带有名字的普通函数

- 没有名字的匿名函数

由于 `Go` 语言是编译型语言，所以函数编写的顺序是无关紧要的，它不像 `Python` 那样，函数在位置上需要定义在调用之前。

### 函数的声明

函数的声明，使用 `func` 关键字，后面依次接 函数名，参数列表，返回值列表，用 `{ }` 包裹的代码逻辑体

```go
func 函数名(形式参数列表)(返回值列表){
    函数体
}
```

形式参数列表描述了函数的参数名以及参数类型，这些参数作为局部变量，其值由参数调用者提供

返回值列表描述了函数返回值的变量名以及类型，如果函数返回一个无名变量或者没有返回值，返回值列表的括号是可以省略的。

举个例子，定义一个 `sum` 函数，接收两个 `int` 类型的参数，在运行中，将其值分别赋值给 `a`，`b`，并规定必须返回一个 `int` 类型的值 。

```go
func sum(a int, b int) (int){
    return a + b
}

func main() {
    fmt.Println(sum(1,2))
}
```

### 函数实现可变参数

上面举的例子，参数个数都是固定的，这很好理解 ，指定什么类型的参数就传入什么类型的变量，数量上，不能多一个，也不能少一个。（好像没有可选参数）。

可变参数分为几种：

- 多个类型一致的参数

这边定义一个可以对多个数值进行求和的函数，

使用 `...int`，表示一个元素为 `int` 类型的切片，用来接收调用者传入的参数。

```go
// 使用 ...类型，表示一个元素为int类型的切片
func sum(args ...int) int {
    var sum int
    for _, v := range args {
        sum += v
    }
    return sum
}
func main() {
    fmt.Println(sum(1, 2, 3))
}

// output: 6
```

其中 `...` 是 `Go` 语言为了方便程序员写代码而实现的语法糖，如果该函数下会多个类型的函数，这个语法糖必须得是最后一个参数。

同时这个语法糖，只能在定义函数时使用。

- 多个类型不一致的参数

上面那个例子中，我们的参数类型都是 `int`，如果你希望传多个参数且这些参数的类型都不一样，可以指定类型为 `...interface{}`，然后再遍历。

比如下面这段代码，是 `Go` 语言标准库中 `fmt.Printf()` 的函数原型：

```go
import "fmt"

func MyPrintf(args ...interface{}) {
    for _, arg := range args {
        switch arg.(type) {
            case int:
                fmt.Println(arg, "is an int value.")
            case string:
                fmt.Println(arg, "is a string value.")
            case int64:
                fmt.Println(arg, "is an int64 value.")
            default:
                fmt.Println(arg, "is an unknown type.")
        }
    }
}

func main() {
    var v1 int = 1
    var v2 int64 = 234
    var v3 string = "hello"
    var v4 float32 = 1.234
    MyPrintf(v1, v2, v3, v4)
}
```

在某些情况下，我们需要定义一个参数个数可变的函数，具体传入几个参数，由调用者自己决定，但不管传入几个参数，函数都能够处理。

比如这边实现一个累加

```go
func myfunc(args ...int) {
    for _, arg := range args {
        fmt.Println(arg)
    }
}
```

### 多个可变参数函数传递参数

上面提到了可以使用 `...` 来接收多个参数，除此之外，它还有一个用法，就是用来解序列，将函数的可变参数（一个切片）一个一个取出来，传递给另一个可变参数的函数，而不是传递可变参数变量本身。

同样这个用法，也只能在给函数传递参数里使用。

例子如下：

```go
import "fmt"

func sum(args ...int) int {
    var result int
    for _, v := range args {
        result += v
    }
    return result
}

func Sum(args ...int) int {
    // 利用 ... 来解序列
    result := sum(args...)
    return result
}
func main() {
    fmt.Println(sum(1, 2, 3))
}
```

### 函数的返回值

`Go` 语言中的函数，在你定义的时候，就规定了此函数

有没有返回值？

当没有指明返回值的类型时, 函数体可以有 `return`，`Go` 并不像 `Python` 那样没有 `return`，就默认返回 `None`

返回几个值？

`Go` 支持一个函数返回多个值

```go
func double(a int) (int, int) {
   b := a * 2
   return a, b
}
func main() {
   // 接收参数用逗号分隔
   a, b := double(2)
   fmt.Println(a, b)
}
```

怎么返回值?

`Go` 支持返回带有变量名的值

```go
func double(a int) (b int) {
   // 不能使用 := ,因为在返回值哪里已经声明了为int
   b = a * 2
   // 不需要指明写回哪个变量,在返回值类型那里已经指定了
   return
}
func main() {
   fmt.Println(double(2))
}
// output: 4
```

### 方法与函数

方法和函数有什么区别？ 为防有朋友第一次接触面向对象，这里多嘴一句。

方法，是一种特殊的函数。当你一个函数和对象/结构体进行绑定的时候，我们就称这个函数是一个方法。

### 匿名函数的使用

所谓匿名函数，就是没有名字的函数，它只有函数逻辑体，而没有函数名。

定义的格式如下

```go
func(参数列表)(返回参数列表){
    函数体
}
```

一个名字实际上并没有多大区别，所有使用匿名函数都可以改成普通有名函数，那么什么情况下，会使用匿名函数呢？

定义变量名，是一个不难但是还费脑子的事情，对于那到只使用一次的函数，是没必要拥有姓名的。这才有了匿名函数。

有了这个背景，决定了匿名函数只有拥有短暂的生命，一般都是定义后立即使用。

就像这样，定义后立马执行（这里只是举例，实际代码没有意义）。

```go
func(data int) {
    fmt.Println("hello", data)
}(100)
```

亦或是做为回调函数使用

```go
// 第二个参数为函数
func visit(list []int, f func(int)) {
    for _, v := range list {
        // 执行回调函数
        f(v)
    }
}
func main() {
    // 使用匿名函数直接做为参数
    visit([]int{1, 2, 3, 4}, func(v int) {
        fmt.Println(v)
    })
}
```

## 语言流程控制：if-else​

### 条件语句模型

`Go` 里的流程控制方法还是挺丰富，整理了下有如下这么多种：

- `if - else` 条件语句

- `switch - case` 选择语句

- `for - range` 循环语句

- `goto` 无条件跳转语句

- `defer` 延迟执行

先来讲讲 `if-else` 条件语句, `Go` 里的条件语句模型是这样的

```go
if 条件 1 {
  分支 1
} else if 条件 2 {
  分支 2
} else if 条件 ... {
  分支 ...
} else {
  分支 else
}
```

`Go` 编译器，对于 `{` 和 `}` 的位置有严格的要求，它要求 `else if` （或 `else`）和 两边的花括号，必须在同一行。

由于 `Go` 是强类型，所以要求你条件表达式必须严格返回布尔型的数据（`nil` 和 0 和 1 都不行）。

### 单分支判断

只有一个 `if` ，没有 `else`

```go
import "fmt"

func main() {
    age := 20
    if age > 18 {
        fmt.Println("已经成年了")
    }
}
```

如果条件里需要满足多个条件，可以使用 `&&` 和 `||`

`&&` ：表示且，左右都需要为 `true`，最终结果才能为 `true`，否则为 `false`

`||` ：表示或，左右只要有一个为 `true`，最终结果即为 `true`，否则为 `false`

```go
import "fmt"

func main() {
    age := 20
    gender := "male"
    if (age > 18 && gender == "male") {
        fmt.Println("是成年男性")
    }
}
```

### 多分支判断

`if - else` 语句

```go
import "fmt"

func main() {
    age := 20
    if age > 18 {
        fmt.Println("已经成年了")
    } else {
        fmt.Println("还未成年")
    }
}
```

`if - else if - else` 语句

```go
import "fmt"

func main() {
    age := 20
    if age > 18 {
        fmt.Println("已经成年了")
    } else if age >12 {
        fmt.Println("已经是青少年了")
    } else {
        fmt.Println("还不是青少年")
    }
}
```

### 高级写法

在 `if` 里可以允许先运行一个表达式，取得变量后，再对其进行判断，比如第一个例子里代码也可以写成这样

```go
import "fmt"

func main() {
    if age := 20;age > 18 {
        fmt.Println("已经成年了")
    }
}
```

## 语言流程控制：switch-case

### 语句模型

`Go` 里的选择语句模型是这样的

```go
switch 表达式 {
    case 表达式1:
        代码块
    case 表达式2:
        代码块
    case 表达式3:
        代码块
    case 表达式4:
        代码块
    case 表达式5:
        代码块
    default:
        代码块
}
```

拿 `switch` 后的表达式分别和 `case` 后的表达式进行对比，只要有一个 `case` 满足条件，就会执行对应的代码块，然后直接退出 `switch - case` ，如果 一个都没有满足，才会执行 `default` 的代码块。

### 最简单的示例

`switch` 后接一个你要判断变量 `education` （学历），然后 `case` 会拿这个 变量去和它后面的表达式（可能是常量、变量、表达式等）进行判等。

如果相等，就执行相应的代码块。如果不相等，就接着下一个 `case`。

```go
import "fmt"

func main() {
    education := "本科"

    switch education {
    case "博士":
        fmt.Println("我是博士")
    case "研究生":
        fmt.Println("我是研究生")
    case "本科":
        fmt.Println("我是本科生")
    case "大专":
        fmt.Println("我是大专生")
    case "高中":
        fmt.Println("我是高中生")
    default:
        fmt.Println("学历未达标..")
    }
}

// 我是本科生
```

### 一个 case 多个条件

`case` 后可以接多个多个条件，多个条件之间是 "或" 的关系，用逗号相隔。

```go
import "fmt"

func main() {
    month := 2

    switch month {
    case 3, 4, 5:
        fmt.Println("春天")
    case 6, 7, 8:
        fmt.Println("夏天")
    case 9, 10, 11:
        fmt.Println("秋天")
    case 12, 1, 2:
        fmt.Println("冬天")
    default:
        fmt.Println("输入有误...")
    }
}

// 冬天
```

### case 条件常量不能重复

当 `case` 后接的是常量时，该常量只能出现一次。

以下两种情况，在编译时，都会报错：`duplicate case "male" in switch`

错误案例一

```go
gender := "male"

switch gender {
    case "male":
        fmt.Println("男性")
    // 与上面重复
    case "male":
        fmt.Println("男性")
    case "female":
        fmt.Println("女性")
}
```

错误案例二

```go
gender := "male"

switch gender {
    case "male", "male":
        fmt.Println("男性")
    case "female":
        fmt.Println("女性")
}
```

### switch 后可接函数

`switch` 后面可以接一个函数，只要保证 `case` 后的值类型与函数的返回值 一致即可。

```go
import "fmt"

// 判断一个同学是否有挂科记录的函数
// 返回值是布尔类型
func getResult(args ...int) bool {
    for _, i := range args {
        if i < 60 {
            return false
        }
    }
    return true
}

func main() {
    chinese := 80
    english := 50
    math := 100

    switch getResult(chinese, english, math) {
    // case 后也必须 是布尔类型
    case true:
        fmt.Println("该同学所有成绩都合格")
    case false:
        fmt.Println("该同学有挂科记录")
    }
}
```

### switch 可不接表达式

`switch` 后可以不接任何变量、表达式、函数。

当不接任何东西时，`switch - case` 就相当于 `if - elseif - else`

```go
score := 30

switch {
    case score >= 95 && score <= 100:
        fmt.Println("优秀")
    case score >= 80:
        fmt.Println("良好")
    case score >= 60:
        fmt.Println("合格")
    case score >= 0:
        fmt.Println("不合格")
    default:
        fmt.Println("输入有误...")
}
```

### switch 的穿透能力

正常情况下 `switch - case` 的执行顺序是：只要有一个 `case` 满足条件，就会直接退出 `switch - case` ，如果一个都没有满足，才会执行 `default` 的代码块。但是有一种情况是例外。

那就是当 `case` 使用关键字 `fallthrough` 开启穿透能力的时候。

```go
s ：= "hello"
switch {
case s == "hello":
    fmt.Println("hello")
    fallthrough
case s != "world":
    fmt.Println("world")
}

// hello
// world
```

需要注意的是，`fallthrough` 只能穿透一层，意思是它只给你一次再判断 `case` 的机会，不管你有没有匹配上，都要退出了。

```go
s := "hello"
switch {
case s == "hello":
    fmt.Println("hello")
    fallthrough
case s == "xxxx":
    fmt.Println("xxxx")
case s != "world":
    fmt.Println("world")
}

// hello
// xxxx
```

## 语言流程控制：for 循环

### 语句模型

这是 `for` 循环的基本模型。

```go
for [condition |  ( init; condition; increment ) | Range]
{
   statement(s);
}
```

可以看到 `for` 后面，可以接三种类型的表达式。

- 接一个条件表达式

- 接三个表达式

- 接一个 range 表达式

但其实还有第四种, 就是：不接表达式

- 接一个条件表达式

这个例子会打印 1 到 5 的数值。

```go
a := 1
for a <= 5 {
    fmt.Println(a)
    a ++
}

// 1
// 2
// 3
// 4
// 5
```

- 接三个表达式

`for` 后面，紧接着三个表达式，使用 `;` 分隔。

这三个表达式，各有各的用途

- 第一个表达式：初始化控制变量，在整个循环生命周期内，只运行一次；

- 第二个表达式：设置循环控制条件，当返回 true，继续循环，返回 false，结束循环；

- 第三个表达式：每次循完开始（除第一次）时，给控制变量增量或减量。

这边的例子和上面的例子，是等价的。

```go
import "fmt"

func main() {
    for i := 1; i <= 5; i++ {
        fmt.Println(i)
    }
}

// 1
// 2
// 3
// 4
// 5
```

- 不接表达式：无限循环

在 `Go` 语言中，没有 `while` 循环，如果要实现无限循环，也完全可以 `for` 来实现。

当你不加任何的判断条件时， 就相当于你每次的判断都为 `true`，程序就会一直处于运行状态，但是一般我们并不会让程序处于死循环，在满足一定的条件下，可以使用关键字 `break` 退出循环体，也可以使用 `continue` 直接跳到下一循环。

下面两种写法都是无限循环的写法。

```go
for {
    代码块
}

// 等价于
for ;; {
    代码块
}
举个例子

import "fmt"

func main() {
    var i int = 1
    for {
        if i > 5 {
            break
        }
        fmt.Printf("hello, %d\n", i)
        i++
    }
}

// hello, 1
// hello, 2
// hello, 3
// hello, 4
// hello, 5
```

- 接 `for-range` 语句

遍历一个可迭代对象，是一个很常用的操作。在 `Go` 可以使用 `for-range` 的方式来实现。

`range` 后可接数组、切片，字符串等

由于 `range` 会返回两个值：索引和数据，若你后面的代码用不到索引，需要使用 `_` 表示 。

```go
import "fmt"

func main() {
    myarr := [...]string{"world", "python", "go"}
    for _, item := range myarr {
        fmt.Printf("hello, %s\n", item)
    }
}

// hello, world
// hello, python
// hello, go
```

## 语言流程控制：goto

### 基本模型

`goto` 顾言思义，是跳转的意思。

`goto` 后接一个标签，这个标签的意义是告诉 `Go` 程序下一步要执行哪里的代码。

所以这个标签如何放置，放置在哪里，是 `goto` 里最需要注意的。

```go
goto 标签;
...
...
标签: 表达式;
```

### 最简单的示例

`goto` 可以打破原有代码执行顺序，直接跳转到某一行执行代码。

```go
import "fmt"

func main() {

    goto flag
    fmt.Println("B")
flag:
    fmt.Println("A")

}
```

执行结果，并不会输出 B ，而只会输出 A

### 如何使用？

`goto` 语句通常与条件语句配合使用。可用来实现条件转移， 构成循环，跳出循环体等功能。

这边举一个例子，用 `goto` 的方式来实现一个打印 1 到 5 的循环。

```go
import "fmt"

func main() {
    i := 1
flag:
    if i <= 5 {
        fmt.Println(i)
        i++
        goto flag
    }
}

// 1
// 2
// 3
// 4
// 5
```

再举个例子，使用 `goto` 实现 类型 `break` 的效果。

```go
import "fmt"

func main() {
    i := 1
    for {
        if i > 5 {
            goto flag
        }
        fmt.Println(i)
        i++
    }
flag:
}

// 1
// 2
// 3
// 4
// 5
```

最后再举个例子，使用 `goto` 实现 类型 `continue` 的效果，打印 1 到 10 的所有偶数。

```go
import "fmt"

func main() {
    i := 1
flag:
    for i <= 10 {
        if i%2 == 1 {
            i++
            goto flag
        }
        fmt.Println(i)
        i++
    }
}

// 2
// 4
// 6
// 8
// 10
```

### 注意事项

`goto` 语句与标签之间不能有变量声明，否则编译错误。

```go
import "fmt"

func main() {
    fmt.Println("start")
    goto flag
    var say = "hello oldboy"
    fmt.Println(say)
flag:
    fmt.Println("end")
}
```

编译错误

```bash
.\main.go:7:7: goto flag jumps over declaration of say at .\main.go:8:6
```

## 语言流程控制：defer 延迟调用

### 延迟调用

`defer` 的用法很简单，只要在后面跟一个函数的调用，就能实现将这个 `xxx` 函数的调用延迟到当前函数执行完后再执行。

```go
defer xxx()
```

这是一个很简单的例子，可以很快帮助你理解 `defer` 的使用效果。

```go
import "fmt"

func myfunc() {
    fmt.Println("B")
}

func main() {
    defer myfunc()
    fmt.Println("A")
}

// A
// B
```

当然了，对于上面这个例子可以简写为成如下，输出结果是一致的

```go
import "fmt"

func main() {
    defer fmt.Println("B")
    fmt.Println("A")
}
```

### 即时求值的变量快照

使用 `defer` 只是延时调用函数，此时传递给函数里的变量，不应该受到后续程序的影响。

比如这边的例子

```go
import "fmt"

func main() {
    name := "go"
    defer fmt.Println(name) // 输出: go

    name = "python"
    fmt.Println(name)      // 输出: python
}

// python
// go
```

可见给 `nam`e 重新赋值为 `python`，后续调用 `defer` 的时候，仍然使用未重新赋值的变量值，就好像在 `defer` 这里，给所有的变量做了一个快照一样。

### 多个 defer 反序调用

当我们在一个函数里使用了多个 `defer`，那么这些 `defer` 的执行函数是如何的呢？

```go
import "fmt"

func main() {
    name := "go"
    defer fmt.Println(name) // 输出: go

    name = "python"
    defer fmt.Println(name) // 输出: python

    name = "java"
    fmt.Println(name)
}

// java
// python
// go
```

可见 多个 `defer` 是反序调用的，有点类似栈一样，后进先出。

### defer 与 return 孰先孰后

至此，`defer` 还算是挺好理解的。在一般的使用上，是没有问题了。

在这里提一个稍微复杂一点的问题，`defer` 和 `return` 到底是哪个先调用？

使用下面这段代码，可以很容易的观察出来

```go
import "fmt"

var name string = "go"

func myfunc() string {
    defer func() {
        name = "python"
    }()

    fmt.Printf("myfunc 函数里的name：%s\n", name)
    return name
}

func main() {
    myname := myfunc()
    fmt.Printf("main 函数里的name: %s\n", name)
    fmt.Println("main 函数里的myname: ", myname)
}

// myfunc 函数里的name：go
// main 函数里的name: python
// main 函数里的myname:  go
```

来一起理解一下这段代码，第一行很直观，`name` 此时还是全局变量，值还是 `go`

第二行也不难理解，在 `defer` 里改变了这个全局变量，此时 `name` 的值已经变成了 `python`

重点在第三行，为什么输出的是 `go` ？

解释只有一个，那就是 `defer` 是 `return` 后才调用的。所以在执行 `defer` 前，`myname` 已经被赋值成 `go` 了。

### 为什么要有 defer？

你可能会有疑问，这也没什么意义呀，我把这个放在 `defer` 执行的函数放在 `return` 那里执行不就好了。

固然可以，但是当一个函数里有多个 `return` 时，你得多调用好多次这个函数，代码就臃肿起来了。

若是没有 `defer`，你可能这样写代码

```go
func f() {
    r := getResource()  //0，获取资源
    ......
    if ... {
        r.release()  //1，释放资源
        return
    }
    ......
    if ... {
        r.release()  //2，释放资源
        return
    }
    ......
    if ... {
        r.release()  //3，释放资源
        return
    }
    ......
    r.release()     //4，释放资源
    return
}
```

使用了 `defer` 后，代码就显得简单直接了，不管你在何处 `return`，都会执行 `defer` 后的函数。

```go
func f() {
    r := getResource()  //0，获取资源

    defer r.release()  //1，释放资源
    ......
    if ... {
        ...
        return
    }
    ......
    if ... {
        ...
        return
    }
    ......
    if ... {
        ...
        return
    }
    ......
    return
}
```

## 面向对象编程：接口与多态

### 接口是什么？

在面向对象的领域里，接口一般这样定义：接口定义一个对象的行为。接口只指定了对象应该做什么，至于如何实现这个行为（即实现细节），则由对象本身去确定。

在 `Go` 语言中，接口就是方法签名（`Method Signature`）的集合。当一个类型定义了接口中的所有方法，我们称它实现了该接口。这与面向对象编程（`OOP`）的说法很类似。接口指定了一个类型应该具有的方法，并由该类型决定如何实现这些方法。

#### 如何定义接口

使用 `type` 关键字来定义接口。

如下代码，定义了一个电话接口，要求实现 `call` 方法。

```go
type Phone interface {
   call()
}
```

#### 如何实现接口

如果有一个类型/结构体，实现了一个接口要求的所有方法，这里 `Phone` 接口只有 `call` 方法，所以只要实现了 `call` 方法，我们就可以称它实现了 `Phone` 接口。

意思是如果有一台机器，可以给别人打电话，那么我们就可以把它叫做电话。

这个接口的实现是隐式的，不像 `JAVA` 中要用 `implements` 显示说明。

继续上面电话的例子，我们先定义一个 `Nokia` 的结构体，而它实现了 `call` 的方法，所以它也是一台电话。

```go
type Nokia struct {
    name string
}

// 接收者为 Nokia
func (phone Nokia) call() {
    fmt.Println("我是 Nokia，是一台电话")
}
```

#### 接口实现多态

鸭子类型（`Duck typing`）的定义是，只要你长得像鸭子，叫起来也像鸭子，那我认为你就是一只鸭子。

举个通俗的例子

什么样子的人可以称做老师呢？

不同的人标准不一，有的人认为必须有一定的学历，有的人认为必须要有老师资格证。

而我认为只要能育人，能给传授给其他人知识的，都可以称之为老师。

而不管你教的什么学科？是体育竞技，还是教人烹饪。

也不管你怎么教？是在教室里手执教教鞭、拿着粉笔，还是追求真实，直接实战演练。

通通不管。

这就一个接口（老师）下，在不同对象（人）上的不同表现。这就是多态。

在 `Go` 语言中，是通过接口来实现的多态。

这里以商品接口来写一段代码演示一下。

先定义一个商品（`Good`）的接口，意思是一个类型或者结构体，只要实现了 `settleAccount()` 和 `orderInfo()` 两个方法，那这个类型/结构体就是一个商品。

```go
type Good interface {
    settleAccount() int
    orderInfo() string
}
```

然后我们定义两个结构体，分别是手机和赠品。

```go
type Phone struct {
    name string
    quantity int
    price int
}

type FreeGift struct {
    name string
    quantity int
    price int
}
```

然后分别为他们实现 `Good` 接口的两个方法

```go
// Phone
func (phone Phone) settleAccount() int {
    return phone.quantity * phone.price
}

func (phone Phone) orderInfo() string{
    return "您要购买" + strconv.Itoa(phone.quantity)+ "个" +
        phone.name + "计：" + strconv.Itoa(phone.settleAccount()) + "元"
}

// FreeGift
func (gift FreeGift) settleAccount() int {
    return 0
}

func (gift FreeGift) orderInfo() string{
    return "您要购买" + strconv.Itoa(gift.quantity)+ "个" +
        gift.name + "计：" + strconv.Itoa(gift.settleAccount()) + "元"
}
```

实现了 `Good` 接口要求的两个方法后，手机和赠品在 `Go` 语言看来就都是商品（`Good`）类型了。

这里候，我挑选了两件商品（实例化），分别是手机和耳机（赠品，不要钱）

```go
iPhone := Phone{
    name:     "iPhone",
    quantity: 1,
    price:    8000,
}

earphones := FreeGift{
    name:     "耳机",
    quantity: 1,
    price:    200,
}
```

然后创建一个购物车（也就是类型为 `Good` 的切片），来存放这些商品。

```go
goods := []Good{iPhone, earphones}
```

最后，定义一个方法来计算购物车里的订单金额

```go
func calculateAllPrice(goods []Good) int {
    var allPrice int
    for _,good := range goods{
        fmt.Println(good.orderInfo())
        allPrice += good.settleAccount()
    }
    return allPrice
}
```

完整代码如下：

```go
package main

import (
    "fmt"
    "strconv"
)

// 定义一个接口
type Good interface {
    settleAccount() int
    orderInfo() string
}

type Phone struct {
    name string
    quantity int
    price int
}

func (phone Phone) settleAccount() int {
    return phone.quantity * phone.price
}

func (phone Phone) orderInfo() string{
    return "您要购买" + strconv.Itoa(phone.quantity)+ "个" +
        phone.name + "计：" + strconv.Itoa(phone.settleAccount()) + "元"
}

type FreeGift struct {
    name string
    quantity int
    price int
}

func (gift FreeGift) settleAccount() int {
    return 0
}

func (gift FreeGift) orderInfo() string{
    return "您要购买" + strconv.Itoa(gift.quantity)+ "个" +
        gift.name + "计：" + strconv.Itoa(gift.settleAccount()) + "元"
}

func calculateAllPrice(goods []Good) int {
    var allPrice int
    for _,good := range goods{
        fmt.Println(good.orderInfo())
        allPrice += good.settleAccount()
    }
    return allPrice
}

func main()  {
    iPhone := Phone{
        name:     "iPhone",
        quantity: 1,
        price:    8000,
    }
    earphones := FreeGift{
        name:     "耳机",
        quantity: 1,
        price:    200,
    }

    goods := []Good{iPhone, earphones}
    allPrice := calculateAllPrice(goods)
    fmt.Printf("该订单总共需要支付 %d 元", allPrice)
}

// 您要购买1个iPhone计：8000元
// 您要购买1个耳机计：0元
```

## 关键字：make 和 new 的区别

### `new` 函数

在官方文档中，`new` 函数的描述如下

> // The new built-in function allocates memory. The first argument is a type,
> // not a value, and the value returned is a pointer to a newly
> // allocated zero value of that type.

> func new(Type) \*Type

可以看到，`new` 只能传递一个参数，该参数为一个任意类型，可以是 `Go` 语言内建的类型，也可以是你自定义的类型

那么 `new` 函数到底做了哪些事呢：

- 分配内存

- 设置零值

- 返回指针（重要）

举个例子

```go
import "fmt"

type Student struct {
   name string
   age int
}

func main() {
    // new 一个内建类型
    num := new(int)
    fmt.Println(*num) //打印零值：0

    // new 一个自定义类型
    s := new(Student)
    s.name = "wangbm"
}
```

### make 函数

在官方文档中，`make` 函数的描述如下

> //The make built-in function allocates and initializes an object
> //of type slice, map, or chan (only). Like new, the first argument is
> // a type, not a value. Unlike new, make's return type is the same as
> // the type of its argument, not a pointer to it.

> func make(t Type, size …IntegerType) Type

内建函数 `make` 用来为 `slice`，`map` 或 `chan` 类型（注意：也只能用在这三种类型上）分配内存和初始化一个对象

`make` 返回类型的本身而不是指针，而返回值也依赖于具体传入的类型，因为这三种类型（`slice`，`map` 和 `chan`）本身就是引用类型，所以就没有必要返回他们的指针了

由于这三种类型都是引用类型，所以必须得初始化（`size` 和 `cap`），但是不是置为零值，这个和 `new` 是不一样的。

举几个例子

```go
//切片
a := make([]int, 2, 10)

// 字典
b := make(map[string]int)

// 通道
c := make(chan int, 10)
```

### 总结

`new` ：为所有的类型分配内存，并初始化为零值，返回指针。

`make` ：只能为 `slice`，`map`，`chan` 分配内存，并初始化，返回的是类型。

另外，目前来看 `new` 函数并不常用，大家更喜欢使用短语句声明的方式。

```go
a := new(int)
a = 1
// 等价于
a := 1
```

但是 `make` 就不一样了，它的地位无可替代，在使用`slice`、`map` 以及 `channel` 的时候，还是要使用 `make` 进行初始化，然后才可以对他们进行操作。

## Go 的语句块与作用域

由于 `Go` 使用的是词法作用域，而词法作用域依赖于语句块。所以在讲作用域时，需要先了解一下 `Go` 中的语句块是怎么一回事？

### 显示语句块与隐式语句块

通俗地说，语句块是由花括弧（`{}`）所包含的一系列语句。

语句块内部声明的名字是无法被外部块访问的。这个块决定了内部声明的名字的作用域范围，也就是作用域。

用花括弧包含的语句块，属于显示语句块。

在 `Go` 中还有很多的隐式语句块：

主语句块：包括所有源码，对应内置作用域

包语句块：包括该包中所有的源码（一个包可能会包括一个目录下的多个文件），对应包级作用域

文件语句块：包括该文件中的所有源码，对应文件级作用域

`for` 、`if`、`switch` 等语句本身也在它自身的隐式语句块中，对应局部作用域

前面三点好理解，第四点举几个例子

`for` 循环完后， 不能再使用变量 `i`

```go
for i := 0; i < 5; i++ {
    fmt.Println(i)
}
```

`if` 语句判断完后，同样不能再使用变量 `i`

```go
if i := 0; i >= 0 {
    fmt.Println(i)
}
```

`switch` 语句完了后，也是不是再使用变量 `i`

```go
switch i := 2; i * 4 {
case 8:
    fmt.Println(i)
default:
    fmt.Println(“default”)
}
```

且每个 `switch` 语句的子句都是一个隐式的语句块

```go
switch i := 2; i * 4 {
case 8:
    j := 0
    fmt.Println(i, j)
default:
    // "j" is undefined here
    fmt.Println(“default”)
}
// "j" is undefined here
```

### 四种作用域的理解

变量的声明，除了声明其类型，其声明的位置也有讲究，不同的位置决定了其拥有不同的作用范围，说白了就是我这个变量，在哪里可用，在哪里不可用。

根据声明位置的不同，作用域可以分为以下四个类型：

- 内置作用域：不需要自己声明，所有的关键字和内置类型、函数都拥有全局作用域

- 包级作用域：必須函数外声明，在该包内的所有文件都可以访问

- 文件级作用域：不需要声明，导入即可。一个文件中通过 `import` 导入的包名，只在该文件内可用

- 局部作用域：在自己的语句块内声明，包括函数，`for`、`if` 等语句块，或自定义的 `{}` 语句块形成的作用域，只在自己的局部作用域内可用

以上的四种作用域，从上往下，范围从大到小，为了表述方便，我这里自己将范围大的作用域称为高层作用域，而范围小的称为低层作用域。

对于作用域，有以下几点总结：

- 低层作用域，可以访问高层作用域

- 同一层级的作用域，是相互隔离的

- 低层作用域里声明的变量，会覆盖高层作用域里声明的变量

在这里要注意一下，不要将作用域和生命周期混为一谈。声明语句的作用域对应的是一个源代码的文本区域；它是一个编译时的属性。

而一个变量的生命周期是指程序运行时变量存在的有效时间段，在此时间区域内它可以被程序的其他部分引用；是一个运行时的概念。

### 静态作用域与动态作用域

根据局部作用域内变量的可见性，是否是静态不变，可以将编程语言分为如下两种：

静态作用域，如 `Go` 语言

动态作用域，如 `Shell` 语言

具体什么是动态作用域，这里用 `Shell` 的代码演示一下，你就知道了

```shell
#!/bin/bash
func01() {
    local value=1
    func02
}
func02() {
    echo "func02 sees value as ${value}"
}

# 执行函数
# func01
# func02
```

从代码中，可以看到在 `func01` 函数中定义了个局部变量 `value`，按理说，这个 `value` 变量只在该函数内可用，但由于在 `shell` 中的作用域是动态的，所以在 `func01` 中也可以调用 `func02` 时，`func02` 可以访问到 `value` 变量，此时的 `func02` 作用域可以当成是局部作用域中（`func01`）的局部作用域。

但若脱离了 `func01` 的执行环境，将其放在全局环境下或者其他函数中， `func02` 是访问不了 `value` 变量的。

所以此时的输出结果是

```shell
func02 sees value as 1
func02 sees value as
```

但在 `Go` 中并不存在这种动态作用域，比如这段代码，在 `func01` 函数中，要想取得 `name` 这个变量，只能从 `func01` 的作用域或者更高层作用域里查找（文件级作用域，包级作用域和内置作用域），而不能从调用它的另一个局部作用域中（因为他们在层级上属于同一级）查找。

```go
import "fmt"

func func01() {
    fmt.Println("在 func01 函数中，name：", name)
}

func main()  {
    var name string = "Python编程时光"
    fmt.Println("在 main 函数中，name：", name)

    func01()
}
```

因此你在执行这段代码时，会报错，提示在 `func01` 中的 `name` 还未定义。

## 学习 Go 协程：goroutine

说到 `Go` 语言，很多没接触过它的人，对它的第一印象，一定是它从语言层面天生支持并发，非常方便，让开发者能快速写出高性能且易于理解的程序。

在其他开发语言里，你需要要学习多进程，多线程，还要掌握各种支持并发的库，同时你还要清楚它们之间的区别及优缺点，懂得在不同的场景选择不同的并发模式。

而 `Golang` 作为一门现代化的编程语言，它不需要你直面这些复杂的问题。在 `Golang` 里，你不需要学习如何创建进程池/线程池，也不需要知道什么情况下使用多线程，什么时候使用多进程。因为你没得选，也不需要选，它原生提供的 `goroutine` （也即协程）已经足够优秀，能够自动帮你处理好所有的事情，而你要做的只是执行它，就这么简单。

一个 `goroutine` 本身就是一个函数，当你直接调用时，它就是一个普通函数，如果你在调用前加一个关键字 `go` ，那你就开启了一个 `goroutine`。

```go
// 执行一个函数
func()

// 开启一个协程执行这个函数
go func()
```

### 协程的初步使用

一个 `Go` 程序的入口通常是 `main` 函数，程序启动后，`main` 函数最先运行，我们称之为 `main goroutine`。

在 `main` 中或者其下调用的代码中才可以使用 `go + func()` 的方法来启动协程。

`main` 的地位相当于主线程，当 `main` 函数执行完成后，这个线程也就终结了，其下的运行着的所有协程也不管代码是不是还在跑，也得乖乖退出。

因此如下这段代码运行完，只会输出 `hello, world` ，而不会输出 `hello, go` （因为协程的创建需要时间，当 `hello, world` 打印后，协程还没来得及并执行）。

```go
import "fmt"

func mytest() {
    fmt.Println("hello, go")
}

func main() {
    // 启动一个协程
    go mytest()
    fmt.Println("hello, world")
}
```

对于刚学习 `Go` 的协程同学来说，可以使用 `time.Sleep` 来使 `main` 阻塞，使其他协程能够有机会运行完全，但你要注意的是，这并不是推荐的方式（后续我们会学习其他更优雅的方式）。

当我在代码中加入一行 `time.Sleep` 输出就符合预期了。

```go
import (
    "fmt"
    "time"
)

func mytest() {
    fmt.Println("hello, go")
}

func main() {
    go mytest()
    fmt.Println("hello, world")
    time.Sleep(time.Second)
}

// hello, world
// hello, go
```

### 多个协程的效果

为了让你看到并发的效果，这里举个最简单的例子

```go
import (
    "fmt"
    "time"
)

func mygo(name string) {
    for i := 0; i < 10; i++ {
        fmt.Printf("In goroutine %s\n", name)
        // 为了避免第一个协程执行过快，观察不到并发的效果，加个休眠
        time.Sleep(10 * time.Millisecond)
    }
}

func main() {
    go mygo("协程1号") // 第一个协程
    go mygo("协程2号") // 第二个协程
    time.Sleep(time.Second)
}

// In goroutine 协程2号
// In goroutine 协程1号
// In goroutine 协程1号
// In goroutine 协程2号
// In goroutine 协程2号
// In goroutine 协程1号
// In goroutine 协程1号
// In goroutine 协程2号
// In goroutine 协程1号
// In goroutine 协程2号
// In goroutine 协程1号
// In goroutine 协程2号
// In goroutine 协程1号
// In goroutine 协程2号
// In goroutine 协程1号
// In goroutine 协程2号
// In goroutine 协程1号
// In goroutine 协程2号
// In goroutine 协程1号
// In goroutine 协程2号
```

可以观察到两个协程就如两个线程一样，并发执行, 通过以上简单的例子，是不是折服于 `Go` 的这种强大的并发特性，将同步代码转为异步代码，真的只要一个关键字就可以了，也不需要使用其他库，简单方便。

本篇只介绍了协程的简单使用，真正的并发程序还是要结合信道（ `channel` ）来实现。关于信道的内容，将在下一篇文章中介绍。

## Go 协程：详解信道/通道

### 前言

`goroutine` 是 `Go` 语言程序的并发执行的基本单元，多个 `goroutine` 的通信是需要依赖本文的主人公 —— `channel` 。`channel`，中文翻译有叫通道，也有叫信道的。以下为了方便，我统一称之为 信道 。

信道，就是一个管道，连接多个 `goroutine` 程序 ，它是一种队列式的数据结构，遵循先入先出的规则。

### 信道的定义与使用

每个信道都只能传递一种数据类型的数据，所以在你声明的时候，你得指定数据类型（ `string` `int` 等等）

```go
var 信道实例 chan 信道类型
```

声明后的信道，其零值是 `nil`，无法直接使用，必须配合 `make` 函进行初始化。

```go
信道实例 = make(chan 信道类型)
```

亦或者，上面两行可以合并成一句，以下我都使用这样的方式进行信道的声明

```go
信道实例 := make(chan 信道类型)
```

假如我要创建一个可以传输 `int` 类型的信道，可以这样子写。

```go
// 定义信道
pipline := make(chan int)
```

信道的数据操作，无非就两种：发送数据与读取数据

```go
// 往信道中发送数据
pipline <- 200

// 从信道中取出数据，并赋值给mydata
mydata := <- pipline
```

信道用完了，可以对其进行关闭，避免有人一直在等待。

```go
close(pipline)
```

对一个已关闭的信道再关闭，是会报错的。所以我们还要学会，如何判断一个信道是否被关闭？

当从信道中读取数据时，可以有多个返回值，其中第二个可以表示 信道是否被关闭，如果已经被关闭，`ok` 为 `false`，若还没被关闭，`ok` 为 `true`。

```go
x, ok := <-pipline
```

### 信道的容量与长度

一般创建信道都是使用 `make` 函数，`make` 函数接收两个参数

- 第一个参数：必填，指定信道类型

- 第二个参数：选填，不填默认为 0，指定信道的容量（可缓存多少数据）

对于信道的容量，很重要，这里要多说几点：

- 当容量为 0 时，说明信道中不能存放数据，在发送数据时，必须要求立马有人接收，否则会报错。此时的信道称之为无缓冲信道。

- 当容量为 1 时，说明信道只能缓存一个数据，若信道中已有一个数据，此时再往里发送数据，会造成程序阻塞。 利用这点可以利用信道来做锁。

- 当容量大于 1 时，信道中可以存放多个数据，可以用于多个协程之间的通信管道，共享资源。

至此我们知道，信道就是一个容器。

若将它比做一个纸箱子

它可以装 10 本书，代表其容量为 10

当前只装了 1 本书，代表其当前长度为 1

信道的容量，可以使用 `cap` 函数获取 ，而信道的长度，可以使用 `len` 长度获取。

```go
package main

import "fmt"

func main() {
    pipline := make(chan int, 10)
    fmt.Printf("信道可缓冲 %d 个数据\n", cap(pipline))
    pipline<- 1
    fmt.Printf("信道中当前有 %d 个数据", len(pipline))
}

// 信道可缓冲 10 个数据
// 信道中当前有 1 个数据
```

### 缓冲信道与无缓冲信道

按照是否可缓冲数据可分为：缓冲信道 与 无缓冲信道

- 缓冲信道

允许信道里存储一个或多个数据，这意味着，设置了缓冲区后，发送端和接收端可以处于异步的状态。

```go
pipline := make(chan int, 10)
```

- 无缓冲信道

在信道里无法存储数据，这意味着，接收端必须先于发送端准备好，以确保你发送完数据后，有人立马接收数据，否则发送端就会造成阻塞，原因很简单，信道中无法存储数据。也就是说发送端和接收端是同步运行的。

```go
pipline := make(chan int)

// 或者
pipline := make(chan int, 0)
```

### 双向信道与单向信道

通常情况下，我们定义的信道都是双向通道，可发送数据，也可以接收数据。

但有时候，我们希望对信道的数据流向做一些控制，比如这个信道只能接收数据或者这个信道只能发送数据。

因此，就有了 双向信道 和 单向信道 两种分类。

- 双向信道

默认情况下你定义的信道都是双向的，比如下面代码

```go
import (
    "fmt"
    "time"
)

func main() {
    pipline := make(chan int)

    go func() {
        fmt.Println("准备发送数据: 100")
        pipline <- 100
    }()

    go func() {
        num := <-pipline
        fmt.Printf("接收到的数据是: %d", num)
    }()
    // 主函数sleep，使得上面两个goroutine有机会执行
    time.Sleep(1)
}
```

- 单向信道

单向信道，可以细分为 只读信道 和 只写信道。

定义只读信道

```go
var pipline = make(chan int)
type Receiver = <-chan int // 关键代码：定义别名类型
var receiver Receiver = pipline
```

定义只写信道

```go
var pipline = make(chan int)
type Sender = chan<- int  // 关键代码：定义别名类型
var sender Sender = pipline
```

仔细观察，区别在于 `<-` 符号在关键字 `chan` 的左边还是右边。

`<-chan` 表示这个信道，只能从里发出数据，对于程序来说就是只读

`chan<-` 表示这个信道，只能从外面接收数据，对于程序来说就是只写

有同学可能会问：为什么还要先声明一个双向信道，再定义单向通道呢？比如这样写

```go
type Sender = chan<- int
sender := make(Sender)
```

代码是没问题，但是你要明白信道的意义是什么？

信道本身就是为了传输数据而存在的，如果只有接收者或者只有发送者，那信道就变成了只入不出或者只出不入了吗，没什么用。所以只读信道和只写信道，唇亡齿寒，缺一不可。

当然了，若你往一个只读信道中写入数据，或者从一个只写信道中读取数据，是必然都会出错的，不多说了。

完整的示例代码如下，供你参考：

```go
import (
    "fmt"
    "time"
)
 //定义只写信道类型
type Sender = chan<- int

//定义只读信道类型
type Receiver = <-chan int

func main() {
    var pipline = make(chan int)

    go func() {
        var sender Sender = pipline
        fmt.Println("准备发送数据: 100")
        sender <- 100
    }()

    go func() {
        var receiver Receiver = pipline
        num := <-receiver
        fmt.Printf("接收到的数据是: %d", num)
    }()
    // 主函数sleep，使得上面两个goroutine有机会执行
    time.Sleep(1)
}
```

### 遍历信道

遍历信道，可以使用 `for` 搭配 `range` 关键字，在 `range` 时，要确保信道是处于关闭状态，否则循环会阻塞。

```go
import "fmt"

func fibonacci(mychan chan int) {
    n := cap(mychan)
    x, y := 1, 1
    for i := 0; i < n; i++ {
        mychan <- x
        x, y = y, x+y
    }
    // 记得 close 信道
    // 不然主函数中遍历完并不会结束，而是会阻塞。
    close(mychan)
}

func main() {
    pipline := make(chan int, 10)

    go fibonacci(pipline)

    for k := range pipline {
        fmt.Println(k)
    }
}
```

### 用信道来做锁

当信道里的数据量已经达到设定的容量时，此时再往里发送数据会阻塞整个程序。

利用这个特性，可以用当他来当程序的锁。

示例如下，详情可以看注释

```go
package main

import {
    "fmt"
    "time"
}

// 由于 x=x+1 不是原子操作
// 所以应避免多个协程对x进行操作
// 使用容量为1的信道可以达到锁的效果
func increment(ch chan bool, x *int) {
    ch <- true
    *x = *x + 1
    <- ch
}

func main() {
    // 注意要设置容量为 1 的缓冲信道
    pipline := make(chan bool, 1)

    var x int
    for i := 0; i < 1000; i++ {
        go increment(pipline, &x)
    }

    // 确保所有的协程都已完成
    // 以后会介绍一种更合适的方法（Mutex），这里暂时使用sleep
    time.Sleep(3)
    fmt.Println("x 的值：", x)
}

// x 的值：1000
```

如果不加锁，输出会小于 1000。

## 几个信道死锁经典错误案例详解

刚接触 `Go` 语言的信道的时候，经常会遇到死锁的错误，而导致这个错误的原因有很多种，这里整理了几种我初学时见到的。

```bash
fatal error: all goroutines are asleep - deadlock!
```

### 错误示例一

看下面这段代码

```go
package main

import "fmt"

func main() {
    pipline := make(chan string)
    pipline <- "hello world"
    fmt.Println(<-pipline)
}
```

运行会抛出错误，如下

```bash
fatal error: all goroutines are asleep - deadlock!
```

看起来好像没有什么问题？先往信道中存入数据，再从信道中读取数据。

回顾前面的基础，我们知道使用 `make` 创建信道的时候，若不传递第二个参数，则你定义的是无缓冲信道，而对于无缓冲信道，在接收者未准备好之前，发送操作是阻塞的.

因此，对于解决此问题有两种方法：

- 使接收者代码在发送者之前执行

- 使用缓冲信道，而不使用无缓冲信道

第一种方法：

若要程序正常执行，需要保证接收者程序在发送数据到信道前就进行阻塞状态，修改代码如下

```go
package main

import "fmt"

func main() {
    pipline := make(chan string)
    fmt.Println(<-pipline)
    pipline <- "hello world"
}
```

运行的时候还是报同样的错误。问题出在哪里呢？

原来我们将发送者和接收者写在了同一协程中，虽然保证了接收者代码在发送者之前执行，但是由于前面接收者一直在等待数据 而处于阻塞状态，所以无法执行到后面的发送数据。还是一样造成了死锁。

有了前面的经验，我们将接收者代码写在另一个协程里，并保证在发送者之前执行，就像这样的代码

```go
package main

func hello(pipline chan string)  {
    <-pipline
}

func main()  {
    pipline := make(chan string)
    go hello(pipline)
    pipline <- "hello world"
}
```

运行之后 ，一切正常。

第二种方法：

接收者代码必须在发送者代码之前 执行，这是针对无缓冲信道才有的约束。

既然这样，我们改使用可缓冲信道不就 OK 了吗？

```go
package main

import "fmt"

func main() {
    pipline := make(chan string, 1)
    pipline <- "hello world"
    fmt.Println(<-pipline)
}
```

运行之后，一切正常。

### 错误示例二

每个缓冲信道，都有容量，当信道里的数据量等于信道的容量后，此时再往信道里发送数据，就失造成阻塞，必须等到有人从信道中消费数据后，程序才会往下进行。

比如这段代码，信道容量为 1，但是往信道中写入两条数据，对于一个协程来说就会造成死锁。

```go
package main

import "fmt"

func main() {
    ch1 := make(chan string, 1)

    ch1 <- "hello world"
    ch1 <- "hello China"

    fmt.Println(<-ch1)
}
```

### 错误示例三

当程序一直在等待从信道里读取数据，而此时并没有人会往信道中写入数据。此时程序就会陷入死循环，造成死锁。

比如这段代码，`for` 循环接收了两次消息（"hello world"和“hello China”）后，再也没有人发送数据了，接收者就会处于一个等待永远接收不到数据的囧境。陷入死循环，造成死锁。

```go
package main

import "fmt"

func main() {
    pipline := make(chan string)
    go func() {
        pipline <- "hello world"
        pipline <- "hello China"
    }()
    for data := range pipline{
        fmt.Println(data)
    }
}
```

包子铺里的包子已经卖完了，可还有人在排队等着买，如果不再做包子，就要告诉排队的人：不用等了，今天的包子已经卖完了，明日请早呀。

不能让人家死等呀，不跟客人说明一下，人家还以为你们店后面还在蒸包子呢。

所以这个问题，解决方法很简单，只要在发送完数据后，手动关闭信道，告诉 `range` 信道已经关闭，无需等待就行。

```go
package main

import "fmt"

func main() {
    pipline := make(chan string)
    go func() {
        pipline <- "hello world"
        pipline <- "hello China"
        close(pipline)
    }()
    for data := range pipline{
        fmt.Println(data)
    }
}
```

## Go 协程：WaitGroup

在前几篇文章里，我们学习了协程和信道的内容，里面有很多例子，当时为了保证 `main goroutine` 在所有的 `goroutine` 都执行完毕后再退出，我使用了 `time.Sleep` 这种方式。

由于写的 demo 都是比较简单的， sleep 个 1 秒，我们主观上认为是够用的。

但在实际开发中，开发人员是无法预知，所有的 `goroutine` 需要多长的时间才能执行完毕，`sleep` 多了吧主程序就阻塞了， `sleep` 少了吧有的子协程的任务就没法完成。

因此，使用 `time.Sleep` 是一种极不推荐的方式，今天主要就要来介绍一下如何优雅的处理这种情况。

### 使用信道来标记完成

“不要通过共享内存来通信，要通过通信来共享内存”

学习了信道后，我们知道，信道可以实现多个协程间的通信，那么我们只要定义一个信道，在任务完成后，往信道中写入 `true`，然后在主协程中获取到 `true`，就认为子协程已经执行完毕。

```go
import "fmt"

func main() {
    done := make(chan bool)
    go func() {
        for i := 0; i < 5; i++ {
            fmt.Println(i)
        }
        done <- true
    }()
    <-done
}

// 输出如下

// 0
// 1
// 2
// 3
// 4
```

### 使用 WaitGroup

上面使用信道的方法，在单个协程或者协程数少的时候，并不会有什么问题，但在协程数多的时候，代码就会显得非常复杂，有兴趣可以自己尝试一下。

那么有没有一种更加优雅的方式呢？

有，这就要说到 `sync` 包 提供的 `WaitGroup` 类型。

`WaitGroup` 你只要实例化了就能使用

```go
var 实例名 sync.WaitGroup
```

实例化完成后，就可以使用它的几个方法：

- `Add` ：初始值为 0，你传入的值会往计数器上加，这里直接传入你子协程的数量

- `Done` ：当某个子协程完成后，可调用此方法，会从计数器上减一，通常可以使用 `defer` 来调用。

- `Wait` ：阻塞当前协程，直到实例里的计数器归零。

举一个例子：

```go
import (
    "fmt"
    "sync"
)

func worker(x int, wg *sync.WaitGroup) {
    defer wg.Done()
    for i := 0; i < 5; i++ {
        fmt.Printf("worker %d: %d\n", x, i)
    }
}

func main() {
    var wg sync.WaitGroup

    wg.Add(2)
    go worker(1, &wg)
    go worker(2, &wg)

    wg.Wait()
}

// 输出如下

// worker 2: 0
// worker 2: 1
// worker 2: 2
// worker 2: 3
// worker 2: 4
// worker 1: 0
// worker 1: 1
// worker 1: 2
// worker 1: 3
// worker 1: 4
```

以上就是我们在 `Go` 语言中实现一主多子的协程协作方式，推荐使用 `sync.WaitGroup`。

## Go协程：互斥锁和读写锁

在前面的章节中我们介绍了信道的一些用法，要知道的是在 `Go` 语言中，信道的地位非常高，它是 `first class` 级别的，面对并发问题，我们始终应该优先考虑使用信道，如果通过信道解决不了的，不得不使用共享内存来实现并发编程的，那 `Golang` 中的锁机制，就是你绕不过的知识点了。

今天就来讲一讲 `Golang` 中的锁机制。

在 `Golang` 里有专门的方法来实现锁，还是上一节里介绍的 `sync` 包。

这个包有两个很重要的锁类型

- 一个叫 `Mutex`， 利用它可以实现互斥锁。
- 一个叫 `RWMutex`，利用它可以实现读写锁。

### 互斥锁 ：Mutex

使用互斥锁（`Mutex`，全称 `mutual exclusion`）是为了来保护一个资源不会因为并发操作而引起冲突导致数据不准确。

举个例子，就像下面这段代码，我开启了三个协程，每个协程分别往 `count` 这个变量加1000次 1，理论上看，最终的 count 值应试为 3000

```go
package main

import (
    "fmt"
    "sync"
)

func add(count *int, wg *sync.WaitGroup) {
    for i := 0; i < 1000; i++ {
        *count = *count + 1
    }
    wg.Done()
}

func main() {
    var wg sync.WaitGroup
    count := 0
    wg.Add(3)
    go add(&count, &wg)
    go add(&count, &wg)
    go add(&count, &wg)

    wg.Wait()
    fmt.Println("count 的值为：", count)
}
```

可运行多次的结果，都不相同

```go
// 第一次
count 的值为： 2854

// 第二次
count 的值为： 2673

// 第三次
count 的值为： 2840
```

原因就在于这三个协程在执行时，先读取 `count` 再更新 `count` 的值，而这个过程并不具备原子性，所以导致了数据的不准确。

解决这个问题的方法，就是给 `add` 这个函数加上 `Mutex` 互斥锁，要求同一时刻，仅能有一个协程能对 `count` 操作。

在写代码前，先了解一下 `Mutex` 锁的两种定义方法

```go
// 第一种
var lock *sync.Mutex
lock = new(sync.Mutex)

// 第二种
lock := &sync.Mutex{}
```

然后就可以修改你上面的代码，如下所示

```go
import (
    "fmt"
    "sync"
)

func add(count *int, wg *sync.WaitGroup, lock *sync.Mutex) {
    for i := 0; i < 1000; i++ {
        lock.Lock()
        *count = *count + 1
        lock.Unlock()
    }
    wg.Done()
}

func main() {
    var wg sync.WaitGroup
    lock := &sync.Mutex{}
    count := 0
    wg.Add(3)
    go add(&count, &wg, lock)
    go add(&count, &wg, lock)
    go add(&count, &wg, lock)

    wg.Wait()
    fmt.Println("count 的值为：", count)
}
```

此时，不管你执行多少次，输出都只有一个结果

```go
count 的值为： 3000
```

使用 `Mutext` 锁虽然很简单，但仍然有几点需要注意：

- 同一协程里，不要在尚未解锁时再次使加锁

- 同一协程里，不要对已解锁的锁再次解锁

加了锁后，别忘了解锁，必要时使用 `defer` 语句

### 读写锁：RWMutex

`Mutex` 是最简单的一种锁类型，他提供了一个傻瓜式的操作，加锁解锁加锁解锁，让你不需要再考虑其他的。

简单同时意味着在某些特殊情况下有可能会造成时间上的浪费，导致程序性能低下。

举个例子，我们平时去图书馆，要嘛是去借书，要嘛去还书，借书的流程繁锁，没有办卡的还要让管理员给你办卡，因此借书通常都要排老长的队，假设图书馆里只有一个管理员，按照 `Mutex`（互斥锁）的思想， 这个管理员同一时刻只能服务一个人，这就意味着，还书的也要跟借书的一起排队。

可还书的步骤非常简单，可能就把书给管理员扫下码就可以走了。

如果让还书的人，跟借书的人一起排队，那估计有很多人都不乐意了。

因此，图书馆为了提高整个流程的效率，就允许还书的人，不需要排队，可以直接自助还书。

图书管将馆里的人分得更细了，对于读者的不同需求提供了不同的方案。提高了效率。

`RWMutex`，也是如此，它将程序对资源的访问分为读操作和写操作

为了保证数据的安全，它规定了当有人还在读取数据（即读锁占用）时，不允计有人更新这个数据（即写锁会阻塞）

为了保证程序的效率，多个人（线程）读取数据（拥有读锁）时，互不影响不会造成阻塞，它不会像 `Mutex` 那样只允许有一个人（线程）读取同一个数据。

理解了这个后，再来看看，如何使用 `RWMutex`？

定义一个 `RWMuteux` 锁，同样有两种方法

```go
// 第一种
var lock *sync.RWMutex
lock = new(sync.RWMutex)

// 第二种
lock := &sync.RWMutex{}
```

`RWMutex` 里提供了两种锁，每种锁分别对应两个方法，为了避免死锁，两个方法应成对出现，必要时请使用 `defer`。

- 读锁：调用 `RLock` 方法开启锁，调用 `RUnlock` 释放锁

- 写锁：调用 `Lock` 方法开启锁，调用 `Unlock` 释放锁（和 `Mutex`类似）

接下来，直接看一下例子吧

```go
package main

import (
    "fmt"
    "sync"
    "time"
)

func main() {
    lock := &sync.RWMutex{}
    lock.Lock()

    for i := 0; i < 4; i++ {
        go func(i int) {
            fmt.Printf("第 %d 个协程准备开始... \n", i)
            lock.RLock()
            fmt.Printf("第 %d 个协程获得读锁, sleep 1s 后，释放锁\n", i)
            time.Sleep(time.Second)
            lock.RUnlock()
        }(i)
    }

    time.Sleep(time.Second * 2)

    fmt.Println("准备释放写锁，读锁不再阻塞")
    // 写锁一释放，读锁就自由了
    lock.Unlock()

    // 由于会等到读锁全部释放，才能获得写锁
    // 因为这里一定会在上面 4 个协程全部完成才能往下走
    lock.Lock()
    fmt.Println("程序退出...")
    lock.Unlock()
}

// 输出如下
// 
// 第 1 个协程准备开始... 
// 第 0 个协程准备开始... 
// 第 3 个协程准备开始... 
// 第 2 个协程准备开始... 
// 准备释放写锁，读锁不再阻塞
// 第 2 个协程获得读锁, sleep 1s 后，释放锁
// 第 3 个协程获得读锁, sleep 1s 后，释放锁
// 第 1 个协程获得读锁, sleep 1s 后，释放锁
// 第 0 个协程获得读锁, sleep 1s 后，释放锁
// 程序退出...
```

## Go里的异常处理：panic 和 recover

编程语言一般都会有异常捕获机制，在 `Python` 中 是使用 `raise` 和 `try-except` 语句来实现的异常抛出和异常捕获的。

在 `Golang` 中，有不少常规错误，在编译阶段就能提前告警，比如语法错误或类型错误等，但是有些错误仅能在程序运行后才能发生，比如数组访问越界、空指针引用等，这些运行时错误会引起程序退出。

当然能触发程序宕机退出的，也可以是我们自己，比如经过检查判断，当前环境无法达到我们程序进行的预期条件时（比如一个服务指定监听端口被其他程序占用），可以手动触发 `panic`，让程序退出停止运行。

### 触发panic

手动触发宕机，是非常简单的一件事，只需要调用 `panic` 这个内置函数即可，就像这样子

```go
package main

func main() {
    panic("crash")
}
```

运行后，直接报错宕机

```bash
$ go run main.go
go run main.go
panic: crash

goroutine 1 [running]:
main.main()
        E:/Go-Code/main.go:4 +0x40
exit status 2
```

### 捕获 panic

发生了异常，有时候就得捕获，就像 `Python` 中的 `except` 一样，那 `Golang` 中是如何做到的呢？

这就不得不引出另外一个内建函数 -- `recover`，它可以让程序在发生宕机后起生回生。

但是 `recover` 的使用，有一个条件，就是它必须在 `defer` 函数中才能生效，其他作用域下，它是不工作的。

这是一个简单的例子

```go
import "fmt"

func set_data(x int) {
    defer func() {
        // recover() 可以将捕获到的panic信息打印
        if err := recover(); err != nil {
            fmt.Println(err)
        }
    }()

    // 故意制造数组越界，触发 panic
    var arr [10]int
    arr[x] = 88
}

func main() {
    set_data(20)

    // 如果能执行到这句，说明panic被捕获了
    // 后续的程序能继续运行
    fmt.Println("everything is ok")
}
```

运行后，输出如下

```bash
$ go run main.go
runtime error: index out of range [20] with length 10
everything is ok
```

通常来说，不应该对进入 `panic` 宕机的程序做任何处理，但有时，需要我们可以从宕机中恢复，至少我们可以在程序崩溃前，做一些操作，举个例子，当 `web` 服务器遇到不可预料的严重问题时，在崩溃前应该将所有的连接关闭，如果不做任何处理，会使得客户端一直处于等待状态，如果 `web` 服务器还在开发阶段，服务器甚至可以将异常信息反馈到客户端，帮助调试。

### 无法跨协程

从上面的例子，可以看到，即使 `panic` 会导致整个程序退出，但在退出前，若有 `defer` 延迟函数，还是得执行完 `defer` 。

但是这个 `defer` 在多个协程之间是没有效果，在子协程里触发 `panic`，只能触发自己协程内的 `defer`，而不能调用 `main` 协程里的 `defer` 函数的。

来做个实验就知道了

```go
import (
    "fmt"
    "time"
)

func main() {
    // 这个 defer 并不会执行
    defer fmt.Println("in main")

    go func() {
        defer println("in goroutine")
        panic("")
    }()

    time.Sleep(2 * time.Second)
}
```

输出如下

```bash
in goroutine
panic:

goroutine 6 [running]:
main.main.func1()
        E:/Go-Code/main.go:12 +0x7b
created by main.main
        E:/Go-Code/main.go:10 +0xbc
exit status 2
```

### 总结

`Golang` 异常的抛出与捕获，依赖两个内置函数：

- `panic` ：抛出异常，使程序崩溃

- `recover`：捕获异常，恢复程序或做收尾工作

`revocer` 调用后，抛出的 `panic` 将会在此处终结，不会再外抛，但是 `recover`，并不能任意使用，它有强制要求，必须得在 `defer` 下才能发挥用途。