####Cấu trúc thư mục cấu hình Apache trên Ubuntu

Mặc định trên Ubuntu, thư mục chứa các thiết lập của Apache sẽ nằm trong thư mục /etc/apache2. 
Ta dùng lệnh cd di chuyển vào thư mục đó, rồi dùng lệnh `ls -lh` để xem một số thư mục và file cấu hình như sau:

![](http://imgur.com/CELdMVb.png)

**`conf-available/`** – Thư mục này sẽ chứa các file thiết lập cấu hình sẵn của Apache trên Ubuntu, nhưng các thiết lập trong đây sẽ chưa được áp dụng vì Ubuntu không load thiết lập cấu hình trong thư mục này. <br>
**`conf-enabled/`** – Thư mục chứa các file thiết lập cấu hình của Apache trên Ubuntu đang được bật. Hãy hiểu là nếu thư mục này có một liên kết tượng trưng (symlink) qua một file module nào đó bên thư mục conf-available thì nó sẽ được bật. <br>
**`mods-available/`** – Thư mục chứa các file từng module của Apache trên Ubuntu nhưng chưa được bật. <br>
**`mods-enabled/`** – Thư mục chứa các file từng module của Apache trên Ubuntu đang được bật. <br>
**`site-available/`** – Thư mục chứa file cấu hình VirtualHost của Apache trên Ubuntu nhưng chưa được bật. <br>
**`site-enabled/`** – Thư mục chứa file cấu hình VirtualHost của Apache trên Ubuntu đang được bật. <br>
**`apache2.conf`** – File cấu hình Apache trên Ubuntu. <br>
**`envvars`** – File thiết lập các biến với giá trị sẵn để sử dụng trong các file cấu hình. <br>
**`magic`** – File thiết lập của module mod_mime_magic trên Apache. <br>
**`ports.conf`** – File cấu hình cổng mạng của Apache (mặc định là port 80).
