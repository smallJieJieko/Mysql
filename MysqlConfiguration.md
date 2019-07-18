# Mysql
Mysql configuration and Product in use（使用经验）

### Configuration
1. 官网下载MySQL 8.0.16解压到自己的文件夹中

2. 在系统变量里面添加变量MYSQL_HOME， 变量值为安装路径 ：(自己的文件夹)...\mysql-8.0.16-winx64

3. 在path中添加 %MYSQL_HOME%\bin

4. 直接用管理员身份打开cmd，输入命令：

   ```
   mysqld --initialize --console
   ```

   ![2019052009504244](C:\Users\zhb54\Desktop\2019052009504244.png)

   注意其中黄色的是临时随机密码，可以记录下，后面需要用。

5. 初始化后进行安装，使用：

   ```
   mysqld --install /卸载服务 mysqld --remove mysql   
   ```

6. 用以下命令启动服务：

   ```
   net start mysql / 停止服务 net stop mysal
   ```

7. 启动之后需要修改为自己的密码，输入命令登陆：

   ```
   ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY '新密码';
   修改为自己的密码，这里新密码要6位以上
   ```

8. 输入 退出mysql

   ```
   quit;
   ```

9. 使用navicat链接数据库即可