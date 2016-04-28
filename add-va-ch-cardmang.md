#Cách add 2 card mạng và cấu hình cho card mạng trong VMware Workstation
##Mục lục
[I. Tổng quan về card mạng trong VMware](#tong-quan)

[II. Cách add mới 2 card mạng](#add-card)

[III. Cấu hình cho 2 card mạng vừa add](#cau-hinh)

----

### <a name="tong-quan"></a>I.Tổng quan về card mạng trong VMware
- Các thành phần hình thành nên mạng ảo trong VMware gồm switch ảo, card mạng ảo, DHCP server ảo và thiết bị NAT.
- Switch ảo (Virtual Switch) cũng giống như switch vật lý, một Virtual Switch kết nối các thành phần mạng ảo lại với nhau. 
  Những  switch ảo hay còn gọi là mạng ảo, chúng có tên là VMnet0, VMnet1, VMnet2… một số switch ảo được gắn vào mạng một cách mặc định.
- Mặc định khi ta cài Wmware thì có sẵn 3 Switch ảo như sau: **VMnet0** chế độ `Bridged` (cầu nối), 
															 **VMnet8 chế độ `NAT` 
															 và **VMnet1** chế độ `Host-only`.
<img src="https://cloud.githubusercontent.com/assets/18635054/14832541/0228df1e-0c25-11e6-899b-0a8329713263.png">

- Ta có thể thêm, bớt, chỉnh các option của VMnet bằng cách vào menu `Edit -> Virtual Network Editor`
Xem thêm [tại đây](https://github.com/ducnc/vmware-workstation-network)

- Khi ta tạo các VMnet thì trên máy thật của ta sẽ tạo ra những card mạng ảo tương ứng, 
riêng VMnet0 kết nối trực tiếp với card mạng vật lý nên không tạo ra card VMnet.

<img src="https://cloud.githubusercontent.com/assets/18635054/14832556/18c83350-0c25-11e6-972e-4dd3763f49ac.png">

- DHCP(Dynamic Host Configuration) server ảo cung cấp địa chỉ IP cho các máy ảo trong việc kết nối máy ảo vào các Switch ảo không có tính năng Bridged (VMnet0)
Ví dụ như DHCP ảo cấp đến các máy ảo có kết nối đến Host-only và NAT.
- Nếu muốn bỏ chế độ DHCP của VMnet nào, chỉ cần bỏ dấu check tại `Use local DHCP service to distribute IP address to VMs` trong `Virtual Network Editor`.

<img src="https://cloud.githubusercontent.com/assets/18635054/14832568/26614150-0c25-11e6-9b33-688304441b12.png">

- LAN Segment: Các card mạng của máy ảo có thể gắn kết với nhau thành từng LAN Segment. 
Không giống như VMnet, LAN Segment chỉ kết nối các card ảo lại với nhau mà không có những tính năng như DHCP 
hoặc kết nối chung với một card mạng ảo được tạo bên ngoài (các VMware Network Adapter VMnet được tạo bên ngoài máy thật).

----

### <a name="add-card"></a>I.Cách add mới 2 card mạng trong VMware

- Đầu tiên hãy kiểm tra card mạng hiện có bằng cách vào `Edit -> Virtual Network Editor`

- Chọn vào phần `Setting` của máy cần thêm card mạng, chọn `add` để thêm.

<img src="https://cloud.githubusercontent.com/assets/18635054/14832587/38e88112-0c25-11e6-808a-33b8a60d608c.png">

- Chọn tiếp kiểu card mạng(Bridge, NAT và Host-only)
- Trong VMware có 3 chế độ cho card mạng ảo
<ul>
<li>Chế độ **Bridge**: ở chế độ này thì card mạng trên máy ảo sẽ được gắn vào VMnet0 và VMnet0 này liên kết trực tiếp với card mạng vật lý. 
Ở chế độ này máy ảo sẽ kết nối internet thông qua lớp card mạng vật lý và có chung lớp mạng với card mạng vật lý.</li>
<li>Chế độ **NAT**: ở chế độ này thì card mạng của máy ảo kết nối với VMnet8, VNnet8 cho phép máy ảo đi internet thông qua cơ chế NAT (NAT device).
Lúc này lớp mạng bên trong máy ảo khác hoàn toàn với lớp mạng của card vật lý bên ngoài. IP của card mạng sẽ được cấp bởi DHCP VMnet8 cấp, 
trong trường hợp bạn muốn thiết lập IP tĩnh cho card mạng máy ảo bạn phải đảm bảo chung lớp mạng với VNnet8 thì máy ảo mới có thể đi internet.</li>
<li>Cơ chế **Host-only**: ở cơ chế này máy ảo được kết nối với VMnet có tính có tính năng Host-only, trong trường hợp này là VMnet1 (bạn có thể add nhiều VMnet Host-only).
VMnet Host-only kết nối ra một card mạng ảo tương ứng ngoài máy thật.

Ở chế độ này máy ảo không có kết nối internet. IP của máy ảo được cấp bởi DHCP của VMnet tương ứng.
Trong nhiều trường hợp đặc biệt cần cấu hình riêng, ta có thể tắt DHCP trên VMnet và cấu hình IP bằng tay cho máy ảo.</li>
</ul>

<img src="https://cloud.githubusercontent.com/assets/18635054/14832611/4e893cfa-0c25-11e6-8b4f-56944f258f80.png">

- Ấn `Finish` để hoàn thành việc add card mạng
- Làm tương tự với card mạng còn lại

----
### <a name="cau-hinh"></a>III. Cấu hình cho 2 card mạng mới add

- Cấu hình địa chỉ IP tĩnh và động cho card mạng bằng cách sửa file và câu lệnh
Xem thêm [tại đây](https://github.com/edenhanu/cauhinh-ip-cho-ubuntusv)

<img src="https://cloud.githubusercontent.com/assets/18635054/14832638/635358dc-0c25-11e6-8366-6436f1d81f10.png">

