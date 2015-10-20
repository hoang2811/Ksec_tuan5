###I.VirtualHost
Là tính năng cua Apache gúp ta duy trì nhiều hơn một web server trên một máy tính. Nhiều tên cùng chia sẻ một địa chỉ IP gọi là named-based virtual hosting, và sử dụng những đại chỉ IP khác nhau cho từng domain gọi là IP-based virtual hosting.
####1.IP-based VirtualHost
VirtualHost dựa trên IP yêu cầu những server phải có một địa chỉ IP khác nhau cho mỗi virtualhost dựa trên IP. Như vậy, một máy tính phải có nhiều interface hay sử dụng cơ chế virtual interface mà những hệ điều hành sau này hỗ trợ.
####2. Name-based Virtual Hosts
IP-based VirtualHost dựa vào địa chỉ IP để quyết định VirtualHost nào đúng để truy cập. Vì thế, bạn cần phải có địa chỉ IP khác nhau cho mỗi VirtualHost. Với Name-based VirtualHost, server dựa vào HTTP header của client để biết được hostname. Sử dụng kỹ thuật này, một địa chỉ IP có thể có nhiều tên máy tính khác nhau. Name-based VirtualHost rất đơn giản, bạn chỉ cần cấu hình DNS sao cho nó phân giải mỗi tên máy đúng với một địa chỉ IP và sau đó cấu hình Apache để tổ chức những web server cho những miền khác nhau.

###II. Thêm VirtualHost (thêm domain) vào Apache trên Ubuntu
- Trước tiên, chúng ta cũng cần tạo cho nó một thư mục chứa dữ liệu cho domain cần thêm vào.

![](http://imgur.com/fyD4KsZ.png)

- Vào thư mục /etc/apache2/sites-available/ để xem có những file gì.
![](http://imgur.com/uZNQKDp.png)

- Sau đó chúng ta cần copy file /etc/apache2/sites-available/000-default.conf ra một file mới chứa cấu hình của domain cần thêm vào (hoang2811.com) ở /etc/apache2/sites-available/hoang2811.com.conf.

![](http://imgur.com/Q0MMufi.png)

- Bây giờ hãy mở file /etc/apache2/sites-available/hoang2811.com.conf lên 

![](http://imgur.com/7AOojna.png)

và sửa nội dung trong đó cho nó gọn hơn như thế này:

![](http://imgur.com/4FkQkYv.png)

- Nhớ thay:

  + **SererName** – Domain website cần thêm vào.

  + **ServerAlias** – Sử dụng một tên domain khác thay thế, hay còn gọi là Parked Domain nếu bạn đã từng sử dụng qua cPanel đó.

  + **DocumentRoot** – Đường dẫn tới thư mục chứa dữ liệu website của domain này mà ta đã tạo ở trên.

  + **ErrorLog** – Đường dẫn tới thư mục log đã tạo ở trên cho domain này.

  + **CustomLog** – Tương tự ErrorLog nhưng sẽ lưu log lại các lượt truy cập với file là access.log.

- Sau đó chúng ta gõ lệnh sau để nó tự động tạo ra một symlink của file này vào thư mục sites-enabled để bật nó lên.

![](http://imgur.com/hzhFTcB.png)

Hãy nhớ rằng, hoang2811.com.conf là tên file cấu hình trong thư mục sites-available đã bỏ đuôi .conf.

- Kết quả trả về:
![](http://imgur.com/bKTr6bb.png)

- Gõ lệnh sau để khởi động lại Apache.
![](http://imgur.com/oXJgeyK.png)

- Tạo một trang sample cho Virtual Hosts


Save và đóng lại.

- Kiểm tra Virtual Hosts

Sửa đổi file host: /etc/hosts

sudo vi /etc/hosts
Và thêm vào domain

[...]
192.168.1.100   nguyenandfriend.wordpress.com
Sau đó Save và đóng file lại.



