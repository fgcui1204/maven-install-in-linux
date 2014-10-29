#Linux命令行下Maven的安装与配置


>1.先[下载](http://maven.apache.org/download.cgi) maven,请下载.tar.gz格式.

>2.在命令行中输入：
```
tar xzf apache-maven-3.2.3-bin.tar.gz -C /cuifugang/local
```
(此命令是将下载下来的tar.gz包解压到/cuifugang/local（tar默认将文件解压到当前目录，加了-C参数之后，是将解压的文件存放到/cuifugang/local中)

```
cd /cuifugang/local
```
```
ln -s apache-maven-3.2.3 maven
```

>**当然，解压完下载下来的maven包是现在还不能启用，需要在PATH里面设置一下路径，如下：**
```
sudo gedit  /etc/profile.d/maven.sh'
```
```
export MAVEN_HOME=/cuifugang/local/maven
```
```
export PATH=${MAVEN_HOME}/bin:${PATH}
```
>**设置好Maven的路径之后，需要运行下面的命令,使得上面设置的环境变量立即生效。**

```
source /etc/profile.d/maven.sh
```
>输入mvn -v  或mvn -version

>控制台显示：
```
Apache Maven 3.0.5
Maven home: /usr/share/maven
Java version: 1.8.0_25, vendor: Oracle Corporation
Java home: /usr/lib/jvm/java-8-oracle/jre
Default locale: en_US, platform encoding: UTF-8
OS name: "linux", version: "3.13.0-24-generic", arch: "amd64", family: "unix"
```
则安装配置成功！！！(*^__^*)
