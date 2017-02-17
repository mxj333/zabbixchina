# [如何使用的zabbix API（购置主机列表中）](https://blog.apar.jp/zabbix/3055/)

随着的zabbix API，从程序或命令行，你可以添加一台主机，就可以得到的监测数据。当诸如自动化工具，大厨相结合，有可能实现自动化的监视设置甚至服务器。有一个小深奥的图像和听到的API，但是，的zabbix API是[JSON-RPC 2.0](http://www.jsonrpc.org/specification)似乎是因为他们顺应了简单的规范，它使用比较简单。在这项研究中，我们介绍的基本使用从PHP的zabbix API的。



## 版本信息采集的zabbix API的

首先，以确认的基本要求和方法在JSON-RPC 2.0的反应，试图得到一个版本的zabbix API的。

### 创建一个数据请求



PHP

| 1234567 | $request=array\('jsonrpc'=&gt;'2.0','method'=&gt;'apiinfo.version','id'=&gt;1,'auth'=&gt;null,'params'=&gt;array\(\),\); |
| :--- | :--- |




**jsonrpc**  
　指定JSON-RPC的协议版本。此参数始终设置为“2.0”。

**方法**  
[的zabbix API方法](https://www.zabbix.com/documentation/2.4/manual/api/reference)指定。这一次，以获得API版本[apiinfo.version](https://www.zabbix.com/documentation/2.4/manual/api/reference/apiinfo/version)设置方法。

**标识**  
　值在这里指定，因为它也是在响应将被返回。用于识别多个请求和响应。请求会如果它是一个来可被设定为“1”。

**AUTH**  
　指定访问令牌。在大多数的方法，这个参数是强制性的，但你已经设置了空，因此你不需要只是apiinfo.version方法来获取版本。

**PARAMS**  
　指定参数传递给该方法。在这里，也用不着apiinfo.version方法，并设置一个空数组。

### 转换JSON格式的请求数据

数据与API的zabbix进行交换，使您在使用JSON格式，它已经转换成JSON格式。

PHP

| 1 | $request\_json=json\_encode\($request\); |
| :--- | :--- |




### 创建HTTP流上下文

它是在准备POST发送到的zabbix API。PHP在[stream\_context\_create](http://php.net/manual/ja/function.stream-context-create.php)方便使用。

PHP

| 123456 | $opts\['http'\]=array\('method'=&gt;'POST','header'=&gt;'Content-Type: application/json-rpc','content'=&gt;$request\_json,\);$context=stream\_context\_create\($opts\); |
| :--- | :--- |




**方法**  
　是指定的HTTP方法。设置“POST”。

**头**  
　指定的HTTP标头。始终“内容类型：应用程序/ json- RPC”设置。

**内容**  
　和设置您刚刚创建JSON格式的请求数据。

### 一个请求的执行

只有当发送到的zabbix API的请求。API的URL是如下。

HTTPS：\[管理画面的URL\] // /api\_jsonrpc.php

当你访问令牌，因为它管理用户发送密码，我们建议您使用HTTPS。

PHP

| 12 | $url='https://example.com/zabbix/api\_jsonrpc.php';$response\_json=file\_get\_contents\($url,false,$context\); |
| :--- | :--- |




### 响应显示

JSON格式的响应将被退回。为了更容易检查的内容，并从此显示转换为一个数组。

PHP

| 12 | $response=json\_decode\($response\_json,true\);var\_dump\($response\); |
| :--- | :--- |




总之，这将是在下面的这样的程序。处理比“请求数据的创造”另一个是基本上任何的zabbix API的方法相同。

PHP

| 12345678910111213141516171819202122232425262728 | &lt;?php// リクエストデータの作成$request=array\('jsonrpc'=&gt;'2.0','method'=&gt;'apiinfo.version','id'=&gt;1,'auth'=&gt;null,'params'=&gt;array\(\),\);// リクエストデータを JSON 形式に変換$request\_json=json\_encode\($request\);// HTTPストリームコンテキストの作成$opts\['http'\]=array\('method'=&gt;'POST','header'=&gt;'Content-Type: application/json-rpc','content'=&gt;$request\_json,\);$context=stream\_context\_create\($opts\);// リクエストの実行$url='https://example.com/zabbix/api\_jsonrpc.php';$response\_json=file\_get\_contents\($url,false,$context\);// レスポンスの表示$response=json\_decode\($response\_json,true\);var\_dump\($response\); |
| :--- | :--- |




当你运行程序时，你将看到类似下面的响应。结果是的zabbix API的版本。还可以保证它返回相同的“1”，并要求的ID。

PHP

| 12345678 | array\(3\){\["jsonrpc"\]=&gt;string\(3\)"2.0"\["result"\]=&gt;string\(5\)"2.4.2"\["id"\]=&gt;int\(1\)} |
| :--- | :--- |




## 的zabbix API访问令牌的收购

正如我前面写的，以最常用的API的zabbix方法，你将需要访问令牌。

访问令牌的收购[user.login](https://www.zabbix.com/documentation/2.4/manual/api/reference/user/login)使用的方法。传递到方法，并设置管理用户名和密码的参数。

PHP

| 12345678910 | $request=array\('jsonrpc'=&gt;'2.0','method'=&gt;'user.login','params'=&gt;array\('user'=&gt;'Admin',　←管理ユーザ名'password'=&gt;'zabbix',　←パスワード\),'id'=&gt;1,'auth'=&gt;null,\); |
| :--- | :--- |




比请求数据处理其他是相同的版本采集时。  
当你运行程序时，您将收到类似下面的响应。结果是访问令牌。

PHP

| 12345678 | array\(3\){\["jsonrpc"\]=&gt;string\(3\)"2.0"\["result"\]=&gt;string\(32\)"f6ae88c261483c1ec3b6ceb0df6d7fa6"\["id"\]=&gt;int\(1\)} |
| :--- | :--- |




## 监控主机列表的收购

由于访问令牌能够得到，试图让监控主机尝试的列表。

监控主机列表是[host.get](https://www.zabbix.com/documentation/2.4/manual/api/reference/host/get)使用的方法。设置访问令牌，你刚刚得到的AUTH参数。

PHP

| 12345678910 | $request=array\('jsonrpc'=&gt;'2.0','method'=&gt;'host.get','params'=&gt;array\('output'=&gt;array\('hostid','host'\),'selectInterfaces'=&gt;array\('interfaceid','ip'\),\),'id'=&gt;1,'auth'=&gt;'ddadcf12532aaf8c41edff2a13a2202e',\); |
| :--- | :--- |




当你运行程序时，您将收到类似下面的响应。如果您指定传递给方法的参数，监控主机的各种信息是，你可以得到。可以指定参数[的官方手册](https://www.zabbix.com/documentation/2.4/manual/api/reference/host/get)，请参考。

PHP

| 1234567891011121314151617181920212223242526272829303132333435363738394041424344454647484950 | array\(3\){\["jsonrpc"\]=&gt;string\(3\)"2.0"\["result"\]=&gt;array\(2\){\[0\]=&gt;array\(3\){\["hostid"\]=&gt;string\(5\)"10084"\["host"\]=&gt;string\(13\)"Zabbix server"\["interfaces"\]=&gt;array\(1\){\[0\]=&gt;array\(2\){\["interfaceid"\]=&gt;string\(1\)"1"\["ip"\]=&gt;string\(9\)"127.0.0.1"}}}\[1\]=&gt;array\(3\){\["hostid"\]=&gt;string\(5\)"10105"\["host"\]=&gt;string\(6\)"LAMP01"\["interfaces"\]=&gt;array\(2\){\[0\]=&gt;array\(2\){\["interfaceid"\]=&gt;string\(1\)"2"\["ip"\]=&gt;string\(11\)"172.16.1.20"}\[1\]=&gt;array\(2\){\["interfaceid"\]=&gt;string\(1\)"3"\["ip"\]=&gt;string\(11\)"172.16.1.20"}}}}\["id"\]=&gt;int\(1\)} |
| :--- | :--- |




## 官方手册ZABBIX API

ZABBIX API是非常广泛的官方文件。请参阅下面的详细资料。

▽的zabbix API手册  
[https://www.zabbix.com/documentation/2.4/manual/api](https://www.zabbix.com/documentation/2.4/manual/api)

的zabbix API方法▽名单  
[https://www.zabbix.com/documentation/2.4/manual/api/reference](https://www.zabbix.com/documentation/2.4/manual/api/reference)

## 在结束

如果你有不同的检查的zabbix API的事情，我发现在正式训练的文章。虽然当然是像需要的zabbix的认证，它很可能要牢固学习的量。

