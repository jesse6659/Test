实验1：Android开发基础 - 创建第一个Android应用
实验信息
课程名称：移动应用开发

实验编号：实验1

实验名称：Android开发环境搭建与第一个应用创建

学号：121052023049

姓名：戴颖杰

实验日期：2025.10.7

实验目标
掌握Android Studio开发环境的安装与配置

学习创建第一个Android项目

了解Android项目的基本结构

掌握在模拟器或真机上运行应用的方法

学习将项目同步到GitHub/Gitee

实验环境
环境组件	版本信息
操作系统	Windows 11
Android Studio	Narwhal 3 (2025.1.3)
JDK	1.8+
Gradle
Git	2.40+
实验步骤
步骤1：安装Android Studio
下载Android Studio

访问Android Developer官网

下载最新版本的Android Studio

安装过程

bash
# 安装注意事项：
# - 选择适合的安装路径
# - 安装Android SDK
# - 配置环境变量（如果需要）
首次运行配置

选择安装类型：Standard（标准安装）

下载必要的SDK组件

等待初始配置完成

步骤2：创建第一个Android项目
新建项目

打开Android Studio

选择"New Project"

选择模板："Empty Views Activity"

配置项目信息：

java
// 项目配置参数
名称：MyFirstApp
包名：com.example.myfirstapp
语言：Java
最低SDK：API 21 (Android 5.0)
项目结构说明

text
MyFirstApp/
├── app/
│   ├── src/main/
│   │   ├── java/com/example/myfirstapp/
│   │   │   └── MainActivity.java
│   │   ├── res/
│   │   │   ├── layout/
│   │   │   │   └── activity_main.xml
│   │   │   └── values/
│   │   │       └── strings.xml
│   │   └── AndroidManifest.xml
│   └── build.gradle
├── gradle/
└── build.gradle
步骤3：理解项目文件
MainActivity.java

java
package com.example.myfirstapp;

import androidx.appcompat.app.AppCompatActivity;
import android.os.Bundle;

public class MainActivity extends AppCompatActivity {
    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main); // 设置布局文件
    }
}
activity_main.xml（布局文件）

xml
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout
    xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    android:layout_width="match_parent"
    android:layout_height="match_parent">

    <TextView
        android:id="@+id/textView"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Hello World!"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent" />

</androidx.constraintlayout.widget.ConstraintLayout>
步骤4：配置运行环境
创建虚拟设备

打开AVD Manager

选择设备类型（Pixel 4）

选择系统镜像（API 36.0）

完成虚拟设备创建

运行应用

点击运行按钮（▶️）

选择目标设备（模拟器或真机）

等待应用安装和启动

步骤5：版本控制与代码托管
安装Git

访问Git官网下载安装

配置全局用户信息：

bash
git config --global user.name "jesse6659"
git config --global user.email "3060848556@qq.com"
创建GitHub仓库

登录GitHub

创建新仓库：MyFirstApp

复制仓库地址

同步项目到GitHub

bash
# 在项目根目录执行以下命令
git init
git add .
git commit -m "初始提交：完成实验1 - 第一个Android应用"
git branch -M main
git remote add origin https://github.com/你的用户名/MyFirstApp.git
git push -u origin main
实验结果
成功运行截图


应用运行效果：

屏幕上显示"Hello World!"文本

应用图标显示在启动器中

应用能够正常启动和退出

项目结构验证
text
✅ app/src/main/java/ - MainActivity.java存在
✅ app/src/main/res/layout/ - activity_main.xml存在
✅ app/src/main/AndroidManifest.xml - 配置文件正确
✅ Gradle构建成功
✅ 应用在模拟器/真机上正常运行
遇到的问题及解决方案
问题1：Android Studio安装失败
现象：安装过程中出现错误提示
解决方案：

检查系统是否满足最低要求

以管理员身份运行安装程序

关闭杀毒软件后重试

问题2：模拟器启动缓慢
现象：AVD启动时间过长
解决方案：

启用VT-x/AMD-V虚拟化技术

分配更多内存给模拟器

使用x86系统镜像

问题3：Git推送失败
现象：git push命令执行失败
解决方案：

检查网络连接

验证GitHub账号权限

使用Personal Access Token进行认证

实验总结
掌握的知识点
✅ Android Studio开发环境的安装与配置

✅ Android项目创建流程

✅ 项目结构的基本理解

✅ 虚拟设备的创建与管理

✅ 应用运行与调试方法

✅ Git版本控制的基本使用

✅ GitHub代码托管操作

实验收获
通过本次实验，我成功搭建了Android开发环境，创建了第一个Android应用，并理解了Android项目的基本结构。掌握了从项目创建到代码托管的完整开发流程，为后续的Android开发学习奠定了坚实基础。

参考资料
Android Developer官方文档

课程CSDN博客 - Android Studio安装指南

Git官方文档

GitHub Guides

附录
项目地址
GitHub仓库：https://github.com/你的用户名/MyFirstApp

.gitignore文件内容
text
# Android Studio忽略文件
*.iml
.gradle
/local.properties
/.idea/caches
/.idea/libraries
/.idea/modules.xml
/.idea/workspace.xml
/.idea/navEditor.xml
/.idea/assetWizardSettings.xml
.DS_Store
/build
/captures
.externalNativeBuild
.cxx
local.properties
