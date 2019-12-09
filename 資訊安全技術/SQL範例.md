# SQL
```
https://www.runoob.com/sql/sql-tutorial.html
https://www.runoob.com/mysql/mysql-tutorial.html
https://www.cnblogs.com/henryhappier/archive/2010/07/05/1771295.html
```
```
1.DDL（Data Definition Language）資料庫定義語言statements are used to define the database structure or schema.

DDL是SQL語言的四大功能之一。
用於定義資料庫的三級結構，包括外模式、概念模式、內模式及其相互之間的映射，定義資料的完整性、安全控制等約束
DDL不需要commit.
CREATE 
ALTER
DROP
TRUNCATE
COMMENT
RENAME

2.DML（Data Manipulation Language）資料操縱語言statements are used for managing data within schema objects.

由DBMS提供，用於讓用戶或程式師使用，實現對資料庫中資料的操作。
DML分成交互型DML和嵌入型DML兩類。
依據語言的級別，DML又可分成過程性DML和非過程性DML兩種。
需要commit.
SELECT
INSERT
UPDATE
DELETE
MERGE
CALL
EXPLAIN PLAN
LOCK TABLE

3.DCL（Data Control Language）資料庫控制語言  授權，角色控制等
GRANT 授權
REVOKE 取消授權

4.TCL（Transaction Control Language）事務控制語言
SAVEPOINT 設置保存點
ROLLBACK  回滾
SET TRANSACTION

SQL主要分成四部分：
（1）資料定義。（SQL DDL）用於定義SQL模式、基本表、視圖和索引的創建和撤銷操作。
（2）資料操縱。（SQL DML）資料操縱分成資料查詢和資料更新兩類。資料更新又分成插入、刪除、和修改三種操作。
（3）資料控制。包括對基本表和視圖的授權，完整性規則的描述，事務控制等內容。
（4）嵌入式SQL的使用規定。涉及到SQL語句嵌入在主機語言程式中使用的規則。

```
```
DDL---- create | drop
DML---- Insert into| update | select ...from  ... where .... order by ....   
DCL---- grant  | 

```

#
```
SET NAMES utf8;
SET FOREIGN_KEY_CHECKS = 0;

-- ----------------------------
--  Table structure for `websites`
-- ----------------------------
DROP TABLE IF EXISTS `websites`;

CREATE TABLE `websites` (
  `id` int(11) NOT NULL AUTO_INCREMENT,
  `name` char(20) NOT NULL DEFAULT '' COMMENT '網站名稱',
  `url` varchar(255) NOT NULL DEFAULT '',
  `alexa` int(11) NOT NULL DEFAULT '0' COMMENT 'Alexa 排名',
  `country` char(10) NOT NULL DEFAULT '' COMMENT '國家',
  PRIMARY KEY (`id`)
) ENGINE=InnoDB AUTO_INCREMENT=6 DEFAULT CHARSET=utf8;

-- ----------------------------
--  Records of `websites`
-- ----------------------------
BEGIN;
INSERT INTO `websites` 
VALUES ('1', 'Google', 'https://www.google.cm/', '1', 'USA'), 
       ('2', '淘寶', 'https://www.taobao.com/', '13', 'CN'), 
       ('3', '菜鳥教程', 'http://www.runoob.com/', '4689', 'CN'), 
       ('4', '微博', 'http://weibo.com/', '20', 'CN'), 
       ('5', 'Facebook', 'https://www.facebook.com/', '3', 'USA');
COMMIT;


SET FOREIGN_KEY_CHECKS = 1;
```
###
```
SELECT * 
FROM Websites;
```
