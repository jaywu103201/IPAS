#
```

NET指令是Windows NT中的一個功能強大的工具。雖然必須用指令行方式執行，但它的功能確覆蓋了Windows NT中 大部分重要的管理功能
例如，它可以管理網路環境、各種服務程序的執行和配置、進行用戶和登入管理等。
它還可以檢視伺服器的許多本機信息。
Windows98中也包含NET指令，但其功能比在NT中少得多。
可以通過以下兩種方法獲得NET指令的說明 信息： 
(1)在NT下可以用圖形的方式，通過開始選單>說明 >索引，然後輸入NET。
(2)也可以在指令行方式下輸入NET /?或NET或NET HELP得到它的功能（COMMAND）列表，
然後通過NET COMMAND /HELP或NET HELP COMMAND 或NET COMMAND /? 指令得到相應功能的說明 信息。

在使用NET指令時需要注意的是：它的有一些指令是會馬上產生作用並永久儲存的，使用的時候要慎重。

下面對NET指令的不同參數的基本用法做一些初步的介紹：
1. NET VIEW 作用：顯示域列表、電腦列表或指定電腦的共享資源列表。
指令格式：
net view [\\computername | /domain[:domainname]] 
參數介紹：
(1)鍵入不帶參數的net view顯示當前域的電腦列表。
(2)\\computername 指定要檢視其共享資源的電腦。
(3)/domain[:domainname]指定要檢視其可用電腦的域。
舉例說明：
(1)net view \\XIAOHU檢視XIAOHU的共享資源列表。
(2)net view /domain:MYDOMAIN檢視MYDOMAIN域中的機器列表。

2. NET USER 作用：增加或更改用戶帳號或顯示用戶帳號信息。該指令也可以寫為 net users。 
指令格式：
net user [username [password | *] [options]][/domain]
參數介紹：
(1)鍵入不帶參數的net user檢視電腦上的用戶帳號列表。
(2)username增加、刪除、更改或檢視用戶帳號名。
(3)password為用戶帳號分配或更改密碼。
(4)*提示輸入密碼。
(5)/domain在電腦主域的主域控制器中執行操作。
舉例說明：
(1)net user xiaohu檢視用戶XIAOHU的信息。

3. NET USE 作用：連接電腦或中斷連線電腦與共享資源的連接，或顯示電腦的連接信息。
指令格式：
net use [devicename | *] [\\computername\sharename[\volume]] [password | *]] [/user:[domainname\]username] [[/delete] | [/persistent:{yes | no}]]
參數介紹：
(1)鍵入不帶參數的net use列出網路連接。
(2)devicename指定要連線到的資源名稱或要中斷連線的設備名稱。
(3)\\computername\sharename伺服器及共享資源的名稱。
(4)password訪問共享資源的密碼。
(5)*提示鍵入密碼。
(6)/user指定進行連接的另外一個用戶。
(7)domainname指定另一個域。
(8)username指定登入的用戶名。
(9)/home將用戶連線到其宿主目錄。
(10)/delete取消指定網路連接。
(11)/persistent控制永久網路連接的使用。
舉例說明：
(1)net use e: \\XIAOHU\TEMP將\\XIAOHU\TEMP目錄建立為E碟。
(2)net use e: \\XIAOHU\TEMP /delete中斷連線連接。

4. NET TIME 作用：使電腦的時鐘與另一台電腦或域的時間同步。
指令格式：
net time [\\computername | /domain[:name]] [/set]
參數介紹：
(1)\\computername要檢查或同步的伺服器名。
(2)/domain[:name]指定要與其時間同步的域。
(3)/set使本電腦時鐘與指定電腦或域的時鐘同步。

下面的這4個參數是相關的，所以一起介紹： 
5. Net Start 作用：啟動服務，或顯示已啟動服務的列表。
指令格式：
net start service 
6. Net Pause 作用：暫停正在執行的服務。
指令格式：
net pause service
7. Net Continue 作用：重新啟動掛起的服務。
指令格式：
net continue service
8. NET STOP 作用：停止 Windows NT 網路服務。
指令格式：
net stop service 
參數介紹：
(1)alerter(警報)
(2)client service for netware(Netware 客戶端服務) 
(3)clipbook server(剪貼簿伺服器)
(4)computer browser(電腦瀏覽器)
(5)directory replicator(目錄複製器)
(6)ftp publishing service (ftp )(ftp 發行服務)
(7)lpdsvc
(8)net logon(網路登入)
(9)network dde(網路 dde)
(10)network dde dsdm(網路 dde dsdm)
(11)network monitor agent(網路監控代理)
(12)nt lm security support provider(NT LM 安全性支持提供)
(13)ole(對像連接與嵌入)
(14)remote access connection manager(遠端訪問連接管理器)
(15)remote access isnsap service(遠端訪問 isnsap 服務)
(16)remote access server(遠端訪問伺服器)
(17)remote procedure call (rpc) locator(遠端程序使用定位器)
(18)remote procedure call (rpc) service(遠端程序使用服務)
(19)schedule(調度)
(20)server(伺服器)
(21)simple tcp/ip services(簡單 TCP/IP 服務)
(22)snmp
(23)spooler(後台列印程序)
(24)tcp/ip netbios helper(TCP/IP NETBIOS 協助工具)
(25)ups
(26)workstation(工作站)
(27)messenger(信使)
(28)dhcp client
(29)eventlog

9. Net Statistics 作用：顯示本機工作站或伺服器服務的統計記錄。
指令格式：
net statistics [workstation | server]
參數介紹：
(1)鍵入不帶參數的net statistics列出其統計信息可用的執行服務。
(2)workstation顯示本機工作站服務的統計信息。
(3)server顯示本機伺服器服務的統計信息。
舉例說明：
net statistics server | more顯示伺服器服務的統計信息。

10. Net Share 作用：新增、刪除或顯示共享資源。
指令格式：
net share share name=driveath [/users:number | /unlimited] [/remark:"text"] 
參數介紹：
(1)鍵入不帶參數的net share顯示本機電腦上所有共享資源的信息。
(2)sharename是共享資源的網路名稱。
(3)driveath指定共享目錄的絕對路徑。
(4)/users:number設定可同時訪問共享資源的最大用戶數。
(5)/unlimited不限制同時訪問共享資源的用戶數。
(6)/remark:"text "增加關於資源的註釋，註釋文字用引號引住。
舉例說明：
(1)net share mymydomain=c:\temp /remark:"my first share"以mymydomain為共享名共享 C:\temp。 (2)net share mymydomain /delete停止共享mymydomain目錄。

11. Net Session 作用：列出或中斷連線本機電腦和與之連接的客戶端的會話，也可以寫為net sessions或net sess。
指令格式：
net session [\\computername] [/delete] 
參數介紹：
(1)鍵入不帶參數的net session顯示所有與本機電腦的會話的信息。
(2)\\computername標識要列出或中斷連線會話的電腦。
舉例說明：
net session \\XIAOHU要顯示電腦名稱為XIAOHU的客戶端會話信息列表。 

12. Net Send 作用：向網路的其他用戶、電腦或通信名傳送消息。
指令格式：
net send {name | * | /domain[:name] | /users} message 
參數介紹：
(1)name要接收傳送消息的用戶名、電腦名稱或通信名。
(2)*將消息傳送到組中所有名稱。
(3)/domain[:name]將消息傳送到電腦域中的所有名稱。
(4)/users將消息傳送到與伺服器連接的所有用戶。
(5)message作為消息傳送的文本。
舉例說明：
(1)net send /users server will shutdown in 5 minutes給所有連線到伺服器的用戶傳送關 機消息。 

13. Net Print 作用：顯示或控制列印作業及列印貯列。
指令格式：
net print [\\computername ] job# [/hold | /release | /delete]
參數介紹：
(1)computername共享列印機貯列的電腦名稱。
(2)sharename列印貯列名稱。
(3)job#在列印機貯列中分配給列印作業的標識號。
(4)/hold使用 job# 時，在列印機貯列中使列印作業等待。
(5)/release釋放保留的列印作業。
(6)/delete從列印機貯列中刪除列印作業。
舉例說明：
(1)net print \\XIAOHU\SEEME列出\\XIAOHU電腦上SEEME列印機貯列的目錄。

14. Net Name 作用：增加或刪除消息名（有時也稱別名），或顯示電腦接收消息的名稱列表。 
指令格式：
net name [name [/add | /delete]]
參數介紹：
(1)鍵入不帶參數的net name列出當前使用的名稱。
(2)name指定接收消息的名稱。
(3)/add將名稱增加到電腦中。
(4)/delete從電腦中刪除名稱。

15. Net Localgroup 作用：增加、顯示或更改本機組。
指令格式：
net localgroup groupname {/add [/comment:"text "] | /delete} [/domain]
參數介紹：
(1)鍵入不帶參數的net localgroup顯示伺服器名稱和電腦的本機組名稱。
(2)groupname要增加、擴充或刪除的本機組名稱。
(3)/comment: "text "為新增或現有組增加註釋。
(4)/domain在當前域的主域控制器中執行操作，否則僅在本機電腦上執行操作?
(5)name [ ...]列出要增加到本機組或從本機組中刪除的一個或多個用戶名或組名。
(6)/add將全局組名或用戶名增加到本機組中。
(7)/delete從本機組中刪除組名或用戶名。
舉例說明：
(1)net localgroup mydomain /add將名為mydomain的本機組增加到本機用戶帳號資料庫。 (2)net localgroup mydomain顯示mydomain本機組中的用戶。

16. Net Group 作用：在 Windows NT Server 域中增加、顯示或更改全局組。
指令格式：
net group groupname {/add [/comment:"text "] | /delete} [/domain]
參數介紹：
(1)鍵入不帶參數的net group顯示伺服器名稱及伺服器的組名稱。
(2)groupname要增加、擴展或刪除的組。
(3)/comment:"text "為新增組或現有組增加註釋。
(4)/domain在當前域的主域控制器中執行該操作，否則在本機電腦上執行操作? (5)username[ ...]列表顯示要增加到組或從組中刪除的一個或多個用戶
(6)  /add增加組或在組中增加用戶名。
(7)  /delete刪除組或從組中刪除用戶名。
舉例說明：
net group mydomain xiaohu1 xiaohu2 /add將現有用戶帳號xiaohu1和xiaohu2增加到本機計算 機的mydomain組。 

17. Net Config 作用：顯示當前執行的可配置服務，或顯示並更改某項服務的設定。
指令格式：
net config [service [options]]
參數介紹：
(1)鍵入不帶參數的net config顯示可配置服務的列表。
(2)service通過net config指令進行配置的服務(server或workstation)。
(3)options服務的特定選項。

18. Net Computer 作用：從Domain資料庫中增加或刪除電腦。
指令格式：
net computer \\computername {/add | /del}
參數介紹：
(1)\\computername指定要增加到域或從域中刪除的電腦。
(2)/add將指定電腦增加到域。
(3)/del將指定電腦從域中刪除。
舉例說明：
net computer \\cc /add將電腦 cc 增加到登入域。

19. Net Accounts 作用：更新用戶帳號資料庫、更改密碼及所有帳號的登入要求。
指令格式：
net accounts [/forcelogoff:{minutes | no}] [/minpwlen:length] [/maxpwage:{days | unlimited}] [/minpwage:days] [/uniquepw:number] [/domain]
參數介紹：
(1)鍵入不帶參數的net accounts顯示當前密碼設定、登入時限及域信息。 (2)/forcelogoff:{minutes | no}設定當用戶帳號或有效登入時間過期時。
(3)/minpwlen:length設定用戶帳號密碼的最少字串數。
(4)/maxpwage:{days | unlimited}設定用戶帳號密碼有效的最大天數。
(5)/minpwage:days設定用戶必須保持原密碼的最小天數。
(6)/uniquepw:number要求用戶更改密碼時，必須在經過number次後才能重複使用與之相同的密碼。
(7)/domain在當前域的主域控制器上執行該操作。
(8)/sync當用於主域控制器時，該指令使域中所有制作備份域控制器同步。 
舉例說明：
net accounts /minpwlen:7將用戶帳號密碼的最少字串數設定為7。

```
