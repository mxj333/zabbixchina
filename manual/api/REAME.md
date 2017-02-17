# [如何使用的zabbix API（购置主机列表中）](https://blog.apar.jp/zabbix/3055/)

使用zabbix API，从程序或命令行，你可以添加一台主机，就可以得到的监测数据。如果用自动化工具和Chef等组合的话，可能实现自动化的监视设置甚至服务器。Zabbix API接口，它们遵循[JSON-RPC 2.0](http://www.jsonrpc.org/specification)规范，使用比较简单。
在这篇文章中，我们介绍的基本使用从PHP的zabbix API的。

## 版本信息采集的zabbix API

首先，以确认的基本要求和方法在JSON-RPC 2.0的反应，试图得到一个版本的zabbix API的。

### 创建一个数据请求

**PHP**
```
$request = array(
    'jsonrpc'   => '2.0',
    'method'    => 'apiinfo.version',
    'id'        => 1,
    'auth'      => null,
    'params'    => array(),
);
```

**jsonrpc**  
　指定JSON-RPC的协议版本。此参数始终设置为“2.0”。

**method**  
指定[zabbix API方法](https://www.zabbix.com/documentation/2.4/manual/api/reference)。例如，获得API版本[apiinfo.version](https://www.zabbix.com/documentation/2.4/manual/api/reference/apiinfo/version) 设置方法。

**id**  
　标识值在这里指定，因为它也是在响应将被返回。用于识别多个请求和响应。请求会如果它是一个来可被设定为“1”。

**auth**  
　指定访问令牌。在大多数的方法，这个参数是强制性的，但你已经设置了空，因此你不需要只是apiinfo.version方法来获取版本。

**PARAMS**  
　指定参数传递给该方法。在这里，也用不着apiinfo.version方法，并设置一个空数组。

### 转换JSON格式的请求数据

数据与API的zabbix进行交换时使用JSON格式，所以要转换成JSON格式。

```
$request_json = json_encode($request);
```

### 创建HTTP流上下文

它是在把数据POST到的zabbix API 时使用。在[stream\_context\_create](http://php.net/manual/ja/function.stream-context-create.php)。
```
$opts['http'] = array(
    'method'    => 'POST',
    'header'    => 'Content-Type: application/json-rpc',
    'content'   => $request_json,
);
$context = stream_context_create($opts);
```

**method**  
　是指定的HTTP方法。设置“POST”。

**header**  
　指定的HTTP标头。始终“内容类型：应用程序/ json- RPC”设置。

**header**  
　创建JSON格式的请求数据。

### 一个请求的执行

只有当发送到的zabbix API的请求。API的URL是如下。

```
https://<你的zabbix访问地址>/api_jsonrpc.php
```

当你访问令牌时，因为它发送密码，我们建议您使用HTTPS。

```
$url = 'https://example.com/zabbix/api_jsonrpc.php';
$response_json = file_get_contents($url, false, $context);

```


### 响应显示

 APA响应将退回JSON格式。为了更容易检查内容，将显示转换为一个数组。

```
$response = json_decode($response_json, true);
var_dump($response);
```

总之，这将是在下面的这样的程序。基于zabbix API请求数据的方法是相同的。
```
<?php
// リクエストデータの作成
$request = array(
    'jsonrpc'   => '2.0',
    'method'    => 'apiinfo.version',
    'id'        => 1,
    'auth'      => null,
    'params'    => array(),
);
 
// リクエストデータを JSON 形式に変換
$request_json = json_encode($request);
 
// HTTPストリームコンテキストの作成
$opts['http'] = array(
    'method'    => 'POST',
    'header'    => 'Content-Type: application/json-rpc',
    'content'   => $request_json,
);
$context = stream_context_create($opts);
 
// リクエストの実行
$url = 'https://example.com/zabbix/api_jsonrpc.php';
$response_json = file_get_contents($url, false, $context);
 
// レスポンスの表示
$response = json_decode($response_json, true);
var_dump($response);
```

当你运行程序时，你将看到类似下面的响应。结果是的zabbix API的版本。还可以保证它返回相同的“1”，并要求的ID。

```
array(3) {
  ["jsonrpc"]=>
  string(3) "2.0"
  ["result"]=>
  string(5) "2.4.2"
  ["id"]=>
  int(1)
}
```

##Zabbix API访问令牌

正如我前面写的，以最常用的API的zabbix方法，你将需要访问令牌。

访问需要令牌的[user.login](https://www.zabbix.com/documentation/2.4/manual/api/reference/user/login)使用的方法。调用该方法，并设置管理用户名和密码的参数。
```
$request = array(
    'jsonrpc'   => '2.0',
    'method'    => 'user.login',
    'params'    => array(
        'user'      => 'Admin',　//用户名
        'password'  => 'zabbix',　//密码
    ),
    'id'        => 1,
    'auth'      => null,
);
```

当请求数据处理与他是相同的版本采集时。  
当你运行程序时，您将收到类似下面的响应。结果是访问令牌。
```
array(3) {
  ["jsonrpc"]=>
  string(3) "2.0"
  ["result"]=>
  string(32) "f6ae88c261483c1ec3b6ceb0df6d7fa6"
  ["id"]=>
  int(1)
}
```

## 监控主机列表的收购

由于能够得到访问令牌，我们试图获取监控主机的列表。

监控主机列表是[host.get](https://www.zabbix.com/documentation/2.4/manual/api/reference/host/get)方法。设置访问令牌，你刚刚得到的AUTH参数。
```
$request = array(
    'jsonrpc'   => '2.0',
    'method'    => 'host.get',
    'params'    => array(
        'output'            => array('hostid', 'host'),
        'selectInterfaces'  => array('interfaceid', 'ip'),
    ),
    'id'        => 1,
    'auth'      => 'ddadcf12532aaf8c41edff2a13a2202e',
);
```

当你运行程序时，您将收到类似下面的响应。如果您指定传递给方法的参数，你是可以得到监控主机的各种信息。请参考[官方手册](https://www.zabbix.com/documentation/2.4/manual/api/reference/host/get)。
```
array(3) {
  ["jsonrpc"]=>
  string(3) "2.0"
  ["result"]=>
  array(2) {
    [0]=>
    array(3) {
      ["hostid"]=>
      string(5) "10084"
      ["host"]=>
      string(13) "Zabbix server"
      ["interfaces"]=>
      array(1) {
        [0]=>
        array(2) {
          ["interfaceid"]=>
          string(1) "1"
          ["ip"]=>
          string(9) "127.0.0.1"
        }
      }
    }
    [1]=>
    array(3) {
      ["hostid"]=>
      string(5) "10105"
      ["host"]=>
      string(6) "LAMP01"
      ["interfaces"]=>
      array(2) {
        [0]=>
        array(2) {
          ["interfaceid"]=>
          string(1) "2"
          ["ip"]=>
          string(11) "172.16.1.20"
        }
        [1]=>
        array(2) {
          ["interfaceid"]=>
          string(1) "3"
          ["ip"]=>
          string(11) "172.16.1.20"
        }
      }
    }
  }
  ["id"]=>
  int(1)
}
```


## ZABBIX API官方手册

ZABBIX API是非常全面的官方文档。请参阅下面的详细资料。

▽的zabbix API手册  
[https://www.zabbix.com/documentation/3.2/manual/api](https://www.zabbix.com/documentation/3.2/manual/api)

的zabbix API方法▽名单  
[https://www.zabbix.com/documentation/2.4/manual/api/reference](https://www.zabbix.com/documentation/2.4/manual/api/reference)

## 在结束

如果你有不同的检查的zabbix API的事情，我发现在正式训练的文章。虽然当然是像需要的zabbix的认证，它很可能要牢固学习的量。

