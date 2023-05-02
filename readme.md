- NoSQL
- database hướng tài liệu (document), các dữ liệu được lưu trữ trong document kiểu JSON thay vì dạng bảng như CSDL quan hệ nên truy vấn sẽ rất nhanh
- So với RDBMS thì trong MongoDB collection ứng với table, còn document sẽ ứng với row
- Trường dữ liệu “_id” luôn được tự động đánh index (chỉ mục) để tốc độ truy vấn thông tin đạt hiệu suất cao nhất
- Một số câu lệnh cơ bản trên MongoDB
CSDL	        MySQL	                                                            MongoDB
Tạo csdl	    CREATE DATABASE test;	                                            use test;
Tạo bảng	    CREATE TABLE students (ten_cot - kieu_du_lieu);	                    db.createCollection('students');
Tạo bản ghi	    INSERT INTO studetns ('name', 'gender') VALUES('nguyen', 'male');	db.students.insert({ name:'nguyen', gender: 'male'});
Cập nhật	    UPDATE students SET name = 'nguyen update' WHERE id = 1;	            db.students.update({ _id: 1 },{$set:{ name: 'nguyen update' }});
Xóa bản ghi	    DELETE FROM students Where id = 1;	                                db.students.remove({ _id: 1});
Tìm kiếm all	SELECT * FROM students;	                                            db.students.find({});
Tìm kiếm	    SELECT * FROM students WHERE name = 'nguyen';	                    db.students