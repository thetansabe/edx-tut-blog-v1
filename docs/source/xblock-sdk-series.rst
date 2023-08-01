Series giới thiệu XBlock-SDK
=============================
.. _xblock-sdk-introduction:

Giới thiệu
-------------------
Trong phần :ref:`cài đặt và triển khai XBlock-SDK trước <xblock-sdk-configuration>` chúng ta đã cùng tìm hiểu và xây dựng một XBlock cơ bản. Để thuận lợi cho việc nghiên cứu và phát triển các XBlock dựa trên XBlock-SDK (Software Development Kit), các bạn hãy tạo một XBlock tên Counter XBlock.

Bài viết này đi vào tìm hiểu những khái niệm cơ bản, xây dựng các chức năng, và thực hành phát triển một XBlock mới dựa trên  dự án Counter XBlock. Đây là một XBlock cơ bản cho phép người dạy tích hợp vào khoá học để đếm số lượng bỏ phiếu của 1 bài khảo sát.

Điều kiện
-------------------
Bài viết này hướng đến các lập trình viên. Do đó, độc giả nên có kiến thức cơ bản các công nghệ sau: 

- Python 

- JavaScript 

- HTML và CSS 

- Môi trường ảo Python (Anaconda) 

Bên cạnh đó, các lập trình viên nên đọc và tìm hiểu thêm về :ref:`series tìm hiểu XBlock <xblock_overview>` để hiểu rõ hơn về cách xây dựng và phát triển một XBlock mới.

Để tiện theo dõi, bạn nên ghé qua `repository này <https://github.com/S1mpleOW/counter_xblock/tree/main/counter>`_

XBlock Fields
-------------------
Sau các bước tạo CounterXBlock, ở trong tập tin counter.py, chúng ta tiến hành tạo một field với tên gọi là count.

Xuyên suốt bài blog, để thuận lợi cho việc tìm hiểu, chúng tôi xin phép sử dụng "field" thay cho "trường".

.. code-block:: python

    count = Integer(
        default=0, 
        scope=Scope.user_state, 
        help="A simple counter, to show something happening")

Có thể truy cập giá trị count để hiện thị ra UI trong tập tin counter.html ở thư mục static 

.. code-block:: html

    <div id="counter-value">{self.count}</div>

.. csv-table::
   :header: "Tham số", "Mô tả"
   :widths: 50, 90

    help, Để mô tả field
    default, Xác định giá trị khởi tạo của field
    scope, Xác định phạm vi field

.. toctree::
    :maxdepth: 4

    field-xblock-scope
    field-user-scope
    field-and-data-storage
    field-and-olx

Tổng kết
-------------------