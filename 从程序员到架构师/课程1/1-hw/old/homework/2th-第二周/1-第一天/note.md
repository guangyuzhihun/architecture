# 第一天课程

> 第二周课程说明
```

```

## 1 周末回顾

> 公司拓扑作业
```
员工增长量 - 倍增 - 算出最大人数 - 算出多少个IP地址 - 算出主机数量 - 算出子网掩码
```

> 推荐书籍 Java TCP/IP Socket 编程

> gulp插件
```
bower 浏览器测试插件
```


## 2 vert.x

> 说明
```
eclipse基金会支持
非J2EE体系
vert.x3 支持 JDK8
强交互应用 => 可支撑上百万用户并发

核心：
分布式部署的，
异步编程的，
事件总线
```

> 部署
```
每台机器安装vert.x
```

> gradle
```
初始化：
mkdir testjava
gradle init

核心文件：
build.gradle

仓库选择：
maven
jcenter // 更新频率更高
```

> build.gradle
```
buildscript 构建时的依赖
```

> maven仓库
```
https://mvnrepository.com/
```

> gradlew 和 gradlew.bat
```
相关网址
https://www.zhihu.com/question/30432152

运行构建任务 - 指定版本及配套环境 - 可以用于测试服务器构建
```

> vertx-gradle-starter
```
git clone https://github.com/vert-x3/vertx-gradle-starter.git
```

> kotlin


## 3 安装mac开发环境

> 下载 intellij IDE
```
官网：
intellij

```

> 配置 本用户的Java 环境 (之前需要安装java)
```
vim ~/.bash_profile

###
// 这个是mac生成的软连接,配置真实路径也可
JAVA_HOME=/usr/libexec/java_home
CLASSPAHT=.:$JAVA_HOME/lib/dt.jar:$JAVA_HOME/lib/tools.jar
###

source ~/.bash_profile

// 查询成功没
zain-MAC:docker zain$ $JAVA_HOME
/Library/Java/JavaVirtualMachines/jdk/Contents/Home
```

> 在 intellij 中新建 gradle 工程
```
Creat New Project
选择 Gradle, lib按需勾选 java/kotlin
填写组织/机构/版本
Gradle 用默认配置就行，若出现 java_home not defiend 按上面的配置下java_home
选择项目名和位置

如果遇到了卡住的诡异问题，关闭IDE，重启电脑
```

> 参考网址
```
intellij:
https://www.jetbrains.com/help/idea/getting-started-with-gradle.html
kotlin on intellij
http://kotlinlang.org/docs/tutorials/getting-started.html
```

> mac运行java时异常
```
Class JavaLaunchHelper is implemented in both /Library/Java/JavaVirtualMachines/jdk1.8.0_121.jdk/Contents/Home/bin/java (0x10d19c4c0) and /Library/Java/JavaVirtualMachines/jdk1.8.0_121.jdk/Contents/Home/jre/lib/libinstrument.dylib (0x10ea194e0). One of the two will be used. Which one is undefined.

java的一个bug，升级到1.8.152以上就好
参考：
http://stackoverflow.com/questions/43003012/objc3648-class-javalaunchhelper-is-implemented-in-both

点击IJ最上面菜单的Help-Edit Custom Properties，没有这个properties文件的话，IJ会提示创建，然后在里面加上
idea.no.launcher=true

之后重启IDE
```

## 4 运行程序

> 等自动build完成功之后，会生成类似如下目录
```
zain/ 项目名
|_ .gradle/
|_ .idea
|_ build
|_ gradle
|_ out
...

如果只有.idea说明build失败了，如果卡了建议重启电脑
```

> 建立代码目录
```
zain/
|_ src/
|  |_ main/
|  |  |_ java/
|  |  |_ kotlin/
|  |  |_ groovy/
|  |_ test/
|
...
```

> 运行java
```
正常写main函数，run它就好了
```

> 运行kotlin
```
建立一个 Main.kt 文件

fun main (args: Array<String>) {
    println("Hello Kotlin")
}

之后右键，run当前文件
```


## 运行 vertx-examples-kotlin

> 网址
```
https://github.com/guangyuzhihun/vertx-examples/tree/master/kotlin-example

git clone https://github.com/guangyuzhihun/vertx-examples.git
```

> 运行该项目
```
用IJ打开其中的kotlin部分
打开任务工具 View -> Tool Windows -> Gradle

等待构建完成后，双击
Tasks -> application -> runShadow

打开网页：
http://localhost:8080/

注：有时候该重启IJ就重启，便于加载插件
```

