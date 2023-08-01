XBlock Scope
-------------------
XBlock Scope là phạm vi truy cập của XBlock.

Hiểu được phạm vi của XBlock, giúp lập trình có thể bảo vệ dữ liệu nhạy cảm, cũng như tái sử dụng hoặc chia sẻ các XBlock với nhau.

Field có thể tương tác XBlock qua bốn kiểu phạm vi:

.. csv-table::
   :header: "Phạm vi", "Mô tả", "Ví dụ"
   :widths: 50, 90, 100

   "Block usage", "`Field thuộc về một thực thể khi sử dụng XBlock trong một khóa học cụ thể. Trong hầu hết các field hợp, nên sử dụng phạm vi này.`", "`Nếu người sử dụng tạo XBlock thăm dò ý kiến, các tùy chọn câu hỏi và câu trả lời của cuộc thăm dò ý kiến ​​sẽ cụ thể theo cách sử dụng, vì có thể có các cuộc thăm dò khác nhau trong các phần khác nhau của khóa học`"
   "Block definition", "`Field được định nghĩa một lần khi XBlock được khởi tạo. Có thể chia sẻ qua các khóa học và được tái sử dụng nhiều lần.`", "`Người sử dụng có thể tạo XBlock cho trình phát video và đặt các tùy chọn mặc định như tự động phát, phụ đề, v.v. trong định nghĩa. Tất cả các phiên bản của trình phát video đó sẽ sử dụng các giá trị mặc định đó.`"
   "Block type", "`Là kiểu dữ liệu Python của field (ví dụ: Integer, String, ...)`", "`Nhà phát triển có thể có một field lưu trữ tên tác giả cho một loại XBlock cụ thể.`"
   "All", "`Khi Field có phạm vi kiểu All, mọi XBlock đều có thể truy cập và sử dụng dữ liệu.`", "`Nhà phát triển có thể tạo XBlock để hiển thị thời gian hiện tại. Khi mỗi phiên bản của XBlock được tải, Field current_datetime sẽ được chia sẻ và hiển thị giá trị đó.`"

.. note::
    Khi sử dụng phạm vi kiểu All, có khả năng xảy ra xung đột giữa các Ffeld với nhau: trùng tên, rối loạn kiểu dữ liệu, …