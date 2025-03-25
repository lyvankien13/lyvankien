# lyvankien
Bài tập về nhà 02 của sv: K225480106101 - Lý Văn Kiên - Môn Hệ Quản Trị CSDL
DEADLINE: 23H59 NGÀY 25/03/2025

ĐIỀU KIỆN: (ĐÃ LÀM XONG BÀI 1)
1. Đã cài đặt SQL Server 2022 Dev.
2. Đã cài đặt SQL Managerment Studio bản mới nhất.
3. Đã kết nối từ SQL Managerment Studio vào SQL Server.
4. Đã có tài khoản github, biết cách tạo repository(kho lưu trữ) cho phép truy cập public.

BÀI TOÁN:
- Tạo csdl quan hệ với tên QLSV gồm các bảng sau:
  + SinhVien(#masv,hoten,NgaySinh)
  + Lop(#maLop,tenLop)
  + GVCN(#@maLop,#@magv,#HK,)
  + LopSV(#@maLop,#@maSV,ChucVu)
  + GiaoVien(#magv,hoten,NgaySinh,@maBM)
  + BoMon(#MaBM,tenBM,@maKhoa)
  + Khoa(#maKhoa,tenKhoa)
  + MonHoc(#mamon,Tenmon,STC)
  + LopHP(#maLopHP,TenLopHP,HK,@maMon,@maGV)
  + DKMH(#@maLopHP,#@maSV,DiemTP,DiemThi,PhanTramThi)

YÊU CẦU:
1. Thực hiện các hành động sau trên giao diện đồ hoạ để tạo cơ sở dữ liệu cho bài toán:
  + Tạo database mới, mô tả các tham số(nếu có) trong quá trình.
  + Tạo các bảng dữ liệu với các trường như mô tả, chọn kiểu dữ liệu phù hợp với thực tế (tự tìm hiểu)
  + Mỗi bảng cần thiết lập PK, FK(s) và CK(s) nếu cần thiết. (chú ý dấu # và @: # là chỉ PK, @ chỉ FK)
2. Chuyển các thao tác đồ hoạ trên thành lệnh SQL tương đương. lưu tất cả các lệnh SQL trong file: Script_DML.sql




****Bài làm: ****

Bước 1: Tạo cơ sở dữ liệu: 

![image](https://github.com/user-attachments/assets/7301d3b3-1a21-47ac-ac2f-6298e2b7f76d)

Bước 2: Tạo csdl với tên QLSV:

![image](https://github.com/user-attachments/assets/30f48a2d-4743-462c-865e-c94588943423)

Bước 3: Tạo các bảng:

![image](https://github.com/user-attachments/assets/8f3f2219-4e51-4ab7-80e2-67172a825a6a)

- Bảng sinh viên:
  
![image](https://github.com/user-attachments/assets/29726dcf-2694-4305-b549-711487ef549b)

- Bảng lớp:

![image](https://github.com/user-attachments/assets/57105e59-2313-4d6c-a794-caaef53b13fa)

  - Bảng Giáo VIên Chủ Nghiệm:
 
 ![image](https://github.com/user-attachments/assets/98a78a4f-ac59-4602-b1cf-3b50ad6fd271)

- Bảng Lớp sinh viên:

![image](https://github.com/user-attachments/assets/88a13a51-888e-4aa1-8158-24612f2e6d3b)

- Bảng giáo viên:

![image](https://github.com/user-attachments/assets/c7fbe02c-303c-42ee-bd6c-b34bffefc0ab)

- Bảng bộ môn:

![image](https://github.com/user-attachments/assets/dc2c59fc-df01-4fc3-851c-7cf1aa079b5b)

- Bảng khoa:

![image](https://github.com/user-attachments/assets/4d0f65c9-92f5-45f5-8006-2ac8505fd553)


- Bảng môn học:

  ![image](https://github.com/user-attachments/assets/88427df1-b43f-4f82-a7a0-2451b58e7491)

- Bảng lớp học phần:

![image](https://github.com/user-attachments/assets/8a4e1be7-e2cd-4094-a780-a6b9e0ab5dd3)

 - Bảng DKMH:

![image](https://github.com/user-attachments/assets/c218ffa8-132e-4740-af5a-d50250da511c)

Bước 4: Check constraints
- Thực hiện ràng buộc cho một số thuộc tính cần thiết:

![image](https://github.com/user-attachments/assets/4652cc1f-c038-4213-a773-f118014effe7)

- Bấm ' add'  để thêm một ràng buộc sau đó cài đặt cho ràng buộc đó:
  
![image](https://github.com/user-attachments/assets/bb30dd8e-106b-46b8-8e86-ebef54873c2f)

![image](https://github.com/user-attachments/assets/e3be6322-9620-4168-bb4e-0d53c373375c)


![image](https://github.com/user-attachments/assets/941c38d5-e782-4512-8937-4cab5a68b8d5)

Bước 5: Cài khóa chính: 
- Nhấp chuột phải vào thuộc tính cần cài làm khóa chính --> chọn Set Primary Key
- Hoặc chọn nhiều thuộc tính rồi chọn biểu tượng chìa khóa trên thanh công cụ:

![image](https://github.com/user-attachments/assets/6a234bee-4c2c-4659-8d94-142aee4acfd5)

  - Các bảng sau khi đã cài khóa chính:
    
![image](https://github.com/user-attachments/assets/7b93aa85-2ebf-4886-9717-f4afd9228bfb)

![image](https://github.com/user-attachments/assets/3d67e7d9-15d8-4fd0-8bea-128bb07723bb)

![image](https://github.com/user-attachments/assets/643fa27a-e3e0-4d67-bef6-e67217bab9a5)

![image](https://github.com/user-attachments/assets/b2c825b0-cd3c-46b7-91fb-eb082039a2ab)

![image](https://github.com/user-attachments/assets/fc85833b-016b-4d61-9878-ac2229156d99)

![image](https://github.com/user-attachments/assets/1d5b3ca4-369c-4e77-a5cc-c6b216c7a91b)

![image](https://github.com/user-attachments/assets/3ab18fe1-c4f3-418b-90eb-44d49d89184d)

![image](https://github.com/user-attachments/assets/92065eff-6d08-4c1a-98c7-00fcf0a79b3a)

![image](https://github.com/user-attachments/assets/31692c1a-8cfa-4b3f-a38e-892d03832284)

![image](https://github.com/user-attachments/assets/8385b4cc-2f2f-4717-93c1-e225b7569910)


Bước 6: Cài khóa ngoại cho các bảng theo yêu cầu: 
- Nhấp chuột phải ----> relationship...
- Bấm 'add' để thêm khóa ngoại:
  


![image](https://github.com/user-attachments/assets/c60b1433-df40-4dce-bc57-52d67cc72f2a)

![image](https://github.com/user-attachments/assets/899b80ad-a9f3-48e4-926c-600242550a99)

![image](https://github.com/user-attachments/assets/b4fb6012-0c6d-4eb7-8a03-8cbfba71429b)

![image](https://github.com/user-attachments/assets/39a224a9-829a-4143-9346-1898d0698652)

![image](https://github.com/user-attachments/assets/71902732-bc46-4178-b843-a1110dc0c0f7)

![image](https://github.com/user-attachments/assets/697c6be7-6c29-48c0-b7cf-f83f9ab16ea3)

![image](https://github.com/user-attachments/assets/bfbc71bd-0662-46e0-bd1a-ae4f919507c4)

![image](https://github.com/user-attachments/assets/4219215e-ae11-453d-ba75-e13cc5ad350f)

![image](https://github.com/user-attachments/assets/0847e4ab-b3f5-44ad-ad25-b389c7ca4726)

![image](https://github.com/user-attachments/assets/b25dd5c3-cd44-4509-90a3-3b12e31eaccd)


Bước 7: Chuyển từ thao tác đồ hoạ sang lệnh SQL: 
- Nhấp chuột phải vào Database/bảng dbo ----> Script table/database as ----> Create to -----> New query editor window


![image](https://github.com/user-attachments/assets/85b1ff50-5e79-4186-b979-3d006b16c686)

 - Ta có được lệnh SQL của các bảng và Database:

![image](https://github.com/user-attachments/assets/a1c600f8-9f9d-41fb-9f92-3a5daf5892d1)

![image](https://github.com/user-attachments/assets/c8fa657f-58b8-4227-8a94-611e92c8bf45)

![image](https://github.com/user-attachments/assets/5c4630b4-f38a-4390-b976-9db9beb01c66)

![image](https://github.com/user-attachments/assets/b953919a-e874-4e1e-8aa5-c23e6658dba0)

![image](https://github.com/user-attachments/assets/c23dee1c-279a-4f3e-aa7a-e59e81bed227)

![image](https://github.com/user-attachments/assets/a2966737-d371-400f-9428-af21c270691e)

![image](https://github.com/user-attachments/assets/df146786-f752-4da4-b5e9-f5f1e80719a3)

![image](https://github.com/user-attachments/assets/c0acf128-c30b-4730-a4d2-98c517d76949)

![image](https://github.com/user-attachments/assets/db70c87d-30be-48f6-9c52-b8ff73d5e40b)

![image](https://github.com/user-attachments/assets/8088ebca-7d4f-4b6d-aa56-09dfd015c906)

![image](https://github.com/user-attachments/assets/072767cf-6b13-4e5c-bdad-ce6f040f203c)






