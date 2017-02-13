### 4 [从源安装](https://www.zabbix.com/documentation/3.2/manual/installation/install) {#installation_from_sources}

你可以通过源编译安装Zabbix的最新版。

本节是从源安装Zabbix的分步教程。

#### 1 安装Zabbix服务器 {#installing_zabbix_daemons}

##### 1 下载源文件 {#download_the_source_archive}

请前往 [Zabbix download page](http://www.zabbix.com/download.php)下载源归档文件。下载后，通过运行以下命令提取源：

```
$ tar -zxvf zabbix-3.2.0.tar.gz
```

```
    在命令中输入正确的Zabbix版本。它必须与下载的存档的名称相匹配。
```

##### 2 创建用户账户 {#create_user_account}

对于所有Zabbix守护进程，需要一个非特权用户。如果Zabbix守护程序从非特权用户帐户启动，它将作为该用户运行。

但是，如果从“root”帐户启动守护程序，它将切换到“zabbix”用户帐户。因此要在Linux系统上创建此类用户帐户（在其自己的组“zabbix”中），请运行：

```
groupadd zabbix
useradd -g zabbix zabbix
```

Zabbix前端安装不需要单独的用户帐户。

如果Zabbix[服务器](https://www.zabbix.com/documentation/3.2/manual/concepts/server)和[agent](https://www.zabbix.com/documentation/3.2/manual/concepts/agent)在同一台机器上运行，则建议使用不同的用户来运行服务器，而不是运行agent。否则，如果两者都作为同一用户运行，则agent可以访问服务器配置文件，并且Zabbix中的任何管理级别用户可以很容易地检索例如数据库密码。

```
    将Zabbix作为root，bin或任何其他具有特殊权限的帐户运行是一种安全风险。
```


