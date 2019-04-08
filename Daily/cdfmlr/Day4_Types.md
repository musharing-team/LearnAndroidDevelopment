# Java 基本数据类型

Java 的两大数据类型:

* 内置数据类型
* 引用数据类型

## 内置数据类型

对于每一种 数据类型 都有一个 **包装类**，如：`void`类型的包装类是 `java.lang.Void`。

对于数值类型的包装类，我们都可以从中获取对应类型的二进制位数、取值范围。

具体的例子，见 [`PrimitiveTypes.java`]()

### `void`

代表空的值的类型。

### 整数型

| 类型 | 说明 | 范围 | 默认值 | 备注 |
| -- | -- | -- | -- | -- |
| `byte` | 8位, 有符号, 以二进制补码表示的整数 | `-128`~`127` | `0` | 用在大型数组中节约空间 |
| `short` | 16位, 有符号, 以二进制补码表示的整数 | `-32768`~`32767` | `0` | |
| `int` | 32位, 有符号, 以二进制补码表示的整数 | `-2147483648`~`2147483647` | `0` | 一般地整型变量默认为 int 类型 |
| `long`| 64位, 有符号, 以二进制补码表示的整数 | `-2^63`~`2^63-1` | `0L` |  字面值常量是数后面加"L"("L"理论上不分大小写，但小写不易分辩，最好大写) |

整型字面值常量都可以用十(正常书写)、八(以`0`开头)、十六(以`0x`开头)进制表示：

```
int decimal = 100;
int octal = 0114;
int hexadecimal = 0x64;
```

### 浮点型

> 浮点数不能用来表示精确的值。

| 类型 | 说明 | 默认值 | 备注 |
| -- | -- | -- | -- | -- |
| `float` | 单精度、32位、符合 IEEE 754 标准的浮点数 | `0.0f` | float 在储存大型浮点数组的时候可节省内存空间 |
| `double` | 双精度、64 位、符合IEEE 754标准的浮点数 | `0.0d` | 浮点数的默认类型为double类型 |

### 字符型

| 类型 | 说明 | 范围 | 默认值 | 备注 |
| -- | -- | -- | -- | -- |
| `char` | char类型是一个单一的 16 位 Unicode 字符 | `\u0000`~`\uffff` | 字面值常量是单引号里字符(如：`'A'`) |

### 布尔型

| 类型 | 说明 | 取值 | 默认值 |
| -- | -- | -- | -- | -- |
| `boolean` | 表示一位的信息 | `true` 和 `false` | `false` |

## 引用数据类型

> 引用类型指向一个对象，指向对象的变量是引用变量。

对象、数组都是引用数据类型。

所有引用类型的默认值都是 `null`。

引用变量一旦声明后，类型就不能被改变了，但一个引用变量可以用来引用任何与之兼容的类型。

## Java 变量

声明一个变量，需要使用如下的格式的语句：

```
type varName;
```

也可以在声明的同时，对它初始化：

```
type varName = initialValue;
```

【注】初始化一个对象时，使用：`ClassName instanceName = new ClassName();`

### 常量

常量在程序运行时是不能被修改的。

#### 字面值常量

字面值常量，就是直接在程序里写一个值，比如 `100`, `-100.0`, `'A'`...
这个东西很好理解，特殊的已经在上面的内置类型表格中有说明了。

字面值常量可以赋给任何内置类型的变量。

#### 声明常量

我们也可以像声明变量一样声明一个常量。

在 Java 中，使用 `final` 关键字来修饰常量，声明方式和变量类似：

```
final double PI = 3.1415927;
```

按照惯例，常量名应该用**全部大写**的名称表示。

#### 字符串常量

和其他语言一样，Java的字符串常量也是包含在两个引号之间的字符序列，其中可以使用转义字符，也可以含有Unicode字符：

```
"Hello World"
"two\nlines"
"\"This is in quotes\""
"\u0001"
```

常用的转义字符如下：

| 				符号     | 				字符含义                 |
|------------|--------------------------|
| 				`\n`     | 				换行 (0x0a)            |
| 				`\r`     | 				回车 (0x0d)            |
| 				`\f`     | 				换页符(0x0c)            |
| 				`\b`     | 				退格 (0x08)            |
| 				`\0`     | 				空字符 (0x20)           |
| 				`\s`     | 				字符串                  |
| 				`\t`     | 				制表符                  |
| 				`\"`     | 				双引号                  |
| 				`\'`     | 				单引号                  |
| 				`\\`     | 				反斜杠                  |
| 				`\ddd`   | 				八进制字符 (ddd)          |
| 				`\uxxxx` | 				16进制Unicode字符 (xxxx) |


### 类型转换