title: NDK
date: 2015-05-22 17:22:04
tags:
---
#NDK安装以及环境配置
1、下载Android NDK压缩包，下载地址：[http://developer.android.com/tools/sdk/ndk/index.html]。

2、解压，将Android NDK压缩包解压到主目录/home/×××/下。
 tar jxvf android-ndk-r9d-linux-x86.tar.bz2
解压后目录结构为：/home/×××/android-ndk-r9d

3、配置PATH路径：

命令行执行
 sudo gedit /etc/profile
在文件末尾加入如下内容：
 #set NDK env
 export NDK_HOME=/home/snowdream/android-ndk-r9d
 export PATH=$NDK_HOME:$PATH
或者加入：
 export NDK_HOME=/home/skywang/workspace/ndk/r9b/android-ndk-r9b
 export PATH=$PATH:$NDK_HOME
保存文件后退出，在终端提示符中输入"source /etc/profile"使环境变量生效

4、编译sample工程：

执行命令
 cd /home/snowdream/android-ndk-r5/samples/hello-jni 
进入示例项目根目录，然后执行如下命令：
 ndk-build
您将看到系统会编译出libhello-jni.so，NDK配置成功
