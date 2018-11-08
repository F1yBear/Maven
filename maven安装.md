# maven的安装步骤
## 1. 前提条件
* [maven 官网](http://maven.apache.org/index.html) 下载maven
* 检查系统是否已安装,支持maven的jdk
```
java -version
```
## 2. windows 安装
* 下载一个的maven安装包
* 解压到存放路径,我默认是 D:/apache-maven-3.6.0
* 创建一个maven的本地仓库,因为C盘磁盘缘故,我默认是D:/repo
* 修改D:/apache-maven-3.6.0/conf/settings.xml文件
```
  <!-- 修改默认仓库-->
  <localRepository>D:/repo</localRepository>
  
  <!-- 设置一个访问网速较快的默认仓库-->
  <mirrors>   
    <mirror>
      <id>aliyun</id>
      <name>aliyun</name>
      <url>http://maven.aliyun.com/nexus/content/groups/public</url>
    </mirror>
  </mirrors>
```
* 配置环境变量
```
M2_HOME = D:/apache-maven-3.6.0
path = %M2_HOME%/bin

# 设置maven内存,编码
MAVEN_OPTS = -Xms256m -Xmx512m -Dfile.encoding=UTF-8
```
* 测试是否安装成功
```
mvn -v
```
