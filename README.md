# mysql-server


## 什麼是mysql
一種資料庫
## 實作步驟
- Step-1 更新套件
```
 sudo apt update 
```
- Step-2 安裝mysql-server 
```
 sudo apt install mysql-server
```
- Step-3 檢查mysql狀態 
```
 sudo service mysql status
```
- Step-4 登入mysql 
```
 sudo mysql -u root

```
- Step-5 查看mysql伺服器中所有資料 
```
 SHOW DATABASES;
``` 
- Step-6 建立名為dbname的資料庫
```
 CREATE DATABASE `dbname`;
```
- Step-7 進入名為dbname的資料庫
```
 USE `dbname`;
```
- Step-8 建立表格 
以下SQL敘述，可以建立名為users的表格，這個表格有兩個欄位。
第一個欄位是userid，儲存的資料型別是tinyint SIGNED(有號8-bit整數)，必須NOT NULL(不能是空的)，且作為每列(row)資料的PRIMARY KEY(主鍵)，會AUTO_INCREMENT(自動遞增)。
第二個欄位是username，儲存的資料型別是varchar(50)(最大可以存50個字元)。
```
 CREATE TABLE `users` (
     `userid` tinyint SIGNED NOT NULL PRIMARY KEY AUTO_INCREMENT,
     `username` varchar(50)
);
```
- Step-9  插入學號至users表格中
```
 INSERT INTO `users` (`username`)
     VALUES ('學號');
```
- Step-10  查詢users表格中的資料
```
 SELECT * FROM `users`;
```
- Step-11 退出mysql 
```
 quit
```
