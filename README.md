#1. Vào thư mục Apache trong XAMPP.
Mặc định XAMPP đợc cài đặt trong thư mục C:\xampp\apache.
#2. Tạo một thư mục mới.
Đây là nơi ta sẽ lưu trữ chứng chỉ SSL. Trong ví dụ này Ngôi Sao Số sẽ tạo thư mục crt ,Vì vậy, đường dẫn sẽ có dạng C:\xampp\apache\crt
#3. Tải về và thêm 2 tập tin này vào thư mục vừa tạo
Vào đường dẫn sau https://github.com/khahdihdz/Enabling-SSL-with-XAMPP tải 2 tập tin cert.conf make-cert.bat về. 2 tập tin này sẽ dùng để tạo chứng chỉ SSL cho tên miền tùy thích. 
#4. Sửa cert.conf và chạy make-cert.bat
Mở file cert.conf và thay đổi {{DOMAIN}} thành tên miền bạn muốn, trong trường hợp này site.test và lưu lại.
Nhấp đúp chuột vào make-cert.bat và nhập tên miền site.test khi được nhắc. Và nhập trả lời cho các câu hỏi khác, thiết lập mặc định có sẵn trong cert.conf
https://wiki.ngoisaoso.vn/uploads/news/2020_04/huong-dan-cau-hinh-ssl-tren-localhost-cho-xampp-1.jpg
#5. Cài đặt chứng chỉ trong windows.
Sau đó, bạn sẽ thấy thư mục site.test được tạo. Trong thư mục đó ta sẽ có server.crt and server.key. Đây là chứng chỉ SSL certificate.

Nhấp đúp chuột vào server.crt để cài đặt nó trên Windows để Windows chấp nhận chứng chỉ này.
https://wiki.ngoisaoso.vn/uploads/news/2020_04/huong-dan-cau-hinh-ssl-tren-localhost-cho-xampp-2.png
Và chọn Local Machine trong Store Location.
https://wiki.ngoisaoso.vn/uploads/news/2020_04/huong-dan-cau-hinh-ssl-tren-localhost-cho-xampp-3.png
Tiếp tục chọn “Place all certificate in the following store” và click browse sau đó chọn Trusted Root Certification Authorities.
https://wiki.ngoisaoso.vn/uploads/news/2020_04/huong-dan-cau-hinh-ssl-tren-localhost-cho-xampp-4.png
Chọn Next và Finish.

Và bây giờ chứng chỉ này đã được cài đặt là tin cậy (trusted) trong Windows. Tiếp theo là làm thế nào để sử dụng chứng chỉ này trong XAMPP.
#6. Thêm trang web trong máy chủ Windows

    Mở notepad với quyền administrator.
    Sửa C:\Windows\System32\drivers\etc\hosts
    Thêm một dòng mới:
127.0.0.1 site.test
https://wiki.ngoisaoso.vn/May-chu/meo-huong-dan-cau-hinh-ssl-tren-localhost-cho-xampp-329.html
