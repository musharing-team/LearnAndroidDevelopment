# Android开发概览


## Android 开发特色

### 四大组件

- 活动 Activity

	- 看得见的界面

- 服务 Servicr

	- 看不见的后台工作

	- 退出了应用后，服务还可以继续运行

- 广播接收器 Broadcast

	- 接收来自各处的广播消息，如电话、短信

	- 也可以向外发送广播

- 内容提供器 Content Provider

	- 使应用间的信息共享成为可能

### 丰富的系统控件

- 方便编写界面

### SQLite数据库

### 强大的多媒体

- 音乐

- 视频

- 拍照

- 录音

- ...

### 地理位置定位


# Android  Studio 使用


## 搭建开发环境

### JDK 8+

### Android SDK

### Android Studio

- 安卓官网下载安装 Android Studio，就可以把三项都配全了

## 第一个 Android 项目: Hello World

### 创建

- Start a new Android Studio project

- Empty Activity

- Name、储存位置(注意要建个新目录)

- 配置模拟器

	- 等编译完，点运行

	- 选择 Create Virtual Device

	- 选一个手机

	- 选一个系统，下载(翻墙)

	- 确定配置

- 点◀️运行


# Android项目目录结构


## Android 项目的目录结构（把Project结构区域从Android换成Project，可见真正的目录结构）

### .gradle 和 .idea

- 编译器自动生成的

- 不用编辑

### app

- 项目的主要代码、资源

	- build

		- 编译时生成的一些文件

	- libs

		- 在项目中使用的第三方jar包要放到这里

	- src

		- androidTest

			- 编写的测试用例

		- main

			- java

				- 用来放java代码的地方

			- res

				- 各种图片、布局、等等资源

					- drawable

						- 图片

					- mipmap

						- 图标

					- valves

						- 放字符串、样式、颜色等配置的

					- layout

						- 放布局文件的

			- AndroidManifest.xml

				- 整个Android项目的配置文件

				- 四大组件注册的地方

				- 应用程序的权限声明（没在这里注册的是不能用的）

		- proguard-rules.pro

			- 指定项目代码的混淆规则

			- 让打包之后的程序难以破解

### build

- 编译时自动生成的一些文件

### gradle

- 一些配置文件

### .gitignore

- 指定排除在git之外的文件

### build.gradle

- 项目全局的gradle构建脚本

- 通常不用编辑

### gradle.properties

- 全局的gradle配置文件

- 影响所有的gradle编译脚本

### gradlew、gradlew.bat

- 命令行执行gradle命令的脚本

- 分别对应UNIX、Windows

### HelloWorld.iml

- IntelliJ IDEA 项目的标识

- 不需要修改

### local.properties

- 指定 Android SDK 路径的

### settings.gradle

- 指定项目中所有引入的模块

- 很少修改

---

导出自 MindNode。

