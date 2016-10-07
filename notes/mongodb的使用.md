# mongoDB

---

### 1. 什么是mongodb？

  - MongoDB是一个基于分布式文件存储的开源数据库系统

  - MongoDB 将数据存储为一个文档，数据结构由键值(key=>value)对组成。MongoDB 文档类似于 JSON 对象。字段值可以包含其他文档，数组及文档数组。

### 2.mongodb启动与连接

#### 2.1启动

  ```
  mongod --dbpath=./data

  ```

- 如果出现`waiting for connections on port 27017` 表示启动成功。
- 可以在命令后面加上参数 `--port 27017` 来指定端口

> 注意： 这个命令窗口不能关闭，否则就停止了mongodb的服务进程

#### 2.2 客户端连接服务器

新开一个命令窗口


`mongo --host=127.0.0.1` 或者 `mongo` 按回车键

> 备注：--host后的值表示服务器的ip地址

## 数据库的操作

### 启动 Mongodb

```
mkdir -p data/db
mongod --dbpath=./data/db
```

### 开启 Mongo Shell

```
$ mongo
```

### 创建一个数据库

```
$ use digicity-express-api
```

数据库是 mongodb 中的顶级存储单位，之下一级就是 **集合** 。

### 创建一个集合

```
$ db.createCollection(‘posts’)
```

### 插入数据记录


一个集合（例如，posts ），里面可以插入多个数据记录。

```
$ db.posts.insert({title: 'myTitle', content: 'myContent'})
```

### 查看集合中的所有记录

```
$ db.posts.find()
```

### 修改一条记录（了解内容）

```
db.posts.update({_id: ObjectId('xxx')}, {$set: {title: 'mongodb'}})
```

### 删除一条记录

```
db.posts.remove({_id: ObjectId('xxx')})
```
### 删除 posts 集合中的所有记录

```
db.posts.remove({})
```

### 删除数据库

假设我们的数据库叫做 test

```
use test
db.dropDatabase()
```
