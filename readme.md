- NoSQL
- database hướng tài liệu (document), các dữ liệu được lưu trữ trong document kiểu JSON thay vì dạng bảng như CSDL quan hệ nên truy vấn sẽ rất nhanh
- So với RDBMS thì trong MongoDB collection ứng với table, còn document sẽ ứng với row
- Trường dữ liệu “_id” luôn được tự động đánh index (chỉ mục) để tốc độ truy vấn thông tin đạt hiệu suất cao nhất
- Một số câu lệnh cơ bản trên MongoDB <br>
CSDL	        MySQL	                                                            MongoDB <br>
Tạo csdl	    CREATE DATABASE test;	                                            use test; <br>
Tạo bảng	    CREATE TABLE students (ten_cot - kieu_du_lieu);	                    db.createCollection('students'); <br>
Tạo bản ghi	    INSERT INTO studetns ('name', 'gender') VALUES('nguyen', 'male');	db.students.insert({ name:'nguyen', gender: 'male'}); <br>
Cập nhật	    UPDATE students SET name = 'nguyen update' WHERE id = 1;	            db.students.update({ _id: 1 },{$set:{ name: 'nguyen update' }}); <br>
Xóa bản ghi	    DELETE FROM students Where id = 1;	                                db.students.remove({ _id: 1}); <br>
Tìm kiếm all	SELECT * FROM students;	                                            db.students.find({}); <br>
Tìm kiếm	    SELECT * FROM students WHERE name = 'nguyen';	                    db.students

https://www.youtube.com/watch?v=cPzNMpkQm2o
