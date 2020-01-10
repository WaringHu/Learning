# 1、

MySQL 不同于其他关系数据库，MySQL 本身只是一个 SQL 接口，其内部还包含多种数据引擎

使用 MySQL 时，不同的表可以使用不同的数据库引擎，使用不同的引擎并不影响 MySQL，一般总是使用 `InnoDB` 数据库引擎

# 2、安装 MySQL CE 版本

[下载链接](https://dev.mysql.com/downloads/installer/)

**大概步骤：**

- 下载 `.msi` 安装包
- 运行程序开始安装
- I agree license --> Next
- 选择 Developer Default --> Next
- 现在是检查安装条件 --> Next
- 开始安装 --> Execute
- 等待安装完成 --> Next
- Product Configuration --> Next
- High Availability 选择第一个 Sxxx MySQL Sxxx / Cxxx MySQL Rxxx --> Next
- Type and Networking --> Next
- Authentication Method 保持默认吧 --> Next
- Accounts and Roles 设置 root 密码 --> Next
- Windows Service --> Next
- Apply Configuration --> Execute --> Finish
- Product Configuration --> Next
- MySQL Router Configuration --> Finish
- Product Configuration --> Next
- Connect To Server 输入 root 密码 --> Check --> Next
- Apply Configuration --> Execute --> Finish
- Product Configuration --> Next
- Installation Complete --> Finish
- 安装完成

[参考](
https://blog.csdn.net/bobo553443/article/details/81383194)

# 3、简单测试一下

MySQL 安装在 `C:\Program Files\MySQL`

**简单介绍：**

- MySQL Server 8.0 --> bin

保存 MySQL 常用的命令行工具以及管理工具

- MySQL Server 8.0 --> data

MySQL 默认用来保存数据文件以及日志文件

- MySQL Server 8.0 --> docs

MySQL 的帮助文档

- MySQL Server 8.0 --> include

MySQL 所依赖的头文件

- MySQL Server 8.0 --> lib

MySQL 所依赖的库文件

- MySQL Server 8.0 --> share

保存目录文件以及日志文件

**注意：**

安装时，MySQL 会自动创建一个 `root` 用户并提示设置 `root` 密码

安装成功后，MySQL 会自动在后天运行，我们需要使用 MySQL 命令来连接 MySQL 服务器，打开 cmd 运行

```
mysql -u root -p
```

然后输入 `root` 密码

如果出现 cmd 报错说 xxx 不是内部指令什么的，就是没有添加环境变量

将 `C:\Program Files\MySQL\MySQL Server 8.0\bin` 添加到系统变量 path 里面

If everything is OK!

就会成功连接到服务器且 cmd 提示符变为 `mysql>`，表示我们已经进入了 MySQL 命令行，执行 `exit` or `quit` 即可退出，但是此时 MySQL 依然在后台运行
