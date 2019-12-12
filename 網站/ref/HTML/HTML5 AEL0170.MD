# 第一章 HTML與CSS入門
## 1-1 html5
### 1-1-1  HTML5介紹
```
一個HTML網頁是用<html>…</html>標籤包含起來。裡面分成
  「表頭（<head>標籤）、標題（<title>標籤）」
  「內容（<body>標籤）」。

HTML5的宣告 -- <!DOCTYPE html>
```
### 1-1-2  HTML的標籤
```
<!DOCTYPE html>

<html lang-"en">
<head>
   <meta charset="utf-8" I>
   <tte>第二個HTML網頁(網頁標題)</ute>
</head>
<body>
   <h3>網頁的內容,寫在Body標籤裡面</h3>
   <p>這是一個文字段落</p>
   <a href-"http://ww.dotblogs.com.tw/mis2000lab/">超連結,前往MIS2000 Lab.的網站</a>
   <p>
     <font color-"red" sze="5">字體大小與顔色</font>
   </p>
</body>
</html>
```
## 1-2  HTML的文字項目
```
	1-3-1  文字段落，<p>與<br />
	1-3-2  文字標題，<h1>到<h6>

	1-3-3  <pre>，保存原始格式 
	1-3-4  項目符號、清單、列表

	1-3-4  項目符號、清單、列表

1-3-5  <img>，Image圖片
	1-3-5  <img>，Image圖片
1-3-6  <a>，Hyperlink超連結
	<a>超連結標籤的屬性與值如下：
	href，必填欄位。超連結的URL網址或書籤。

	target，瀏覽器如何展示這一頁？建議在HTML4.01的Transitional、Frameset DTD使用。共有下列的屬性「值」： 
	_blank，開啟一個新網頁視窗或是新的分頁（Tab）。
	_parent，如果您有使用頁框（frameset），連結的網頁將會以「父頁框」來呈現。
	_self，預設值。如果您有使用頁框（frameset），在原本的頁框範圍內呈現。
	_top，如果您有使用頁框（frameset），以「整頁」的方式來呈現，跳脫原本頁框的限制。
```
1-3  HTML表單
```
	1-4-1  <form>，填寫資料的表單
	action，接收並處理這些資訊的「網頁URL」。
	method，常用的有get與post。
1-4-2  表單的控制項（文字輸入方塊）
1-4-3  表單的控制項（按鈕）
1-4-4  表單的控制項
（單複選與下拉式選單）
1-4-5  表單的控制項（檔案上傳）
	實際上傳的步驟需要自己寫程式，這只是一個上傳檔案的選擇畫面罷了。
1-4-5  <fieldset>表單的外觀與框線

	1-5-3  表單<form>、外觀<fieldset>與標題<legend>
```
1-4  網頁裡面的Script程式
```
	HTML網頁裡面如果要加入JavaScript程式或是jQuery，可以參照<script>標籤的使用。
```

第二章  CSS概觀
HTML5、CSS、JavaScript 網頁程式設計與 MCSD 70-480 認證教材


	CSS跟上一章介紹的<script>標籤有點類似，大多寫在網頁的表頭<head>標籤裡面。基礎的架構如下：
	<style type=”text/css”>
	selector {
			property1:value;    作者註解—寫法為「屬性: 值」。 
			property2:value;
			..
			propertyN:value;
	}
	</style>

2-1  第一個CSS範例與selector
	範例CSS_01.html來說明最快（如圖），
	所謂的selector就是指向「下面的<h1>標籤」，當我們指定<h1>標籤的文字大小、顏色之後，整個網頁的<h1>標籤都會統一管理

	第二個範例CSS_02.html使用兩個selector來做。
2-2  <link>標籤，將CSS寫在另一個檔案
	CSS設定太龐大，可寫在另一個.css檔（純文字檔）。寫在<head>網頁表頭標籤裡：
	<link rel="stylesheet" type="text/css" href="mystyles.css" media="screen">

	<link>標籤的屬性如下：
	rel=”stylesheet”，表示這是一個CSS檔案的參照。
	href，CSS檔案所在位置（目錄與檔名）。
	type，MIME格式，此為純文字檔所以寫成text/css。
	media，表示CSS是針對哪一種媒體來撰寫？預設值通常寫成default可以適用各種狀況。

