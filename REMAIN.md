<blockquote>
说明：
1. 本版本是更具官方OpenTSDB2.2发布版本修改
</blockquote>

1. 安装OpenTSDB编译需要软件
```shell
yum install gnuplot automake autoconf git -y
```
备注：如果缺少automake会抛出如下异常 Can't exec "aclocal": No such file or directory at /usr/share/autoconf/Autom4te/FileUtils.pm line 326.
2. 下载指定版本的OpenTSDB源码（2.2）
3. 编译OpenTSDB
```shell
./build.sh
```
4. 移动源码
```shell
mkdir ~/opentsdb
mkdir ~/opentsdb/src/main/java/net/opentsdb
mkdir ~/opentsdb/src/test/java/net/opentsdb
cp -R ./src/* ~/opentsdb/src/main/java/net/opentsdb
cp -R ./test/* ~/opentsdb/src/test/java/net/opentsdb
cp ./build/src/BuildData.java ~/opentsdb/src/test/java/net/opentsdb
```
5. 编码POM.xml文件
```
./build.sh pom.xml #移除pom.xml中不必要的配置
```