#Thiết lập IP tĩnh và động cho Ubuntu Server
##Mục lục
[I. Giới thiệu về giao diện mạng](#gioi-thieu)

[II. Các cách cấu hình địa chỉ IP](#cau-hinh)
- [1.Cấu hình địa chỉ IP tĩnh](#cau-hinh-tinh)
	<ul>
	<li>[1.1. Cấu hình bằng câu lệnh](#cau-lenh)</li>
	<li>[1.2. Cấu hình bằng cách sửa file](#sua-file)</li>
	</ul>
- [2. Cấu hình địa chỉ IP động](#ip-dong)

----

### <a name="gioi-thieu"></a>I.Giới thiệu về giao diện mạng

Mỗi máy tính cần có một card mạng Ethernet có dây hoặc không dây
- Nhận dạng bởi tên: ethX
  <ul>
  <li>eth0 cho card mạng thứ nhất</li>
  <li>eth1 cho card mạng thứ 2...</li>
  </ul>
- Xem có bao nhiêu giao diện Ethernet
	`ifconfig ­a | grep eth`
- Để kiểm tra xem các card mạng đã được cấu hình hay chưa gõ lệnh sau
                `ifconfig`
Lệnh này cung cấp thông tin về địa chỉ MAC, địa chỉ IP, gateway... của tất cả các card mạng. Nếu muốn xem thông tin từng card mạng gõ lệnh này cộng với tên card mạng được list ở bước trên ví dụ `ifconfig eth0`

- Để xem các định tuyến đi qua các mạng như thế nào gõ lệnh sau:
                `route -n`


-----
### <a name="cau-hinh"></a>II.Các cách cấu hình địa chỉ IP
#### <a name="cau-hinh-tinh"></a>1. Cấu hình địa chỉ IP tĩnh
##### <a name="cau-lenh"></a>1.1. Cấu hình bằng câu lệnh
Để gán ip, cấu hình cho card mạng và kiểm tra chúng ta dùng lệnh sau. 
`ifconfig ethX IP-address netmask subnet-mask`
Lệnh này sẽ có tác dụng ngay lập tức tuy nhiên cấu hình này không ghi vào file config nên sẽ mất khi khởi động lại máy.
- Trong đó:
<ul>
<li>`ethX` là tên card mạng(xem bằng lệnh ifconfig -a)</li>
<li>`IP-address` là địa chỉ ip muốn gán</li>
<li>`subnet-mask` là địa chỉ netmask</li>
</ul>
- Ví dụ : Đặt địa chỉ ip `192.168.1.1`, subnet mask là 255.255.255.0 cho card mạng eth0
`ifconfig eth0 192.168.1.1 netmask 255.255.255.0`

- Kết quả
<img src="https://cloud.githubusercontent.com/assets/18635054/14819031/7443b050-0bea-11e6-891e-f9f3ad32676c.png">
----
##### <a name="sua-file"></a>1.2. Cấu hình bằng cách sửa file

Ubuntu cũng như các hệ điều hành linux khác coi card mạng là một devicce và lưu cấu hình trong file text, sau đó tải lên mỗi khi khởi động máy.
Muốn card mạng được khai báo IP cố định, không mất đi sau khi khởi động lại máy, chúng ta đặt các lệnh cấu hình card mạng trong file cấu hình có đường dẫn là `/etc/network/interface`. 
Có thể dùng lệnh `vi` hoặc `gedit` để tạo file cấu hình card mạng này và chỉnh sửa nó.

`vi /etc/network/interfaces`

**Nội dung file**:
<img src="https://cloud.githubusercontent.com/assets/18635054/14819082/b3770e3e-0bea-11e6-8c7d-07bc0d9c6c62.png">
- Trong đó:
	<ul>
	<li>eth0 là tên card mạng</li>
	<li>static có nghĩa card mạng đang nhận địa chỉ IP tĩnh</li>
	<li>address là địa chỉ ip</li>
	<li>netmask là địa chỉ netmask </li>
	<li>network là địa chỉ đường mạng</li>
	<li>broadcast địa chỉ broadcast</li>
	<li>gateway địa chỉ gateway</li>
	</ul>

- Sau khi chỉnh sửa cần khởi động lại máy hoặc sử dụng lệnh để restart lại card mạng
<ul>
<li>sudo reboot</li>
<li>sudo /etc/init.d/networking restart</li>
</ul>
----
#### <a name="ip-dong"></a>2. Cấu hình địa chỉ IP động
- Để có thể cấu hình IP động cho Ubuntu Server, chúng ta cũng tiến hành sửa thông tin trong file cấu hình

<img src="https://cloud.githubusercontent.com/assets/18635054/14819128/dca28d10-0bea-11e6-8c91-b4b287150663.png">

- Trong đó
<ul>
<li>eth0 là tên card mạng</li>
<li>dhcp có nghĩa card mạng sẽ nhận IP động từ dịch vụ DHCP</li>
</ul>

- Sau khi chỉnh sửa file cấu hình, cần khởi động lại máy hoặc thực hiện lệnh bên trên để khởi động lại card mạng


