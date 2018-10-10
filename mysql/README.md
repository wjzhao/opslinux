# mysql手册
- [Centos6安装mysql5.6](mysql/mysql5.6/centos6-one-install.md)
- [Centos7安装mysql5.6](mysql/mysql5.7/centos6-one-install.md)


## 一、修改密码
```
#方式一
/usr/bin/mysqladmin -u root password '123456'

#方式二
mysql> set password=password('123456');

#方式三
mysql> use mysql
mysql> GRANT ALL PRIVILEGES ON *.* TO root@"%" IDENTIFIED BY "root";
mysql> update user set Password = password('123456') where User='root';
mysql> show grants for root@"%";
mysql> flush privileges;
mysql> select Host,User,Password from user where User='root';
mysql> exit
```

## 二、查看表结构
```
mysql> desc user;

mysql> show create table user\G;

mysql> describe user;
```

## 三、插入数据
```
```