2-3  Case Study—使用
	

第三章  前進HTML5
3-2-1  常見的文件架構與元素
	簡單說明如下：
	<nav>用來作為導覽（navigation）。如上圖最上方，可以經由導覽列連回首頁。建議只放置主要的導覽標題到<nav>裡面。考試重點！
	<header>表示文章的標題（表頭）。不是HTML的表頭<head>，請不要搞混，認證考試會考出來！
	<article>表示文章的主體部分，可以獨立展示的Blog文章（或一篇新聞）、網友針對這篇文章的評論、或是分類目錄。使用它可以增加搜尋引擎最佳化SEO的效用，此為考試重點！可以說是必考！
	<section>用來表示文章內容的一部份，以右圖為例，一篇文章裡面有兩個<section>段落。
	<footer>表示文章的結尾（表尾）。例如：版權宣告、隱私權聲明、網站地圖（site map）等等。
	<aside>用來作為側邊列（sidebar）的內容，例如：廣告橫幅

範例 html5_01_aside.html
3-2-2  可編輯的<article>
	<artcle>的內容如果允許編輯，請改為<article contenteditable>。
	這樣的功能早在IE 5.5就有支援，當初是希望做成「所見即所得（WYSIWYG）」的瀏覽器。

	IE與Chrome瀏覽器都支援這樣的功能
	使用VS2013編輯網頁時，建議寫成<article contenteditable=”true”>。
	詳見範例HTML5_01_contenteditable.html。
3-3  <header>、<hgroup>與<nav>
3-4  <article>與<section>
	範例HTML5_04_Pearson_article.html
3-5  日期時間、文字與圖片
	<time datetime="2014-08-08">Today</time>
	<time datetime="2014-08-08T09:00:00-0500">9am today in New York</time>

	<time>4h</time>
	<time>2014</time>

	ISO（國際標準組織）的日期與時間格式
	年: YYYY (如2014)
	年月: YYYY-MM (如2014-08)
	完整日期: YYYY-MM-DD (如2014-08-16)
	日期加上時分: YYYY-MM-DDThh:mmTZD (如2014-08-16T18:25+01:00)
	日期加上時分秒: YYYY-MM-DDThh:mm:ssTZD (如2014-08-16T18:25:35+01:00)
	日期加上時分秒: YYYY-MM-DDThh:mm:ss.sTZD (如2014-08-16T18:25:35.45+01:00)
	註解：TZD代表「時區」 (Z or +hh:mm or -hh:mm) 。

	範例HTML5_06_Text.html。
	<mark>用來強調重點，會有類似螢光筆標示的段落（文字有底色）。
	<em>重點文字改用「斜體字」來表示。
3-5  details，折疊與隱藏
	範例HTML5_details.html，<details>搭配<summary>作到資訊折疊與隱藏
3-6  拖放（draggable）
	範例HTML5_draggable_2.html

第四章  CSS樣式與HTML5
HTML5、CSS、JavaScript 網頁程式設計與 MCSD 70-480 認證教材
 (碁峰出版)


	本章的結果可能因為您的瀏覽器（廠商）或是版本新舊而有差異，建議您使用新版瀏覽器來觀賞，本文撰寫時的瀏覽器為IE 11與Chrome 32.0.x版
	（註解：本書後續還有一章專門介紹新版的CSS3）。
4-1  字體，fonts
	font-family : Arial, Candara, Verdana, sans-serif;

	font-size : 16px;
	font-size : 150%;  /* 字體比平常大1.5倍。寫成150% */
	font-size : 1em;   /* 1em = 網頁的基礎字體大小，通常是16px */
4-2  色彩（color）與透明度（opacity）
	color : olive;     /* 橄欖綠 */
	color : #808000;  /* 十六進位，前面請加上 # 符號 */
	color : rgb(128, 128, 0);  /* 十進位的表示法 */
