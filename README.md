# Vlc-sdk-lib
vlc-android-lib 2.0.0
 首先说明 下  我在github上找 vlc-android的代码几 乎所有源码都是3年前或者两年前的 库文件
 
此次版本对最新版的 vlc-android的代码在linux  ubuntu64  16.4  中搭建编绎环境
android-sdk 版本 api24    ndk版本 r12    java 版本 8   vlc-android 版本 2.0.0版本


1 我在win10中安装的  VMware Workstation Pro  可以自已百度下载
安装ubuntu 64  16 的最新版
![](https://github.com/mengzhidaren/Vlc-sdk-lib/screenshots/1.png)
2安装  linux 版的  jdk   sdk 最新版就行

3  ubuntu 64 环境设置

全局用户环境设置

sudo gedit /etc/profile
$source /etc/profile

export NDK=/opt/sdk/android-sdk-linux/ndk-bundle
export ANDROID_NDK=/opt/sdk/android-sdk-linux/ndk-bundle
export PATH=${ANDROID_NDK}:$PATH
export ANDROID_SDK=/opt/sdk/android-sdk-linux
export PATH=$ANDROID_SDK/tools:$ANDROID_SDK/platform-tools:$PATH

export JAVA_HOME=/opt/sdk/jdk1.8.0_101
export JRE_HOME=${JAVA_HOME}/jre
export CLASSPATH=.:${JAVA_HOME}/lib:${JRE_HOME}/lib:${JAVA_HOME}/lib/tools.jar
export PATH=${JAVA_HOME}/bin:$PATH

export ANDROID_ABI=armeabi-v7a   //对应的cpu平台 .so包



5安装工具  https://wiki.videolan.org/AndroidCompile/
  sudo apt-get install automake ant autopoint cmake build-essential libtool \
     patch pkg-config protobuf-compiler ragel subversion unzip git
还是最新版就行


6 编译文件 （可能会出现各种问题  一个一个google解吧）

MAC电脑没试过 会简单一点


可以用我编译好的

发现bug或有好的建议欢迎[issue]

我后期会时间会优化下库大小  和其它bug

目前已知bug：  还没有   就是库文件有点大

compile 'com.yyl.vlc:vlc-android-sdk:1.0.1'