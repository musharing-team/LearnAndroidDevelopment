# Java 中的类和对象

> 类可以看成是创建Java对象的模板

## 类的定义

```java
public class Dog {
    String name;
    int age;

    void eat() {
    }
    void sleep() {
    }
}
```

## 类中变量的类型

* **局部变量**：在*方法*或*语句块*中定义的变量被称为局部变量。变量声明和初始化都是在方法中，方法结束后，变量就会自动销毁。
* **成员变量**：成员变量是定义在类中，*方法体之外*的变量。这种变量在创建对象的时候实例化。成员变量可以被类中方法、构造方法和特定类的语句块访问。
* **类变量**：类变量也声明在类中，方法体之外，但必须声明为 `static` 类型。

## 构造方法

构造方法的名称必须与类同名，一个类可以有多个构造方法。

在创建一个对象的时候，至少要调用一个构造方法。
如果没有显式地为类定义构造方法，Java编译器将会为该类提供一个默认构造方法。

```java
public class Dog {
	public Dog() {
		System.out.println("构造Dog");
	}
}
```

## 创建对象

对象是根据类创建的。
创建对象需要以下三步：

* 声明：声明一个对象，包括对象名称和对象类型。
* 实例化：使用关键字 `new` 来创建一个对象。
* 初始化：使用 `new` 创建对象时，会调用构造方法初始化对象。

```java
public class Dog {
	public static void main(String[] args) {
		Dog Dog0 = new Dog();
	}
}
```

## 访问实例变量和方法

* 访问实例的变量：`实例名.变量名`
* 调用实例的方法：`实例名.方法名()`

```java
public class Dog {
	String name;
	int age;

	void eat(String food) {
		System.out.println(name + " is eating " + food + ".");
	}

	public Dog() {
		name = "Dog";
		age = 0;

		System.out.println("构造()：");
		System.out.println(name + "\t" + age);
	}
	public Dog(String dogName, int dogAge) {
		name = dogName;
		age = dogAge;
		System.out.println("构造(name, age)：");
		System.out.println(name + "\t" + age);
	}

	public static void main(String[] args) {
		Dog Dog0 = new Dog();
		Dog Dog1 = new Dog("FooBar", 3);

		// 访问变量 
		Dog0.name = "Ana";
		System.out.println(Dog0.name);

		// 访问方法
		Dog1.eat("cat");

	}
}
```

运行👆上面代码将输出：

```
构造()：
Dog	0
构造(name, age)：
FooBar	3
Ana
FooBar is eating cat.
```

