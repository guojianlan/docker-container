# 基础配置
```yml
- MYSQL_LOG_CONSOLE=true
- MYSQL_ROOT_HOST=%
MYSQL_ROOT_HOST新增一个host
```
## 5.6操作步骤
-------
```txt
创建数据库，并且在里面获取随机密码，第一次登陆需要修改密码
docker-compose exec mysql mysql -uroot -p
设置密码
set password = password('mypassword')

设置外网访问
GRANT ALL PRIVILEGES ON *.* TO 'root'@'%' IDENTIFIED BY 'mypassword' WITH GRANT OPTION;
flush privileges;
```
-------
