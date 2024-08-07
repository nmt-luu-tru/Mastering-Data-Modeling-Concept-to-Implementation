

### Các Giai Đoạn Thiết Kế

Hãy cùng tìm hiểu về chúng.

Có ba giai đoạn chính trong mô hình hóa dữ liệu ERP (ERP data modeling). Nếu bạn nhìn vào sơ đồ này, nó giống như một cái phễu.

Giai đoạn bắt đầu là thiết kế khái niệm (conceptual design), sau đó chuyển sang thiết kế logic (logical design), và cuối cùng là thiết kế vật lý (physical design).

### Thiết Kế Khái Niệm (Conceptual Design)

Thiết kế khái niệm là một thiết kế ở mức cao, không có nhiều chi tiết. Thiết kế logic dựa trên thiết kế khái niệm, và thiết kế vật lý là giai đoạn cuối cùng của ERD, nơi chúng ta tạo ra các script và giao cho khách hàng hoặc dự án.

Trong bài giảng này, chúng ta sẽ thảo luận về bước đầu tiên - thiết kế khái niệm.

### Chi Tiết Về Thiết Kế Khái Niệm

Thiết kế khái niệm là giai đoạn đầu tiên của mô hình hóa dữ liệu. Đây là mô hình dữ liệu trừu tượng nhất mô tả các yếu tố dữ liệu mà không có nhiều chi tiết. Chúng ta chủ yếu hiển thị các thực thể (entities) và mối quan hệ của chúng (relationships).

### Các Yếu Tố Trong Thiết Kế Khái Niệm

Thiết kế khái niệm chứa các thông tin sau:
- **Thực thể thực tế (real world entity)**: Là các yếu tố dữ liệu chính của chúng ta. Thực thể không gì khác ngoài các bảng (tables).
- **Mối quan hệ giữa các thực thể**: Bao gồm mối quan hệ mạnh (strong relationship), mối quan hệ yếu (weak relationship) và các tính quan hệ (cardinalities) như một-nhiều (one-to-many), nhiều-một (many-to-one), không-nhiều (zero-to-many), một-nhiều (one-to-many).
- **Phạm vi tổ chức (organization scope)**: Bao gồm những gì và không bao gồm những gì.
- **Khái niệm và quy tắc kinh doanh (business concept and rules)**: Được định nghĩa trong mô hình khái niệm.

### Ví Dụ Về Thiết Kế Khái Niệm

Dưới đây là một ví dụ về mô hình dữ liệu khái niệm của dự án chúng ta:

- **Course**: Thực thể Course.
- **Course Category**: Thực thể Course Category.
- **Student**: Thực thể Student, có thể đăng ký (enroll) vào một khóa học.

Mỗi thực thể được liên kết với nhau bằng các mối quan hệ và tính quan hệ. Ví dụ: một học sinh có thể đăng ký nhiều khóa học, một khóa học có thể có nhiều học sinh.

### Tầm Quan Trọng Của Thiết Kế Khái Niệm

Thiết kế khái niệm rất quan trọng vì nó giúp ghi lại các yêu cầu kinh doanh ở mức cao. Ví dụ: hỗ trợ đa tiền tệ (multi-currency) và múi giờ khác nhau (multi-time zone).

### Hậu Quả Khi Không Có Thiết Kế Khái Niệm

Nếu không có thiết kế khái niệm, dễ xảy ra các vấn đề như:

- **Thiếu yêu cầu cấp cao**: Ví dụ, không hỗ trợ đa tiền tệ hoặc múi giờ.
- **Giao tiếp kém giữa các nhóm**: Như việc hai nhóm xây dựng đường ray nhưng không kết nối được do thiếu giao tiếp.
- **Áp lực thời hạn**: Khiến thiết kế khái niệm bị bỏ qua, dẫn đến ảnh hưởng đến chu kỳ phát triển và thiếu các test case cho thiết kế cấp cao.
