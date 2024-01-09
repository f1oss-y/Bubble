# bubble

简易的任务清单页面

## 使用说明

### 配置MySQL

1.使用一下指令创建数据库

`CREATE DATABASE bubble DEFAULT CHARSET=utf8mb4;`

2.在`conf/config.ini`中配置数据库连接信息

### 启动

`go run main.go`

## conf

`config.ini`存储数据库信息以及启动信息
```
port = 启动端口
release = false

[mysql]
user = 数据库用户名
password = 数据库密码
host = 数据库ip
port = 数据库端口
db = 数据库名
```

## controller

`controller.go`实现基本业务

- CreateTodo 实现添加数据的功能
- GetTodoList 获取所有列表信息
- UpdateATodo 更新某一个数据
- DeleteATodo 删除某条信息

## dao

`mysql.go`数据库初始化

`github.com/jinzhu/gorm/dialects/mysql`的数据使用说明`https://github.com/go-sql-driver/mysql`

## models

`todo.go`实现模型封装

为`controller.go`中的业务实现基本功能

## routers

`routers.go`使用gin,实现前后端的交互操作

`gin`


## setting

`setting.go`配置类型


