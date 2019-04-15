# Java 数组

Java 语言中提供的数组是用来存储**固定大小**的**同类型元素**的。

## 声明数组变量

欲使用数组，首先必须声明数组变量，用来存放数组对象。

```java
dataType[] arrayRefVar;   // 首选的方法
/* 或 */
dataType arrayRefVar[];  // 效果相同，但不是首选方法，这种风格来自 C/C++，只是为了让 C/C++ 程序员能够快速理解java语言
```

## 创建数组

与其他类型相似，我们可以用 `new` 创建一个数组对象。

```java
arrayRefVar = new dataType[arraySize];
```

与 C 不同的是，arraySize 可以是一个变量，而不必使用字面值常量。

或者，如果我们预先知道了数组的内容，可以像 C 一样用 数组的字面值常量 (`{...}`) 来创建一个数组：

```java
String [] names;
names = {"James", "Larry", "Tom", "Lacy"};
```

正如其他类型的变量，我们常把声明和创建写在一起：

```java
dataType[] arrayRefVar = new dataType[arraySize];
```

## 使用数组

#### 数组大小

对于一个数组 `arrayRefVar` ，我们可以使用 `arrayRefVar.length` 来获取其长度。

#### 索引访问

数组的元素是通过索引访问的。数组索引从 `0` 开始 到 `arrayRefVar.length-1`。

例如，我们用一个长度为 n 的数组来表示出 *斐波那契数列* 的前 n 项，然后把它们输出：

```java
public class FibonacciArray {
	public static void main(String[] args) {
		// 创建数组
		int size = 10;
		int[] fib = new int[10];

		// 填装数列
		fib[0] = 0;
		fib[1] = 1;
		for (int i = 2; i < size; i++) {
			fib[i] = fib[i-1] + fib[i-2];
		}

		// 输出
		for (int i = 1; i < size; i++) {
			System.out.println(fib[i]);
		}
	}
}
```

#### 数组迭代

正如上面的程序，我们常用循环来处理一个数组，我们可以使用传统的 for 或者是 for-each 循环来迭代一个数组：

```java
int arr[] = new int[5];
// for
for (int i = 0; i < arr.length; i++) {
    arr[i] = i * 2;
}
// for-each
for (int element: arr) {
    System.out.println(element);
}
```

---

相关代码:

[FibonacciArray.java](./src/FibonacciArray.java)
