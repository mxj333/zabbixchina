### 2 服务器安装与MySQL数据库 {#server_installation_with_mysql_database}

这是很好的做法设置 _innodb\_file\_per\_table _选项 [启用](https://dev.mysql.com/doc/refman/5.6/en/tablespace-enabling.html)在MySQL。在继续之前检查此设置。

### 红帽企业Linux / CentOS {#red_hat_enterprise_linuxcentos}

#### 安装软件包 {#installing_packages}

这里是一个使用MySQL数据库的Zabbix服务器和Web前端安装的示例：

```
＃yum install zabbix-server-mysql zabbix-web-mysql
```

#### 创建初始数据库 {#creating_initial_database}

通过以下命令在MySQL上创建Zabbix数据库和用户，其中&lt;root\_password&gt;应用`shell> mysql -uroot -p12345`数据库（包括撇号：）上的zabbix用户的实际root密码（例如）和&lt;password&gt;替换为新密码`…identified by '67890';`：

```
shell
>
 mysql -uroot -p 
<
root_password
>

mysql
>
 create database zabbix字符集utf8 collat​​e utf8_bin;

mysql
>
授予zabbix上的所有权限* to zabbix @ localhost由'
<
password
>
'标识;

mysql
>
 quit;
```

现在导入初始模式和数据。请务必插入正确的版本`3.2.*`。系统将提示您输入新创建的密码。

```
＃zcat /usr/share/doc/zabbix-server-mysql-3.2.*/create.sql.gz | 
mysql -uzabbix -p zabbix
```

为了检查您的软件包中的版本，请使用以下命令：

```
＃rpm -q zabbix-server-mysql
```

#### Zabbix服务器的数据库配置 {#database_configuration_for_zabbix_server}

在zabbix\_server.conf中编辑服务器主机，名称，用户和密码，如下所示，其中DBPassword是您设置的创建初始数据库的密码：

```
＃vi /etc/zabbix/zabbix_server.conf

DBHost = localhost

DBName = zabbix

DBUser = zabbix

DBPassword = 
<
password
>
```

#### 启动Zabbix服务器进程 {#starting_zabbix_server_process}

是时候启动Zabbix服务器进程，并使其在系统启动时启动：

```
＃systemctl start zabbix-server

＃systemctl enable zabbix-server
```

#### Zabbix前端的PHP配置 {#php_configuration_for_zabbix_frontend}

Zabbix frontend的Apache配置文件位于/etc/httpd/conf.d/zabbix.conf中。一些PHP设置已配置。但有必要取消注释“date.timezone”设置，并为您[设置正确的时区](http://php.net/manual/en/timezones.php)。

```
php_value max_execution_time 300

php_value memory_limit 128M

php_value post_max_size 16M

php_value upload_max_filesize 2M

php_value max_input_time 300

php_value always_populate_raw_post_data -1

＃php_value date.timezone欧洲/里加
```

#### SELinux配置 {#selinux_configuration}

在强制模式下启用SELinux状态后，需要执行以下命令以使Zabbix前端成功连接到服务器：

```
＃setsebool -P httpd_can_connect_zabbix on
```

由于前端和SELinux配置完成，您需要重新启动Apache Web服务器：

```
＃systemctl start httpd
```

#### 安装前端 {#installing_frontend}

现在您可以继续[前端安装步骤](https://www.zabbix.com/documentation/3.2/manual/installation/install#installing_frontend)，这将允许您访问您新安装的Zabbix。

Zabbix官方存储库为RHEL提供fping，iksemel，libssh2软件包。

这些软件包位于

[_不受支持的_](http://repo.zabbix.com/non-supported/)

目录中。

---

### Debian / Ubuntu {#debianubuntu}

#### 安装软件包 {#installing_packages1}

这里是一个使用MySQL数据库的Zabbix服务器和Web前端安装的示例：

```
＃apt-get install zabbix-server-mysql zabbix-frontend-php
```

#### 创建初始数据库 {#creating_initial_database1}

通过以下命令在MySQL上创建Zabbix数据库和用户，其中&lt;root\_password&gt;应用`shell> mysql -uroot -p12345`数据库（包括撇号：）上的zabbix用户的实际root密码（例如）和&lt;password&gt;替换为新密码`…identified by '67890';`：

```
shell> mysql -uroot -p<root_password>
mysql> create database zabbix character set utf8 collate utf8_general_ci;
mysql> grant all privileges on zabbix.* to zabbix@localhost identified by '<password>';
mysql> quit;
```

然后导入初始模式和数据。系统将提示您输入新创建的密码。

```
zcat /usr/share/zabbix-server-mysql/{schema,images,data}.sql.gz | mysql -uzabbix -p zabbix
```

#### Zabbix服务器的数据库配置 {#database_configuration_for_zabbix_server1}

在zabbix\_server.conf中编辑服务器主机，名称，用户和密码，如下所示，其中DBPassword是您设置的创建初始数据库的密码::

```
＃vi /etc/zabbix/zabbix_server.conf

DBHost = localhost

DBName = zabbix

DBUser = zabbix

DBPassword = <password>
```

#### 启动Zabbix服务器进程 {#starting_zabbix_server_process1}

现在你可以启动Zabbix服务器进程，并使其在系统启动时启动

```
＃service zabbix-server start

＃update-rc.d zabbix-server enable
```

#### Zabbix前端的PHP配置 {#php_configuration_for_zabbix_frontend1}

Zabbix frontend的Apache配置文件位于/etc/zabbix/apache.conf中。一些PHP设置已配置。但有必要取消注释“date.timezone”设置，并为您[设置正确的时区](http://php.net/manual/en/timezones.php)。

```
php_value max_execution_time 300

php_value memory_limit 128M

php_value post_max_size 16M

php_value upload_max_filesize 2M

php_value max_input_time 300

php_value always_populate_raw_post_data -1

＃php_value date.timezone Aisa/Shanghai
```

之后，您需要重新启动Apache Web服务器：

```
＃service apache2 restart
```

如果您在强制模式下启用SELinux状态，请参阅上述RHEL / CentOS的[相应块](https://www.zabbix.com/documentation/3.2/manual/installation/install_from_packages/server_installation_with_mysql#selinux_configuration)。

#### 安装前端 {#installing_frontend1}

现在您可以继续[前端安装步骤](https://www.zabbix.com/documentation/3.2/manual/installation/install#installing_frontend)，这将允许您访问您新安装的Zabbix。

