Fields and Data Storage
-------------------
Mối quan hệ Field and Data Storage (giữa field và nơi lưu trữ dữ liệu): các field được ghi và truy xuất dưới dạng các thực thể (instance) đơn lẻ, nên không thể lưu trữ một lượng lớn dữ liệu trong cùng một field. Do đó, ta nên chia nhỏ dữ liệu thành nhiều field nhỏ hơn để lưu trữ. 

Ví dụ: nếu ta có một XBlock lưu trữ thông tin về học viên bao gồm tên, địa chỉ, và số điện thoại, thay vì lưu trữ tất cả thông tin trong một trường, ta có thể chia thành các trường nhỏ hơn như "name", "address" và "phone_number". Điều này giúp chúng ta quản lý dữ liệu một cách dễ dàng và tiết kiệm không gian lưu trữ.