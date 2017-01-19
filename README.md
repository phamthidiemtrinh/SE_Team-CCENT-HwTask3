## 1.Địa chỉ mạng : 
- network adress là một dãy bit duy nhất để xác định một mạng. mỗi máy tính trong một mạng đều có địa chỉ mạng.
- tùy theo IP adress thuộc lớp A,B,C mà địa chỉ mạng chiếm 8,16 hay 32 bit trong IP
- các bit phần host của một địa chỉ Ip đều bằng không thì đó là địa chỉ mạng
## 2. Địa chỉ broadcast :
- là một loại dịa chỉ đặt biệt ( không dùng cho bất kì host nào) dùng để quảng bá.
- khi một gói tin đươc truyền vào địa chỉ broacast của một mạng thì gói tin đó sẽ được chuyển đến tất cả các host trong mạng đó
- các bit của host ddều là 1
## 3. Địa chỉ host:
- là dãy bit duy nhất được gán cho máy tính trong một mạng ( ở các mạng khác nhau thì địa chỉ host có thể giống nhau)

## 4. Đại chỉ loopback
- 127.0.0.1
- dùng cho việc tự kiểm tra ( IP tự trỏ vào bản thân nó)

## 5. Subnet mask :
-là dãy nhị phân đài 32bit dùng kèm với địa chỉ IP,
khi máy xác định địa chỉ mạng thì nó lấy kết quả của phép toán (IP and subnet mask) dưới dạng nhị phân,
nếu không khai báo subnet mask kèm theo địa chỉ IP thì địa chỉ IP đó được xem là không hợp lệ

## 6. Default gateway
- là một địa chỉ iP còn gọi là cổng mặc định.
- máy tính gửi gói dữ liệu đến địa chỉ này và địa chỉ này sẽ truyền tiếp gói tin đến nơi khác.
- bắt buộc phải cùng lớp mạng với địa chỉ IP của thiết bị cấu hình DG

## 7. vì sao phải chia IP
- tiết kiệm số lượng địa chỉ IP vì số lượng người truy cập Internet ngày càng nhiều
- tăng tính an toàn và tiết kiệm hơn cho người sử dụng internet
## 8. Subnetting : 
- là tổ hợp những kỹ thuật phân chia không gian địa chỉ của một lớp mạng cho trước thành nhiều lớp mạng nhỏ hơn bằng cách lấy một số bit ở phần Host Address (Host ID) để làm địa chỉ mạng cho mạng con (Subnet)

## 9. VSLM ( variable subnet length masking )
- giúp quản lý dãy địa chỉa IP chặt chẽ hơn, kiểm soát được số mạng mới sinh ra, số mạng đã dùng, số mạng dư thừa còn lại
- Có hai công thức về subnet được sử dụng trong phương pháp này là:
  - Số subnet được tạo ra = 2^m (với m là số bit mượn từ HostID)
  - Số host cần tạo = 2^n – 2 (với n là số bit của HostID còn lại sau khi mượn)
  - Số bit subnet mới = số bit subnet cũ + m
  
 - nguồn tham khảo: akali
## 10. CIDR(Classless Interdomain Routing) 
-là một cách để gộp(aggregation) các địa chỉ mạng lại thành một địa chỉ được biểu diễn bằng prefix mask(nghĩa là bằng số bit biểu diễn cho mặt nạ). Cách biểu diễn này không quan tâm đến địa chỉ thuộc lớp nào. CIDR khắc phục được vấn đề thiếu hụt địa chỉ và bảng định tuyến lớn.
- tham khảo : http://www.vnpro.org/forum/forum/ccent%C2%AE/icnd-1-osi-model-basic-tcp-ip/4739-cidr-va%CC%80-vlsm
