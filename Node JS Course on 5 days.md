# JavaScript Fundamentals
## Các khái niệm cần tìm hiểu
-	Thế nào là biến, thế nào là Array 
http://kipalog.com/posts/var--let-va-const-trong-ES6 
-	Thế nào là Object 
http://freetuts.net/doi-tuong-object-trong-javascript-408.html 
-	Thế nào là Function 
http://freetuts.net/ham-va-tao-ham-function-trong-javascript-274.html 
-	Thế nào là Events
https://techmaster.vn/posts/33416/hoc-lap-trinh-web-javascript 
-	Thế nào là Blocking và Unblocking
http://devpro.edu.vn/tim-hieu-ve-blocking-va-non-blocking/ 
-	Thế nào là prototype 
http://kipalog.com/posts/prototype-la-khi-gi- 

## Hướng dẫn
Xem các Videos tại đây
https://drive.google.com/open?id=0B_qqD6vAQe0WcDVfTndmdFhBRUk
# NodeJS Fundamentals
Các khái niệm cần tìm hiểu
-	Thế nào là npm
-	Thế nào là package.json
-	Tài liệu: https://blog.risingstack.com/node-hero-npm-tutorial/
## Hướng dẫn
Để bắt đầu một dự án với NodeJS, ta chạy lệnh:
```sh
$ npm init
```
Sau đó tạo ra file index.js với nội dung
```javascript
'use strict'
console.log('Hello NodeJS');
```
Từ đây ta có thể chạy chương trình:
```sh
$ node .
```
> _Lưu ý_: trên đầu mỗi file .js nên sử dụng ‘use strict’.

## Cài đặt một module mới bằng npm
Cài đặt module node.js lên hệ điều hành
```sh
$ npm install -g strongloop
```
Cài đặt module node.js lên ứng dụng đang làm việc
```sh
$ npm install async --save
```
Nếu bạn đã khai báo danh sách các module trong _package.json_, bạn có thể cài đặt các module này như sau
```sh
$ npm install
```
Bài tập
Clone dự án từ đây về: git@github.com:vietvuhoang/NodeJSHelloWorld.git .
Bạn có thể tìm thấy file _members.json_ trong folder data 
```json
{
    "members" : [
        {
            "name" : "Hoang Do Manh",
            "username" : "hoangdm",
            "birthday" : "1993-10-08",
            "email": "hoangdm@vsii.com",
            "sex" : true,
            "department" : "JPD"
        },{
            "name" : "Quang Dinh Van",
            "username" : "quangdv",
            "birthday" : "1986-07-27",
            "email": "quangdv@vsii.com",
            "sex" : true,
            "department" : "SDC"
        },{
            "name" : "Nhai Vu Thi",
            "username" : "nhaivt",
            "birthday" : "1993-03-08",
            "email": "nhaivt@vsii.com",
            "sex" : false,
            "department" : "JPD"
        },{
            "name" : "Viet Vu Hoang",
            "username" : "vietvh",
            "birthday" : "1983-11-12",
            "email": "vietvh@vsii.com",
            "sex" : true,
            "department" : "IPC"
        },{
            "name" : "Dat Tran Sy",
            "username" : "datts",
            "birthday" : "1993-04-01",
            "email": "datts@vsii.com",
            "sex" : false,
            "department" : "ITD"
        },{
            "name" : "Luan Ngo Quang",
            "luannq" : "datts",
            "birthday" : "1993-10-19",
            "email": "luannq@vsii.com",
            "sex" : true,
            "department" : "JPD"
        }
    ]
}
```
Chúng ta bắt đầu từ đây.
Hãy làm các công việc sau: 
-	Viết function in ra tất cả các thành viên ra console, bao gồm: tên, ngày sinh, giới tính, phòng ban
> Đặt ‘use strict’ lên đầu tất cả các file .js

-	Viết chương trình tìm kiếm một thành viên theo username và in ra màn hình.
> Mỗi yêu cầu được viết trong một Function
> Nên tách việc in thành viên ra màn hình console thành một function độc lập

