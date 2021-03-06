## 循环结构

循环就是事物周而复始的变化，循环结构使得一部分代码按照次数或一定条件反复执行。

循环结构一般分为三大类：

- `for`循环
- `while`循环
- `do...while`循环

`for`循环的格式如下：

```java
for(初始化语句;判断条件语句;控制条件语句) {
	// 循环体
}
```

`while`循环语句的格式：

```java
while(判断条件语句) {
	循环体语句;
	控制条件语句;
}
```

`do...while`循环语句的格式：

```java
do {
	循环体语句;
	控制条件语句;
} while(判断条件语句);
```

**注意：** `while`小括号后的分号不可以省略，`do...while`循环至少会执行一次。

`break`表示中断语句执行，它可以直接跳出循环。
`continue`表示中断本次循环，直接进行下一次循环