4-2  色彩（color）與透明度（opacity）
	透明度（opacity）
4-3  印刷（Typographic）屬性
	這是認證考試的重點！死背也得記下來！
4-4  CSS排版觀念與Box Model
	此為認證考試重點！

	第一種寫法：
	padding: 10px 11px 12 px 13px;
	/* 如果寫四個值，順序是「上、右、下、左」四個位置 */

	第二種寫法：
	padding-top: 10px;   /* 順序是「上、右、下、左」*/
	padding-right : 11px;
	padding-bottom : 12px;
	padding-left : 13px;
4-4-1  設定值與呈現結果的差異
4-4-2  Case Study
	範例CSS04_10_BoxModel.html。
範例CSS04_11.html
4-4-4  Content（內容）的其他設定
	範例CSS04_13_DisplayNone.html
	展示visibility:hidden與display:none這兩者的差異。
4-5  背景（Background）

第八章  HTML5 Form，表單與輸入驗證
HTML5、CSS、JavaScript 網頁程式設計與 MCSD 70-480 認證教材
 (碁峰出版)
8-1  HTML5的表單
	本章為認證考試重點！！
	典型的HTML Form（表單）如下，範例Form_01.html

8-2  其他表單元件
	8-2-1  下拉式選單<select>
	範例Form_02_Select.html

	HTML5比起以前多了一個<optgroup>的群組設定
	範例Form_02_Select.html
8-2-2  文字輸入方塊與<datalist>，類似ComboBox
	範例Form_03_datalist.html
8-2-3  多列文字輸入<textarea>
	範例Form_04_textarea.html
8-3  HTML5 <input>屬性與使用者的輸入驗證
	為了避免使用者在網頁表單上填寫錯誤資訊、格式不符、留空白（未填寫），我們需進行驗證以後才使用這些輸入資料。驗證通常分成兩方面：
	第一，	Client端（前端），也就是在瀏覽器上進行驗證。優點是：
	(1).不會浪費Web Server資源與網路頻寬，
	(2). 只需利用使用者的設備（電腦、手機或平板）就能進行驗證程序。
	(3). 對於使用者經驗（UX, User Experience）來說比較好（輸入有錯立刻呈現，不需等待）。
	第二，	Server端（後端），當資料傳回Web Server的時候進行驗證，通常寫在ASP.NET、PHP、JSP程式裡面的驗證程式就是這一類。

	最好的方式是「兩者並用」，才能驗證、過濾與篩選錯誤的資料。
8-3-2  HTML5新增的Input Type
	範例HTML5_Form_Input01.html（如圖）。
	不同的瀏覽器展示的HTML5表單也不一樣（瀏覽器若不支援，效果就出不來）。
8-3-3  HTML5新增的Input屬性
	<input type=”text”>新的屬性（attritube）如下，這裡是考試重點！！

	autofocus，輸入指標。
	autocomplete，如果您輸入的文字是以前輸入過的，就會自動列表讓您挑選。
	required，必填欄位（不可留白）。考試重點！！
	pattern，輸入正規表達式（Regular Expression）用來驗證格式或是數字，考試重點！！
	placeholder，提示訊息、浮水印文字。
	title，輸入錯誤之後的警告訊息。


	範例HTML5_Form_Input02.html的三種屬性--required、pattern、placeholder（浮水印）。
