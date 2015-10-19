####Các module của Apache

Mặc định, sau khi cài đặt, trong Apache có đi kèm sẵn một số module để thực thi nhiệm vụ của một web server. Các module này, xếp theo thứ tự từng giai đoạn xử lý bao gồm:

#####Chuyển đổi giữa URI thành filename trên server

*Mod_userdir*: chuyển thư mục home cho từng user. <br>
*Mod_rewrite*: điều chỉnh lại đường dẫn URL.

#####Giai đoạn Xác thực / phân quyền

*mod_auth, mod_auth_anon,mod_auth_db, mod_auth_dbm*: các kiểu xác thực người dùng. <br>
*Mod_access*: kiểm soát truy nhập theo từng host.

#####Xác định MIME của đối tượng được truy vấn

*mod_mime*: xác định loại file bằng cách dựa vào phần mở rộng. <br>
*mod_mime_magic*: xác định loại file bằng cách sử dụng “magic number”

#####Chỉnh sửa đường dẫn

*Mod_alias*: thay thế alias bằng đường dẫn thực trên server. <br>
*Mod_env*: thay đổi các tham số hệ thống dựa trên thông tin trong file cấu hình. <br>
*Mod_spelling*: tự động sửa lỗi trong URL.

#####Gửi trả lại dữ liệu cho client

*Mod_actions*: các script cho từng loại file sẽ được thực thi. <br>
*Mod_asis*: gửi file nguyên dạng <br>
*Mod_autoinde**: <br>
*Mod_cgi*: gọi script CGI và trả lại kết quả. <br>
*Mod_include**: <br>
*Mod_dir*: xử lý về thư mục <br>
*Mod_imap*: xử lý image-map files. <br>

#####Ghi log

Mod_log_*: các module log khác nhau.

####Các module quan trọng đối với Apache Server

*httpd_core*: Chứa các chức năng cốt lõi của Apache, cần thiết cho bất cứ Apache nào.

*mod_access*: Cung cấp chế độ khiển tác dựa trên tên máy, địa chỉ IP, hoặc các tính chất yêu cầu thuộc về các clients. Bởi vì module này cần cho các chỉ phối (directive) “order”, “allow” và “deny”, nó cần được cho phép.

*mod_auth*: Cần thiết để ứng dụng vấn đề khai báo người dùng cho việc sử dụng các hồ sơ nguyên bản (khai báo căn bản cho HTTP), được chỉ định trong chức năng trù bị.

*mod_dir*: Cần thiết để tìm kiếm và phục vụ các hồ sơ thư mục: “index.html”, “default.htm”, v..v..

*mod_log_config*: Cần thiết để ứng hiệu báo cáo những yêu cầu thực hiện đến server.

*mod_mime*: Cần thiết để chỉnh lý nhóm chữ cái, mã hoá nội dung, tùy tác ngôn ngữ nội dung và các loại MIME đại diện cho các loại tài liệu.

Module **httpd_core**: Module này đóng vai trò đảm nhiệm các chức năng chính của Web Server. 

**Các Directive bao gồm:**

- DefaultType <br>
- DocumentRoot <br>
- MaxClients <br>
- Modules <br>
- Port <br>
- ServerAdmin <br>
- ServerName <br>
- ServerRoot <br>
- SocketType <br>
- SSLCertificateFile <br>
- SSLCertificateKeyFile <br>
- SSLVerifyClient <br>
