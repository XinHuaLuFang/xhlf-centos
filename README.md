# xhlf-centos

## 目录
* [mysql](#mysql)
* [命令](#命令)

## mysql
> 检测是否已安装`mysql`

```Bash
  rpm -qa | grep mysql
```
> 卸载

```Bash
  rpm -e mysql            // 普通删除
  repm -e --nodeps mysql  // 强力删除，若普通删除提示有依赖文件，则用此命令
```

> 安装

```Bash
  yum install mysql         // 客户端
  yum install mysql-server  // 服务器
  yum install mysql-devel   // 库
```

> 验证

```Bash
  mysqladmin --version
```

> 启动

```Bash
  service mysqld start // 第一次启动mysql时，会显示一些初始化信息
```

> 关闭

```Bash
  service mysqld stop
```

> 重启

```Bash
  service mysqld restart
```

> 是否开机自启

```Bash
 chkconfig --list | grep mysqld
```

> 设置开机自启

```Bash
  chkconfig mysqld on
```

> 关闭开机自启

```Bash
  chkconfig mysqld off
```

> 设置root的密码

```Bash
  mysqladmin -u root password 'root' // mysql初始化后root无密码
```

> root登录mysql

```Bash
  mysql -u root -p  // 然后输入密码登录
```

## 命令
- [GREP](http://man.linuxde.net/GREP) - __Global Regular Expression Print__ - global search regular expression and print out the line
- [RPM](http://man.linuxde.net/RPM) - __Red Hat Package Manager__