8-3-4  Regular Expression規則運算式的入門
	微軟的認證考試，正規表達式（Regular Expression）算是重點，至少會出兩三題！

	美國的電話號碼	
	^[01]?[- .]?(\([2-9]\d{2}\)|[2-9]\d{2})[- .]?\d{3}[- .]?\d{4}$
	(425) 555-0123
	425-555-0123
	425 555 0123
	1-425-555-0123
	E-mail	
	^([0-9a-zA-Z]([-.\w]*[0-9a-zA-Z])*@([0-9a-zA-Z][-\w]*[0-9a-zA-Z]\.)+[a-zA-Z]{2,9})$
	URL網址	
	^(ht|f)tp(s?)\:\/\/[0-9a-zA-Z]([-.\w]*[0-9a-zA-Z])*(:(0-9)*)*(\/?)([a-zA-Z0-9\-\.\?\,\'\/\\\+&amp;%\$#_]*)?$

8-4  以JavaScript進行使用者輸入驗證
	範例HTML5_JavaScript_01.html
<form id="Form1" method="post" action="test.aspx" Name=”Form111” onsubmit="return checkData();" >
   <input type=”text” name="email" />
   <input type="submit" value="送出按鈕" />
</form>
<script type="text/javascript">
function checkData() {
  with (document.Form111) {
     if (email.value.length == 0) {
        alert("不可留白。請輸入您的 E-Mail");
        return false;
} else {
    i = email.value.indexOf("@");
    if (i <= 0) {
       alert("您輸入的 E-mail 不正確 !沒有＠符號");
       return false;
    }        // …..省略
</script>

8-4-1  處理輸入事件
	<form id="Form111" method="post" 
	    action="registration.aspx" 
	    onsubmit="return validateForm();" >
	    ...（省略）…
	    <input type="submit" Value=”確定（送出）” />
	</form>


	<script type="text/javascript">
	    // 註解：自己撰寫額外的JavaScript來進行資料的驗證動作。
	    function validateForm() {
	        ...（省略）…
	    }
	</script>
	註解：完整範例請看HTML5_JavaScript_01.html。

8-4-2  驗證輸入（必須是數字）
	輸入驗證的題目是認證考試的最愛！
<script type="text/javascript">
function isAnInteger(text)  {
    var intTestRegex = /^\s*(\+|-)?\d+\s*$/;
    return String(text).search(intTestRegex) != -1;
}   // 微軟特別喜歡考這種題目，必考題！

function validateForm()  {
    if( !isAnInteger(document.getElementById('score').value))
        return false;  // 驗證失敗
    else
        return true;
}
</script>





第十章  使用CSS3設定HTML5的樣式
HTML5、CSS、JavaScript 網頁程式設計與 MCSD 70-480 認證教材
 (碁峰出版)


10-1  CSS3的文字樣式
	介紹CSS3的style text與style block、選取器（selector）、虛擬類別（pseudo-classes）與虛擬元素（pseudo-elements），還有CSS3增強的圖形效果。
	CSS3新增了@font-face可以把字型下載至使用者（Client端）電腦裡面。透過@font-face將TrueType或OpenType”字型檔”與網頁串連在一起。
	google網站就有提供網路字型作為CSS3的搭配，請上網搜尋「google fonts」關鍵字。
@font-face {
font-family: 'RobotoRegular';
src: url('Roboto-Regular-webfont.ttf') format('truetype');
font-stretch: normal;  // 預設值
font-weight: normal;  // 預設值
font-style: normal;    // 預設值
unicode-range: U+0-10FFFF;  // 預設值
}


	font-family（必填屬性），定義瀏覽器該如何使用字型。下面有三種範例個字使用三種字型檔（.ttf檔）。
	src（必填屬性），用來下載字型檔案或是字型檔的型態。
@font-face {
  font-family: 'RobotoRegular';
  src: url('Roboto-Regular-webfont.ttf') format('truetype');
}

10-1-2  度量單位
	第一種，絕對單位（absolute measurement）。
	Centimeters（cm，公分）。
	Millimeters（mm，公釐），10 Millimeters = 1 Centimeters。
	Inches（in，英吋），1 Inch = 2.54 Centimeters。
	Picas（pc），1 Pica = 12 Points = 1/6 Inches（in，英吋）。
	Points（pt），1 Point = 1/72 Inches（in，英吋）。
	Pixels（px），1 Pixel = 1/96 Inches（in，英吋）。

	第二種，相對單位（relative measurement）用來”等比例”的放大或是縮小。
	em，1 em = 目前元素的字體大小。2em代表目前的兩倍大。
	ex，小寫字母的高度。通常視同em的一半（0.5em）。
	ch，把目前這個字體的0當作標準「寬度」。
	rem，1 rem = html元素的字體大小（預設值為16px）。IE9開始支援這個功能。


	另外有三種「viewport-relative」用來表示「瀏覽器」視窗物件的大小。對於行動週邊（手機、平板）的用戶來說非常實用	vm，1 vm = 1%的viewport寬度（百分之一）。
	vh，1 vm = 1%的viewport高度（百分之一）。
	vmin，vm與vh挑選較小者當成單位。

	第三種，您可以透過calc()函式做到「即時運算」單位大小，即時調整畫面與文字。。
img {
    max-height: calc(100vh - 5px);
    max-width: calc(100vw - 5px);
}

10-1-3  文字特效
	CSS3新的文字特效屬性如下：
	text-indent，讓第一列的文字縮排。
	hyphens，文字斷行（換段落）。如果某一個英文單字太長，可以透過這個屬性來斷行，可以輸入的值有auto（使用 -符號來斷行）、manual（輸入一個看不見的字&shy;）、none（不斷行）。範例htpens.html。
	word-wrap（建議搭配word-break使用），單字的斷行。新的CSS3改名為overflow-wrap，屬性值有normal（在單字之間斷行）與break-word（在單字中的任意位置斷行）。注意！範例word-wrap.html在不同瀏覽器可能呈現出不同成果。
	word-spacing，文字的間距。
	text-shadow，文字陰影的特效。
10-2  CSS3的Block樣式
	CSS3新加入的Block（文字區塊）屬性。

	outlines還有四個屬性：
	outline-width，設定outlines寬度，屬性值：thin（薄）、medium（預設值）、thick（厚）三種。也可以支援單位度量，如2px或1.5em。
	outline-style，線條（區塊框線）的樣式。屬性值：none（透明、無線條）、dotted（點）、dashed（虛線）與solid（實線）等等，詳見下表。
	outline-color，顏色。
	outline-offset，與邊際的距離，詳見上面的範例outlines.html。
10-2-2  外觀
	與區塊外觀有關的屬性：
	border-radius，表格角落變成圓角。
	overflow，如果內容文字太多，導致區塊無法容納該怎麼辦呢？請看範例overflow.html與下圖。
10-2-3  多重欄位的外觀
	範例column-count_01.html
	使用column-count : 3將一篇文章切分成「三個欄位」來展示。

	四個主要的屬性可以作為多重欄位的外觀（multiple column layout）：
	column-count，使用幾個欄位來切割文章，請看上圖（範例column-count_01.html）。
	column-width，欄位之間的寬度。
	column-gap，欄位之間的間距，請看右圖。
	column-rule，欄位之間的線條使用的樣式，請看右圖。

10-2-4  區塊（Block）的外觀
	display的屬性在Block Layout有這幾種作法（詳見範例CSS_Display.html）：
	display:block，請看右圖，使用block兩段文字會換列（斷行）呈現出來。。
	display:inline，請看右圖，即使有兩段文字也會串連在一起，當成同一列呈現。
	display:none，請看右圖，畫面上不見了（看不到），也不佔空間。與visibility:hidden只是隱形看不見，還是有佔空間，兩者略有差異。詳見範例CSS_Display.html。


	display:table，以表格<table>的方式來呈現資料。
	改用CSS來繪製表格，畫面上的HTML碼變得簡潔，適合與程式搭配（不然的話，畫面原始碼很亂）。
	詳見範例CSS_Display_table.html（結果請看下圖）。
10-3  虛擬類別（pseudo-classes）與
        虛擬元素（pseudo-elements）
	範例Text_first-letter.html，針對段落<p>第一個字的效果。

	範例Text_after.html
	段落<p>裡面「後面、最末端」的效果。
10-3-2  超連結<a>的虛擬類別
	超連結<a>會用到的五種虛擬類別。
	a:link，所有「尚未」被瀏覽（使用）過的超連結。
	a:visited，所有「已經」被瀏覽（使用）過的超連結。與上面的:link效果互斥。
	a:focus，所有被鎖定焦點的超連結。例如範例Text_A_Hyperlink.html。
	a:hover，「滑鼠指標經過」的超連結會展現此效果，例如範例Text_focus.html。
	a:active，所有「被選取」的超連結，滑鼠「按下」到「放開」的那段時間內，例如範例Text_A_Hyperlink.html。

10-3-3  表單<form>的虛擬類別
	三種表單<form>常用的虛擬類別如下。詳見範例Text_focus.html。
	input:enabled，正常情況下的表單效果。
	input:disabled，表單選項失能（不可使用）的時候。
	input:checked，單選、複選選單被按下某一個子選項。
	input:focus，成為輸入焦點的時候（詳見右圖），例如正在填寫這個TextBox，或是用Tab按鍵下上移動到這個TextBox。
	input:hover，滑鼠經過時。

10-4  使用CSS3增強圖形效果
	10-4-1  設定顏色

	第一，147種關鍵字（英文）可以用來對應顏色，例如：red、green、darkgreen（深綠）、navy（海軍藍）等等常用的英文單字。

	第二，RGB（red-green-blue）的寫法，以三個或是六個「十六進位（hexadecimal）」的表示法。詳見右圖。

	第三，RGBA（red-green-blue-alpha）。
10-4-2  定義背景與效果
	第一，	多圖片的背景（Multi-Images Backgrounds）。
article {
background-image: url('bluearrow.png'), url('greenarrow.png');

background-repeat: repeat-x, repeat-y;
// 預設情況下，不寫background-repeat就是X與Y軸都重複出現，背景圖片自動佔滿整個畫面。
}


	第二，漸層（Gradients）。CSS3也提供漸層的效果
	2-1，線性漸層（linear gradient）。
	2-2，放射漸層（radial gradient）。從中央點「對外放射」出來的漸層效果。
10-4-3  CSS3的轉換（transforms）效果
	CSS3的transforms效果分成2D與3D兩種。

		translate3d(x, y, z)用來做3D效果。範例如下。
transform: translate3d(10px, 50px, 10px);

		translate2d(x, y)用來做2D效果。

10-4-4  CSS3的繪圖（繪製形狀）
	HTML:
	<div id='square'></div>


	CSS:
	#square {  // 方形
	width: 200px;
	height: 200px;
	background: blue;
	}


第十二章  
使用 HTML5 APIs
建構互動網頁
HTML5、CSS、JavaScript 網頁程式設計與 MCSD 70-480 認證教材
 (碁峰出版)



12-1  與檔案互動的HTML5 File API
	HTML5 File API重點介面（interface）如下：
	Blob介面是一種不可變的（immutable）原始資料（raw data，或二進位的原始資料），一個Blob是一種定義資料型態的type屬性，例如網頁常見的text/plain代表純文字。
	File介面，唯讀的資訊屬性，繼承自Blob，只有兩個屬性：檔名（name）屬性與檔案修改日期（lastModifiedDate）屬性
	FileList介面，可選取多個檔案（File）物件，例如檔案上傳時<input type=”file”>可以一次選取多個檔案。或是使用drop事件，讓使用者以拖拉（drag-and-drop）的方式與網頁互動。
	FileReader介面，應用程式可以讀取一個檔案、或是讀取一個Blob到JavaScript變數裡面。
	URL Scheme介面（W3C網站有提到，微軟教材沒提到），使用二進位的資料（例如檔案）並作為網頁程式的參考。
12-1-1  讀取文字檔    範例 01_API_TextFile.html。

<input type="file" id="theTextFile" onchange="onLoadTextFile()" />
<textarea id="theMessageArea" rows="30" cols="40"></textarea>

function onLoadTextFile() {
var theFile = document.getElementById("theTextFile");
if (theFile.files.length != 0 && theFile.files[0].type.match(/text.*/))   {
    var reader = new FileReader();
    reader.onload = function(e) {
        var MessageArea = document.getElementById("theMessageArea");
        MessageArea.value = e.target.result;
    };
    reader.onerror = function(e){
    alert("例外狀況，無法讀取文字檔");
    };
    reader.readAsText(theFile.files[0], "ISO-8859-1");
} 
else {   //… 省略…  }
}


	12-1-2  讀取二進位檔（如：圖片）
	FileReader的 .readAsDataURL()方法可以從使用者的系統讀取一份二進位檔（圖片檔也是一種二進位格式）。範例與上一個雷同，只有讀取檔案的那一段有差異。範例02_API_BinaryFile.html。

	12-1-3  整合拖拉（drag-and-drop）的行為
	HTML5支援拖拉的行為，讓使用者與網頁的互動更為緊密。要讓元素可使用拖拉必須依循下列作法：
1.	設定draggable屬性為true。
2.	設定dragstart事件。
3.	在事件（Event）物件的dadaTransfer屬性設定拖拉的時候，資料傳遞的資訊給DataTransfer物件。

12-2  與多媒體的整合，<video>標籤
	HTML5提供新的<video>標籤讓您在網頁裡面就能播放影片，而不需要外掛軟體（plug-in），這是HTML5的原生功能，對於平板、智慧手機等行動周邊更有效益。

	播放一段MP4檔案的寫法，如同<img>請把多媒體檔案的目錄（路徑）與檔名寫在src屬性裡面：
<video src="MyVideo.mp4"></video>


	12-2-1  <video>的<source>標籤可支援多種影片格式
	但為了增加相容性，建議您在<video>標籤裡面加上<source>標籤來支援多種影片格式。
	src屬性，如同<img>請把多媒體檔案的目錄（路徑）與檔名。
	type屬性，定義影片的MIME型態，例如 video/mp4、video/webm。

	12-2-2  以JavaScript程式碼與影片互動
function createVideoElement(nameOfVideoFile) {
// 創建一個 video物件並為它設定屬性。
var newVideo = document.createElement("video");

newVideo.src = nameOfVideoFile;
newVideo.loop = true;
newVideo.autoplay = true;
newVideo.controls = true;
newVideo.poster = "ImageLoading.png";

// 在現有網頁內，加入video物件。
var hostElem = document.getElementById("videoDir");
hostElem.appendChild(newVideo);
}
12-4  對應瀏覽器的位置與Context
	12-4-1  HTML5 Geolocation API（地理位置API）

	行動周邊可以依循下面的技術來判別當下的地理位置：
	IP Address。
	GPS定位（positioning）。
	Wi-Fi無線網路。
	行動電話（手機）位置。
	使用者位置（user-defined location）。


12-4-2  接收（Request）地理位置的資訊
	HTML5 Geolocation API支援兩種位置要求：
	One-shot position request。
使用.navigator.geolocation.getCurrentPosition()方法。

	Requested position updates。
使用.navigator.geolocation.watchPosition()方法開始接受位置的更新。此方法回傳回一個watch ID的值。

	範例Geolocation_API.html執行成果，如右圖。
12-4-3  處理（Process）地理位置的資訊
	上一小節提到的兩個方法，.getCurrentPosition()方法與 .watchPosition()方法。

	Call-back功能都有一個coords屬性，其中包含下面三者的座標資訊（coordinate information）：
	latitude。緯度，單位：度（degree）。
	longitude。經度，單位：度。
	Accuracy。精準度，單位：公尺（meter）。

12-4-5  檢測網頁的Context
	HTML5提供了畫面能見度的API（Page Visibility API）讓您決定頁面（網頁）是否該出現在畫面上。

	Page Visibility API有兩個屬性、一個事件：
	document.hidden屬性。
	document.visibilityState屬性。
	visibilitychange事件，只要上述屬性的visibility state更改，這個事件就會被觸發。
12-4-6  Case Study -- 搭配Google Map
	源自w3School的範例（Geolocation_API_GoogleMap.html），搭配Google Map偵測您的所在位置（http://www.w3schools.com/html/html5_geolocation.asp ）。

	下圖偵測到的地理位置，其實是我上網的ISP業者的公司位置。
	範例Geolocation_API_GoogleMap.html執行成果

13-5  網頁應用程式的除錯與分析
	13-5-1  IE瀏覽器的F12開發者工具
