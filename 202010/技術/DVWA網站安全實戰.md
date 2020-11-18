#
```


```
# 1.環境建置
```
使用環境

```
## 啟動image
### 
```
docker image ls
```
### 
```
docker run -p 80:80 -t vulnerables/web-dvwa
```
## 登入DVWA進行設定
```
步驟1: 登入DVWA
       帳號:admin  密碼:password
```
```
步驟2:設定資料庫  
```
![DVWA_2.png](pic/DVWA_2.png)

成功畫面

![DVWA_3.png](pic/DVWA_3.png)


# 2.測試

### 2.1command injection
```

```

原始碼分析
```
<?php

if( isset( $_POST[ 'Submit' ]  ) ) {
    // Get input
    $target = $_REQUEST[ 'ip' ];

    // Determine OS and execute the ping command.
    if( stristr( php_uname( 's' ), 'Windows NT' ) ) {
        // Windows
        $cmd = shell_exec( 'ping  ' . $target );
    }
    else {
        // *nix
        $cmd = shell_exec( 'ping  -c 4 ' . $target );
    }

    // Feedback for the end user
    echo "<pre>{$cmd}</pre>";
}

?>
```
### low註解說明

客戶端原始碼註解
```

	<form name="ping" action="#" method="post">
			<p>
				Enter an IP address:
				<input type="text" name="ip" size="30">
				<input type="submit" name="Submit" value="Submit">
			</p>

	</form>
```

伺服器接收資料的程式分析
```
<?php

//PHP 使用$_POST接收客戶端傳來的資料
//https://www.wibibi.com/info.php?tid=144
//https://www.runoob.com/php/php-post.html
//https://www.webtech.tw/info.php?tid=34

if( isset( $_POST[ 'Submit' ]  ) ) {
    $target = $_REQUEST[ 'ip' ];
    //  Get input　使用$_REQUEST來接收傳來的資料
    //  $target =你輸入的IP
　　//  完全沒有做任何輸入驗證（input validation）

    // Determine OS and execute the ping command.
    if( stristr( php_uname( 's' ), 'Windows NT' ) ) {
        // Windows
        $cmd = shell_exec( 'ping  ' . $target );
    }
    else {
        // *nix
        $cmd = shell_exec( 'ping  -c 4 ' . $target );
    }

    // Feedback for the end user
    echo "<pre>{$cmd}</pre>";
}

?>
```
