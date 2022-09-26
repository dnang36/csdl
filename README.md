# Cơ sở dữ liệu

## Đề bài: Tìm hiểu về csdl

### Thực hiện bởi: [Nguyễn Đoàn Đăng](https://github.com/dnang36)

### Download code và run code tại đường dẫn https://github.com/dnang36/csdl

### Kiến thức thu được:

## 1.DBMS:
- DBMS là viết tắt của Database Management System, dịch sang tiếng Việt là Hệ quản trị Cơ sở dữ liệu. DBMS là phần mềm được thiết kế để có thể xác định, tiến hành các thao tác, truy xuất và quản lý dữ liệu trong Cơ sở dữ liệu
- DBMS thường có khả năng tự thao tác với dữ liệu, định dạng dữ liệu, tên trường, cấu trúc bản ghi và cấu trúc tệp. Nó cũng xác định các quy tắc để xác nhận và thao tác với dữ liệu.
- Với DBMS, người dùng có thể thao tác sửa/xóa/thêm dữ liệu mà không còn cần các chương trình khung. Các ngôn ngữ lập trình truy vấn như SQL thường đi kèm với DBMS để lập trình viên dễ dàng tương tác với dữ liệu họ cần.
- Một vài DBMS phổ biến:
  - MySQL
  - SQL Server
  - Oracle
  - dBASE
  - Fox
## 2.SQL
- Viết tắt của Structured Query Language là ngôn ngữ truy vấn có cấu trúc. Nó là một ngôn ngữ, là tập hợp các lệnh để tương tác với cơ sở dữ liệu. Dùng để lưu trữ, thao tác và truy xuất dữ liệu được lưu trữ trong một cơ sở dữ liệu quan hệ.
- SQL là ngôn ngữ chuẩn được sử dụng hầu hết cho hệ quản trị cơ sở dữ liệu.
- Các kiểu dữ liệu trong SQL:

| kiểu dữ liệu  | Tên                              | Ví Dụ                                                                                                                    |
|---------------|----------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| int           | Số Nguyên                        | VD:3;6;8                                                                                                                 |
| float         | Số Thực                          | VD:3.6;1.2                                                                                                               |
| varchar(size) | Chuỗi                            | Giả sử varchar(50) thì chuỗi tối đa có 50 kí tự (do máy cấp), nhưng nếu không dùng hết thì máy sẽ tự rút ngắn bộ nhớ lại |
| boolean       | kiểu đúng sai                    | Có 2 giá trị: 1 và 0                                                                                                     |
| text          | chuỗi                            | Là chuỗi nhưng cho văn bản dài, không cần khai báo có bao nhiêu kí tự                                                    |
| date          | năm - tháng - ngày               | VD: 2018 - 01 - 01                                                                                                       |
| datetime      | năm - tháng - ngày giờ:phút:giây | VD: 2018 - 01 - 01 23:59:59                                                                                              |
| time          | giờ:phút:giây                    | VD: 23:59:59                                                                                                             |

- Các mối quan hệ trong SQL: được sử dụng để mô tả các mối quan hệ tồn tại giữa các bảng trong cơ sở dữ liệu quan hệ.
  - quan hệ một - một: Mối quan hệ một-một trong cơ sở dữ liệu xảy ra khi mỗi hàng trong bảng 1 chỉ có một hàng liên quan trong bảng 2.
  - quan hệ một - nhiều: Mối quan hệ một-nhiều xảy ra khi một bản ghi trong bảng 1 có liên quan đến một hoặc nhiều bản ghi trong bảng 2. Tuy nhiên, một bản ghi trong bảng 2 không thể liên quan đến nhiều hơn một bản ghi trong bảng 1
  - quan hệ nhiều - nhiều: Mối quan hệ nhiều-nhiều xảy ra khi nhiều bản ghi trong một bảng có liên quan đến nhiều bản ghi trong bảng khác.

- Hàm tổng hợp dữ liệu (Aggregate Functions) trong SQl:là một hàm trong đó các giá trị của nhiều hàng được gom nhóm lại với nhau để làm đầu vào cho các tiêu chí nhất định để tạo thành một giá trị duy nhất có ý nghĩa quan trọng hơn. 
  - COUNT: đếm số lượng bản ghi,
  - SUM: được sử dụng để tính tổng của một trường trong các bản ghi khác nhau.
  - AVG: được sử dụng để tính giá trị trung bình của một trường trong các bản ghi khác nhau.
  - MIN: được sử dụng để tìm ra bản ghi có giá trị nhỏ nhất trong một tập hợp bản ghi.
  - MAX: được sử dụng để tìm ra bản ghi có giá trị lớn nhất trong một tập hợp bản ghi.

- Các câu lệnh SQL(query): Các lệnh SQL tiêu chuẩn để tương tác với cơ sở dữ liệu quan hệ là CREATE, SELECT, INSERT, UPDATE, DELETE và DROP. Các lệnh này có thể được phân thành các nhóm sau dựa trên bản chất của chúng
  - DDL(Ngôn ngữ định nghĩa dữ liệu):

| Lệnh   | Mô tả                                                                |
|--------|----------------------------------------------------------------------|
| CREATE | Tạo ra một bảng mới hoặc các đối tượng khác trong cơ sở dữ liệu.     |
| ALTER  | Sửa đổi một đối tượng cơ sở dữ liệu hiện có, chẳng hạn như một bảng. |
| DROP   | Xoá toàn bộ một bảng hoặc các đối tượng khác trong cơ sở dữ liệu.    |

  - DML(Ngôn ngữ thao tác dữ liệu) :

| Lệnh   | Mô tả                                                 |
|--------|-------------------------------------------------------|
| SELECT | Lấy ra các bảng ghi nhất định từ một hoặc nhiều bảng. | 
| INSERT | Tạo một bảng ghi..                                    |
| UPDATE | Chỉnh sửa bảng ghi.                                   |
| DELETE | Xóa bảng ghi.                                         |

- Truy vấn con (Subquery): Một truy vấn con là một truy vấn được chứa trong một truy vấn khác. Truy vấn bên trong thường được sử dụng để xác định kết quả của truy vấn bên ngoài.
- Transaction SQL :là tiến trình thực hiện một nhóm các câu lệnh SQL. Các câu lệnh này được thực thi một cách tuần tự và độc lập. Một Transaction được thực hiện thành công khi tất cả câu lệnh đều thành công, khi đó tất cả các thay đổi dữ liệu được thực hiện trong Transaction được lưu vào cơ sở dữ liệu. Tuy nhiên, nếu chỉ một trong số đó thất bại thì toàn bộ tiến trình sẽ thất bại, đồng nghĩa với việc dữ liệu phải rollback về trạng thái ban đầu (dữ liệu được khôi phục về trạng thái trước khi thực hiện Transaction).
  - COMMIT: để lưu các thay đổi.
  - ROLLBACK: để quay trở lại trạng thái trước khi có thay đổi.
  - SAVEPOINT: tạo các điểm (point) bên trong các nhóm Transaction để ROLLBACK, tức là để quay trở lại điểm trạng thái đó.
  - SET TRANSACTION: đặt một tên cho một Transaction.

3. NoSQL