-	Sắp xếp các thành viên theo tên và in kết quả ra màn hình.
-	Đảo ngược danh sách thành viên và in ra màn hình.
-	Tách các hàm thực hiện việc in ra console, tìm kiếm, sắp xếp, đảo ngược thành một file riêng có tên students.js, file này sẽ được sử dụng như một module riêng biệt, và index.js sẽ sử dụng các hàm này từ students.js 
> Sử dụng module.exports cho việc tách các hàm ra thành một module riêng.
# ExpressJS Framework
## ExpressJS là gì
Các bạn cần đọc tài liệu về ExpressJS Framework tại đây:
http://expressjs.com/en/starter/installing.html
### Cài đặt ExpressJS
Cài đặt Express Framework
```sh
$ npm install express --save
```
Cài đặt Express Generator 
```sh
$ npm install express-generator -g
```
Tham khảo tại đây để biết về Express Generator http://expressjs.com/en/starter/generator.html 
## Bài tập
Viết ứng dụng Web bằng Express có các chức năng như sau:
-	Liệt kê tất cả tên các members trong file data/members.js ra trang http://localhost:3000/ ở dạng đã sắp xếp theo tên. ( Sử dụng module members.js đã được viết ở phần trước).
-	Với mỗi member, tên sẽ được thể hiện ở dạng link như sau: Vu Hoang Viet cho phép nhảy đến trang http://localhost:3000/user/vietvh 
-	Trang http://localhost:3000/user/vietvh thể hiện details của member được chọn ra màn hình.
# Loopback Framework 
## Loopback Framework là gì
Đọc các tài liệu tại đây
- http://loopback.io/getting-started/
- https://docs.strongloop.com/display/public/LB/LoopBack
## Bắt đầu một dự án Loopback
### Cài đặt StrongLoop
 ```sh
$ npm install -g strongloop
```
### Tạo một dự án với LoopBack Framework
 ```sh
$ slc loopback HelloLoopback
```
### Tạo Data-Source
 ```sh
$ slc loopback:datasource HelloLoopback
```
### Tạo các models 
```sh
$ slc loopback:model YourModel
```
### Tạo các relationships 
 ```sh
$ slc loopback:relation
```
Như tất các các Framework ORM khác, Loopback hỗ trợ các loại relationships sau:
-	Belongs To 
-	Has One
-	Has Many
-	Has May Through 
-	Has And Belongs To Many
Bài viết về các dạng Relationship này tại đây. 
## Kết nối với Database 
Bạn có thể sử dụng loại Database In-memory db được Loopback hỗ trợ sẵn, hoặc sử dụng bất cứ loại cơ sở dữ liệu nào bạn muốn
### PostgreSQL
Với PostgreSQL, bạn cần cài đặt module Loopback PosgreSQL Connector như sau:
```sh
$ npm install loopback-connector-postgresql --save
```
File server/datasources.json cho PostgreSQL 
```json
{
  "JRSP": {
    "host": "DBHOST",
    "port": 5432,
    "url": "",
    "database": "DBNAME",
    "password": "DBPASS",
    "name": "JRSP",
    "user": "DBUSER",
    "connector": "postgresql"
  }
}
```
MySQL 
Với MySQL, bạn cần cài đặt module Loopback MySQL Connector như sau:
```sh
$ npm install loopback-connector-mysql --save
```
File server/datasources.json cho MySQL 
```json
{
  "JRSP": {
    "host": "localhost",
    "port": 3306,
    "url": "",
    "database": "DBNAME",
    "password": "PASSWORD",
    "name": "JRSP",
    "user": "root",
    "connector": "mysql"
  }
}
```
## Callback và Async 
Trong NodeJS, do phương pháp non-blocking thường xuyên được sử dụng, chúng ta sẽ nhận dữ liệu được trả về qua các hàm callback thay vì return value.

Hãy xem ví dụ sau đây : 
```javascript
    let filter = {
      where : {
        username : username
      }
    };

    Member.find( username, function( err, members ) {
      // Do something with asynchronous mecharism  
    })
```
 
