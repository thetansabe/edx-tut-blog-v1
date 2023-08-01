User Scope
-------------------
User Scope là phạm vi truy cập của người dùng.

Một Field có thể có các scope sau:

.. csv-table::
   :header: "Phạm vi", "Mô tả", "Ví dụ"
   :widths: 50, 90, 100

   "No user", "`Field có thể không phụ thuộc vào bất kì user nào`", "`Field count đếm số lượng học viên hiện đang truy cập trang web (mọi người đều nhìn thấy và không một ai có thể sửa được)`"
   "One user", "`Field dành riêng cho một người dùng cụ thể.`", "`Một field id thì chỉ có một user có`"
   "All users", "`Field chứa dữ liệu chung cho tất cả người dùng.`", "`Tổng số học viên trả lời một câu hỏi là như nhau đối với tất cả người dùng.`"

Mối liên hệ giữa phạm vi người dung và phạm vi block: 

.. csv-table::
   :header: "", "UserScope.NONE", "UserScope.ONE", "UserScope.ALL "
   :widths: 60, 50, 50, 50

   BlockScope.DEFINITION, Scope.content, , 
   BlockScope.USAGE, Scope.settings, Scope.user_state, Scope.user_summary
   BlockScope.TYPE, , Scope.preferences, 
   BlockScope.ALL, , Scope.user_info,  