##Web Server và cách hoạt động

Ban đầu Web Server chỉ phục vụ các tài liệu HTML và hình ảnh đơn giản. Tuy nhiên, đến thời điểm hiện tại nó có thể làm nhiều hơn thế, Đầu tiên xét Web Server ở mức độ cơ bản, 
nó chỉ phục vụ các nội dung tĩnh. nghĩa là khi Web Server nhận 1 yêu cầu từ Web browser ( VD: http://www.hoang2811.com/index.html) nó sẽ ánh xạ đường dẫn này (Unifom Resource Locator - URL) 
thành một tập tin cục bộ trên máy Web Server. Máy chủ sau đó sẽ nạp tập tin này từ đĩa và đưa nó thông qua mạng đến Web Browser của người dùng. Web browser và Web Server sử dụng giao thức HTTP trong quá trình trao đổi dữ liệu. Các trang tài liệu HTML là một văn bản thô (raw text). Chúng chứa các thẻ định dạng (HTML tag).

Ví dụ:

`<html>` <br>
`<head><title>WWW</title>` <br>
`</head>` <br>
`<body>` <br>
`<p again=center>` <br>
`<a href="http://www.hoang2811.com/"><b>Trang web của Hoang2811` <br>
`</b></a>` <br>
`</b>` <br>
`</p>` <br>
`</body>` <br>
`</html>`

Trên cơ sở phục vụ những trang web tĩnh đơn giản này, ngày nay Web Server đã được phát triển với nhiều thông tin phức tạp hơn được chuyển giữa Web Server và Web Browser, trong đó quan trọng nhất có lẽ là nội dung động (dynamic content). Với phiên bản đầu tiên, Web Server hoạt động theo mô hình sau:

- Tiếp nhận các yêu cầu từ browser <br>
- trích nội dung từ đĩa.
- Chạy các chương trình CGI.
- Truyền dữ liệu ngược lại cho client. <br>
- Chạy càng nhanh càng tốt.

Điều này sẽ thực hiện tốt đối với các Web sites đơn giản, nhưng server sẽ bắt đầu gặp phải vẫn đề khi có nhiều người truy cập hoạc có quá nhiều trang web đọng phải tốn thời gian đẻ tính toán cho ra kết quả.

![](http://imgur.com/HXvebuL.png)

