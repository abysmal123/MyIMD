# Flutter简介
*by 马骏驰 1813015*
***
## Flutter是什么
Flutter是Google的**开源UI工具包**，可通过单个代码库为移动，网络和台式机构建**美观的**、**精致的**、**本机编译的**应用程序。  
Flutter官网：[https://flutter.dev/](https://flutter.dev/)   
Flutter 可以方便的加入现有的工程中。在全世界，Flutter 正在被越来越多的开发者和组织使用，并且 Flutter是完全免费、开源的。它也是构建未来的 Google Fuchsia 应用的主要方式。   
Flutter 组件采用现代响应式框架构建，这是从React中获得的灵感，中心思想是用组件(widget)构建你的UI。 组件描述了在给定其当前配置和状态时他们显示的样子。当组件状态改变，组件会重构它的描述(description)，Flutter 会对比之前的描述， 以确定底层渲染树从当前状态转换到下一个状态所需要的最小更改。
### Flutter发展历史
Flutter的第一个版本被称为“Sky”，运行在Android操作系统上。它是在2015年Dart开发者峰会上亮相的，其目的是能够以每秒120帧的速度持续渲染。  
#### Beta
Beta1版本于2018年2月27日在2018 世界移动大会公布。   
Beta2版本2018年3月6日发布。   
1.0版本于2018年12月5日(北京时间)发布。   
### Flutter的特点
* **快速开发**：Flutter的内置工具 __热重载(Hot Reload)__ 使得开发人员可以在极短的开发时间内将应用绘制出生机。使用一组完全可自定义的小部件，在数分钟内即可构建本机界面。
* **富有表现力且灵活的用户界面**：快速发布功能，重点放在本地最终用户体验上。分层体系结构允许完全自定义，从而实现了令人难以置信的**快速渲染**以及富有表现力和灵活的设计。
* **原生性能**：Flutter的窗口小部件包含所有关键的平台差异，例如滚动，导航，图标和字体，并且Flutter代码**使用Dart的本机编译器**编译为本机ARM机器代码。
### Flutter的使用者
许多大型公司都在使用Flutter进行智能移动开发，如：google、ebay、bmw、阿里巴巴、square等等。
## Flutter在Windows10上的使用
本段介绍Flutter在Windows10电脑系统上的开始使用的过程。
### 系统配置要求
要想安装和运行Flutter，开发环境至少应该满足如下的需求：
* **操作系统**：*Windows 7 SP1* 或更高的版本（基于 x86-64 的 64 位操作系统）。
* **磁盘空间**：除安装 IDE 和一些工具之外还应有至少 *1.32 GB* 的空间。
* **工具**：要让 Flutter 在你的开发环境中正常使用，依赖于以下的工具：
  -  **Windows PowerShell 5.0** 或者更高的版本（Windows 10 中已经预装了）
  -  **Git for Windows 2.x**，并且勾选从 Windows 命令提示符使用 Git 选项。  
  如果 Windows 版的 Git 已经安装过了，那么请确保能从命令提示符或者 PowerShell 中直接执行 git 命令。
### 获取Flutter SDK
* 安装包下载地址：[flutter_windows_2.0.1-stable.zip](https://storage.flutter-io.cn/flutter_infra/releases/stable/windows/flutter_windows_2.0.1-stable.zip)
* 将压缩包解压，然后把其中的`flutter`目录整个放在想要放置Flutter SDK的路径中（例如 `C:\src\flutter`）。
### 更新path环境变量
如果想在Windows控制台中运行Flutter命令，需要将Flutter的运行文件路径加入到PATH环境变量：
* 在开始菜单的搜索功能键入`env`，然后选择 编辑系统环境变量。
* 在`用户变量`一栏中，检查是否有`Path`这个条目：
  -  如果存在这个条目，以`;`分隔已有的内容，加入`flutter\bin`目录的完整路径。
  -  如果不存在的话，在用户环境变量中创建一个新的`Path`变量，然后将`flutter\bin`所在的完整路径作为新变量的值。
  -  重启命令行提示符窗口。
### 运行flutter doctor
打开一个新的控制台窗口，执行下面的命令： 
```
C:\src\flutter>flutter doctor
```     
上述命令会检查现有环境，并将检测结果以报告形式呈现出来。检查报告，是否有尚未安装的软件或是有其他的步骤需要完成(通常会以**粗体**呈现)。  
例如：
```
[-] Android toolchain - develop for Android devices
• Android SDK at D:\Android\sdk
✗ Android SDK is missing command line tools; download from https://goo.gl/XxQghQ
• Try re-installing or updating your Android SDK,
  visit https://flutter.cn/setup/#android-setup for detailed instructions.
```   
