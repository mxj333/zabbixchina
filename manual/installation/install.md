### 4 [从源安装](https://www.zabbix.com/documentation/3.2/manual/installation/install) {#installation_from_sources}

你可以通过源编译安装Zabbix的最新版。

本节是从源安装Zabbix的分步教程。

#### 1 安装Zabbix服务器 {#installing_zabbix_daemons}

##### 1 下载源文件 {#download_the_source_archive}

Go to the[Zabbix download page](http://www.zabbix.com/download.php)and download the source archive. Once downloaded, extract the sources, by running:

```
$ tar -zxvf zabbix-3.2.0.tar.gz
```

```
Enter the correct Zabbix version in the command. It must match the name of the downloaded archive.
```

##### 2 创建用户账号 {#create_user_account}

For all of the Zabbix daemon processes, an unprivileged user is required. If a Zabbix daemon is started from an unprivileged user account, it will run as that user.

However, if a daemon is started from a 'root' account, it will switch to a 'zabbix' user account, which must be present. To create such a user account \(in its own group, “zabbix”\) on Linux systems, run:

```
groupadd zabbix
useradd -g zabbix zabbix
```

A separate user account is not required for Zabbix frontend installation.

如果Zabbix服务器和代理服务器是运行在同一台机器，建议使用不同的用户运行服务器和运行代理。否则，如果两者都运行相同的用户，代理可以访问服务器的配置文件，在Zabbix的任何管理员级别的用户可以很容易地检索，例如，数据库密码。

