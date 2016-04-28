#Tìm hiểu về VMware Workstation.
##Mục lục
[I. Giới thiệu về VMware Workstation](#gioi-thieu)
[1. Tổng quan về VMware Workstation](#tong-quan)
[2. Tính năng chính](#tinh-nang)
[3. Ưu/Nhược điểm](#uu-nhuoc)
[II. Hướng dẫn sử dụng](#huong-dan)
[1. Cách cài đặt VMware Workstation 12 trên Windows](cai-dat)
[2. Cách tạo máy ảo(Ubuntu Server 14.04) trên VMware](tao-may-ao)
[III. Khái quát một vài tính năng của VMware](khai-quat)
----

### <a name="gioi-thieu"></a>I. Giới thiệu về VMware Workstation
#### <a name="tong-quan"></a>1. Tổng quan về VMware Workstation
- VMware Workstation là một phần mềm ảo hóa desktop mạnh mẽ dành cho các nhà phát triển/kiểm tra
phần mềm và các chuyên gia IT cần chạy nhiều HĐH một lúc trên một máy PC. 
- Người dùng có thể chạy các HĐH Windows, Linux, Netware hay Solaris x86 trên các máy ảo di động mà không cần phải khởi
động lại hay phân vùng ổ cứng.
- VMware Workstation cung cấp khả năng hoạt động tuyệt vời và nhiều
tính năng mới như tối ưu hóa bộ nhớ và khả năng quản lý các thiết lập nhiều lớp. 
- Các tính năng thiết yếu
như mạng ảo, chụp ảnh nhanh trực tiếp, kéo thả, chia sẻ thư mục và hỗ trợ PXE khiến VMware
Workstation trở thành công cụ mạnh mẽ nhất và không thể thiếu cho các nhà doanh nghiệp phát triển tin
học và các nhà quản trị hệ thống.
- VMware Workstation họat động bằng cách cho phép nhiều HĐH và các ứng dụng của chúng chạy đồng
thời trên một máy duy nhất. Các HĐH và ứng dụng này được tách ra vào trong các máy ảo. Những máy
ảo này cùng tồn tại trên một phần cứng duy nhất. Các layer ảo của VMware sẽ kết nối các phần cứng vật
lý với các máy ảo, do đó mỗi máy ảo sẽ có CPU, bộ nhớ, các ổ đĩa, thiết bị nhập/xuất riêng.
#### <a name="tinh-nang"></a>2. Tính năng chính
- Thiết lập và thử nghiệm các ứng dụng đa lớp, cập nhật ứng dụng và các miếng vá cho HĐH chỉ
trên một PC duy nhất.
- Dễ dàng phục hồi và chia sẻ các môi trường thử nghiệm được lưu trữ; giảm thiểu các thiết lập
trùng lặp và thời gian thiết lập.
- Làm cho việc học tập trên máy tính thuận lợi hơn do sinh viên luôn đuợc sử dụng máy với tình
trạng “sạch sẽ” và thử nghiệm với nhiều HĐH, ứng dụng cá các công cụ trên những máy ảo an
toàn và độc lập
- Chạy các bản demo phần mềm với các thiết lập phức tạp hoặc đa lớp trên một chiếc laptop
- Tăng tốc độ giải quyết các rắc rối của người dùng cuối dựa trên một thư viện các máy ảo được
thiết lập sẵn
- Hỗ trợ nhiều màn hình – Bạn có thể thiết lập để một VM trải rộng ra nhiều màn hình, hoặc
nhiều VM, với mỗi VM trên một màn hình riêng biệt.
#### <a name="uu-nhuoc"></a>2. Ưu/Nhược điểm
- Ưu điểm:
<ul>
<li>Giữa các máy ảo: Tính bảo mật cao do các máy ảo làm việc độc lập với nhau</li>
<li>Các tài nguyên vật lý được bảo vệ hoàn toàn vì các máy ảo có thiết bị ảo</li>
<li>Có thể lấy từ Internet về một chương trình lạ và thử vận hành trên máy ảo mà không sợ bị ảnh hưởng đến máy thật</li>
<li>Giải pháp giảm chi phí cho người dùng</li>
</ul>
- Nhược điểm:
<ul>
<li>Nếu hacker nắm quyền điều khiển máy tính chứa các máy ảo thì hacker có thể kiểm soát được tất cả các máy ảo trong nó</li>
<li>Máy tính có cấu hình phần cứng thấp cài nhiều chương trình máy ảo, máy sẽ chậm và ảnh hưởng đến các chương trình khác</li>
<li>Nếu máy tính chứa các máy ảo bị hư thì các máy ảo thiết lập trên nó cũng bị ảnh hưởng</li>
</ul>
### <a name="huong-dan"></a>II. Hướng dẫn sử dụng

#### <a name="cai-dat"></a>1. Hướng dẫn cài đặt VMware Workstation 12 trên Windows
**Tính năng mới của VMware Workstation 12**
- Bổ sung hỗ trợ mới các hệ điều hành: Windows 10, Ubuntu 15.04, Fedora 22, CentOS 7.1, RHEL 7.1, Oracle Linux 7.1, VMware Project Photon...
- Hỗ trợ độ phân giải cao 4K
- Cải tiến hiệu suất
- Tạo được các máy ảo lên đến 16 vCPUs, 8 TB dung lượng ổ đĩa ảo, và 64 GB bộ nhớ
- Tân dụng tối đa phần cứng, hỗ trợ HD audio lên đến 7.1 sound, USB 3.0, và thiết bị Bluetooth dễ dàng thiết lập webcam, headset, hay printer kết nối đến máy ảo.
- Hỗ trợ kết nối đến VMware vSphere và dịch vụ vCloud Air cho phép mở rộng quy mô máy ảo trên cloud

**Cấu hình tối thiểu**

- Hệ điều hành chạy trên nền tảng 64-bit.
- Chip Intel Core 2 Duo Processor, AMD Athlon ™ 64 FX Dual Core Processor hoặc cao hơn..
- Tốc độ xử lý tối thiểu là 1.3GHz..
- Ram tối thiểu là 2GB.

**Cấu hình lí tưởng**
- Đối với Laptop: Corei5 trở lên và Ram 4GB trở lên.
- Đối với máy tính PC (máy bàn): Corei3 và RAM 4GB trở lên

**Các bước cài đặt VMware Workstation trên Windows**

- Bước 1: Download bản mới nhất [tại đây](http://www.vmware.com/products/workstation/workstation-evaluation)

- Bước 2: Mở file cài đặt, chọn `Next`

<img src="https://cloud.githubusercontent.com/assets/18635054/14896437/eda9466c-0da7-11e6-8f31-debd9a33f757.png">

- Bước 3: Chọn `I accept the terms in the License Agreement` và chọn `Next`

<img src="https://cloud.githubusercontent.com/assets/18635054/14896438/edb0095c-0da7-11e6-85a8-e16d1f45c090.png">

- Bước 4: Chọn đường dẫn cài đặt, sau đó ấn `Next`

<img src="https://cloud.githubusercontent.com/assets/18635054/14896453/0599e0d8-0da8-11e6-8048-f2ac7cf77b38.png">

- Bước 5: Lựa chọn tự động kiểm tra update khi khởi động và đóng góp ý kiến cho VMware. Nếu không, có thể bỏ chọn ở cả 2 và ấn `Next`

<img src="https://cloud.githubusercontent.com/assets/18635054/14896454/059cd75c-0da8-11e6-9351-53fa8f9c8d8b.png">

- Bước 6: Lựa chọn tạo ra `Shortcuts` tại Desktop hoặc `Start Menu Programs Folder`

<img src="https://cloud.githubusercontent.com/assets/18635054/14896472/1dd90e26-0da8-11e6-8499-7eb9336c17ab.png">

- Bước 7: Chọn `Install` để tiếp tục cài đặt, sau khi kết thúc, chọn `Finish`

<img src="https://cloud.githubusercontent.com/assets/18635054/14896473/1dde093a-0da8-11e6-8798-b9255c034994.png">

<img src="https://cloud.githubusercontent.com/assets/18635054/14896515/51dc4efe-0da8-11e6-95d8-65429a34b14b.png">

- Bước 8: Khởi động VMware, nhập key và ấn `Continue` để tiếp tục.

<img src="https://cloud.githubusercontent.com/assets/18635054/14896526/688e87de-0da8-11e6-8497-0047c2ab6bba.png">
<img src="https://cloud.githubusercontent.com/assets/18635054/14896528/6ab668ce-0da8-11e6-9d4f-d33f7a47c86d.png">

- Kết quả:

<img src="https://cloud.githubusercontent.com/assets/18635054/14896593/b26e9132-0da8-11e6-8b7f-714d6cc70664.png">

#### <a name="tao-may-ao"></a>2. Cách tạo máy ảo(Ubuntu Server 14.04) trên VMware Workstation 12

- Bước 1: Chọn `Create a new Virtual Machine` và làm theo các bước

<img src="https://cloud.githubusercontent.com/assets/18635054/14896606/c0a14a74-0da8-11e6-965c-aef1e03a7b89.png">

- Bước 2: Chọn `Next`

<img src="https://cloud.githubusercontent.com/assets/18635054/14896605/c09f666e-0da8-11e6-90d3-ec7bea4e1e45.png">

- Bước 3: Chọn `I will install the operating system later` và ấn `Next`

<img src="https://cloud.githubusercontent.com/assets/18635054/14896608/c0a3667e-0da8-11e6-8c3d-600acdb9fc95.png">

- Bước 4: Chọn hệ điều hành, ở đây tôi chọn `Linux` và hệ điều hành là Ubuntu 64 bit

<img src="https://cloud.githubusercontent.com/assets/18635054/14896607/c0a2f450-0da8-11e6-8dd0-3c82f5c3abc5.png">

- Bước 5: Đặt tên cho máy ảo và tạo nơi lưu máy ảo.

<img src="https://cloud.githubusercontent.com/assets/18635054/14896647/eae39170-0da8-11e6-9784-bacf7c31d418.png">

- Bước 6: Cấu hình bộ vi xử lí cho máy ảo

<img src="https://cloud.githubusercontent.com/assets/18635054/14896649/eae66652-0da8-11e6-8784-417aa5c57bb6.png">

- Bước 7: Chọn RAM cho máy ảo và ấn `Next`

<img src="https://cloud.githubusercontent.com/assets/18635054/14896650/eae6fe6e-0da8-11e6-9387-789579b01309.png">

- Bước 8: Chọn kiểu card mạng cho máy ảo. Tham khảo thêm [tại đây](https://github.com/hocchudong/vmware-workstation-network)
Ở đây tôi chọn card NAT, sau đó ấn `Next`

<img src="https://cloud.githubusercontent.com/assets/18635054/14896648/eae40434-0da8-11e6-8ae7-f8b1b0cf4cba.png">

- Bước 9: Cấu hình ổ cứng

<img src="https://cloud.githubusercontent.com/assets/18635054/14896718/2807ebbe-0da9-11e6-853b-2141c03473b4.png">
<img src="https://cloud.githubusercontent.com/assets/18635054/14896717/28060092-0da9-11e6-849f-fedb2554153a.png">
<img src="https://cloud.githubusercontent.com/assets/18635054/14896719/2808f2de-0da9-11e6-8235-a6273001483d.png">
<img src="https://cloud.githubusercontent.com/assets/18635054/14896720/2809e496-0da9-11e6-8b29-cf0e1b8efa11.png">

- Bước 10: Chọn nơi lưu ổ cứng

<img src="https://cloud.githubusercontent.com/assets/18635054/14896749/511c79e8-0da9-11e6-9673-db2ddb1374b5.png">

- Bước 11: Chọn `Customize Hardware` và tiến hành add ISO hệ điều hành vào theo các bước:

<img src="https://cloud.githubusercontent.com/assets/18635054/14896748/511bf22a-0da9-11e6-9406-1b460b7413c6.png">
<img src="https://cloud.githubusercontent.com/assets/18635054/14896750/511d6bd2-0da9-11e6-88ff-f1be621fdb20.png">

- Bước 12: Chọn `Finish` và chọn tiếp `Power on this virtual machine` để khởi động máy ảo.

<img src="https://cloud.githubusercontent.com/assets/18635054/14896751/51331cca-0da9-11e6-86fe-8ea38f177525.png">

- Bước 13: Tiến hành cài đặt Ubuntu Server như bình thường. Xem [tại đây](https://github.com/edenhanu/cai-dat-ubuntu-server)




