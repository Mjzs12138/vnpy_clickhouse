# VeighNa框架的ClickHouse数据库接口

<p align="center">
  <img src ="https://vnpy.oss-cn-shanghai.aliyuncs.com/vnpy-logo.png"/>
</p>

<p align="center">
    <img src ="https://img.shields.io/badge/version-1.0.0-blueviolet.svg"/>
    <img src ="https://img.shields.io/badge/platform-windows|linux|macos-yellow.svg"/>
    <img src ="https://img.shields.io/badge/python-3.10|3.11|3.12-blue.svg" />
</p>

## 说明

ClickHouse数据库接口。

明镜止水的修改：将版本号改为1.0.1，并且将`clickhouse_database`中的数据表名称改为和vnpy的一致。

## 使用

### 全局配置

在VeighNa中使用ClickHouse时，需要在全局配置中填写以下字段信息：

|名称|含义|必填|举例|
|---------|----|---|---|
|database.name|名称|是|clickhouse|
|database.host|地址|是|localhost|
|database.port|端口|是|9000|
|database.database|实例|是|vnpy|
|database.user|用户名|是|clickhouse|
|database.password|密码|是|123456|

请注意，VeighNa不会主动为关系型数据库创建数据库，所以请确保你所填的database.database字段对应的数据库已经创建好了。若未创建数据库，请手动连上数据库并创建。

### 创建实例

VeighNa不会主动为ClickHouse数据库创建实例，所以使用前请确保database.database字段中填写的的数据库实例已经创建了。

若实例尚未创建，可以使用 clickhouse-client客户端的【Create Database】进行操作。