Như vậy rất dễ gặp phải trường hợp ta sử dụng các hàm callback lồng nhau, trường hợp này được gọi là Callback Hell.
Khái niệm về Callback Hell được nói rõ hơn trong bài viết sau: http://kipalog.com/posts/Callback-la-khi-gi- 
Để tránh Callback Hell, có 2 phương pháp thường được sử dụng:
-	Promise : http://kipalog.com/posts/Promise-la-khi-gi- 
-	Async : https://github.com/caolan/async 
Các bạn đọc thêm bài viết sau đây để hiểu hơn về Async và Promise : https://nodejs.vn/topic/15/promise-async-th%C3%AC-sao-n%C3%A0o 

Tôi có một bài viết ngắn về cách sử dụng Async ở đây. 
## Auto Migrate và Auto Update
Với Loopback, để install dữ liệu vào cơ sở dữ liệu, bao gồm:
-	Cài đặt các bảng từ các models
-	Cập nhật các thay đổi trong bảng
-	Chuẩn bị dữ liệu cho ứng dụng
Ta có 2 cách thực hiện các việc trên: Auto Migrate và Auto Update 
### Auto Migrate
Auto Migrate xóa bỏ toàn bộc các bảng trong cơ sở dữ liệu và tạo lại các bản mới. Sử dụng Auto Migrate bạn sẽ mất toàn bộ dữ liệu đang có.
https://docs.strongloop.com/display/public/LB/Creating+a+database+schema+from+models#Creatingadatabaseschemafrommodels-Auto-migrate
```javascript
'use strict';
var app = require("../server/server");
var ds = app.datasources.HelloLoopBack
ds.automigrate( function(err) {
    ds.disconnect();
    process.exit( 0 );
});
```
### Auto Update
Khác với Auto Migrate, Auto Update chỉ cập nhât những thay đổi trong các bảng hoặc tạo ra các bảng chưa có, dữ liệu của bạn sẽ không bị mất.
https://docs.strongloop.com/display/public/LB/Creating+a+database+schema+from+models#Creatingadatabaseschemafrommodels-Auto-update
 ```javascript
'use strict';
var app = require("../server/server");
var ds = app.datasources.HelloLoopBack
ds.autoupdate( function(err) {
    ds.disconnect();
    process.exit( 0 );
});
```
## Bài Tập
### Thiết kế Database đáp ứng các yêu cầu sau: 
-	Ứng dụng quản lý các Members trong công ty VietSoftware Inc. International 
-	Mỗi Member có các thông tin :
o	Name
o	Birthday
o	Username
o	Email 
o	Sex
-	Mỗi thành viên thuộc một Department, và ngược lại mỗi Department có nhiều thành viên
-	Mỗi Department có một Manager cũng là một Member trong công ty,
-	Mỗi Member được quản lý bởi một Manager ( Manager này có thể không phải là Manager của Department )
-	Mỗi Manager có nhiều Members dưới sự quản lý của mình.
-	Mỗi thành viên có thể tham gia các nhóm hoạt động trong công ty ( Group ), các nhóm này có thể là :
o	Đội Bóng đá
o	Đội Cầu Lông
o	Đội Bóng Bàn
o	Đội Technical Support 
o	… 
-	Mỗi Đội có nhiều thành viên tham gia.

> Vẽ mối quan hệ CSDL bằng công cụ http://draw.io/ và export ra dạng hình ảnh.

## Sử dụng các lệnh LoopBack để cài đăt Database đã thiết kế
```sh
$ slc loopback:model YourModel
``` 
 ```sh
$ slc loopback:relation
```
### Sử dụng PostgreSQL là hệ quản trị Database
### Viết chương trình Auto Migrate và Auto Update để cài đặt dữ liệu trong 2 files sau đây vào DataBase :
- data/members.json 
- data/groups.json

> Sử dụng thư viện Promise hoặc Async để tránh Callback Hell. Đây là yêu cầu bắt buộc






