# [Vận dụng cơ bản - 1] SỬA LỖI BUỔI PLANNING POKER CHO CÁC CHỨC NĂNG ĐẶT XE

## Phần 1 - Phân tích

| Mã PBI | Hợp lý / Chưa hợp lý | Quy tắc bị vi phạm | Hậu quả khi lập kế hoạch Sprint |
|---|---|---|---|
| P1 | Chưa hợp lý | 1. Lấy trung bình thay vì để người chọn 3 và 5 giải thích sự chênh lệch. 2. Kết quả (4 SP) không có trên thang điểm của đội. | Ước lượng không chính xác, dẫn đến kế hoạch Sprint không đáng tin cậy. Đội có thể cam kết quá nhiều hoặc quá ít việc trong Sprint, ảnh hưởng đến độ tin cậy của Velocity. |
| P2 | Chưa hợp lý | 1. Product Owner (Đức) tự ý quyết định SP. 2. Có sự chênh lệch lớn giữa các phiếu (5 vs 13) nhưng không có sự giải thích hay làm rõ. | Việc ước lượng bị ảnh hưởng bởi áp lực kế hoạch, không phản ánh đúng độ phức tạp/rủi ro. Đội có thể nhận quá nhiều việc vào Sprint (5 SP thay vì có thể là 8 hoặc 13), dẫn đến không hoàn thành Sprint Goal hoặc chất lượng kém. |
| P3 | Hợp lý | Đội đã thực hiện đúng quy trình Planning Poker: những người có phiếu lệch nhau (3 và 8) đã giải thích, sau đó đội chọn lại và đạt được sự đồng thuận trên một giá trị có trong thang điểm (5 SP). | (Quy trình hợp lý nên không có hậu quả tiêu cực) |
| P4 | Hợp lý về con số, sai ghi chú | 1. Ghi chú "13 SP = 52 giờ" vi phạm quy tắc SP là độ lớn tương đối, không quy đổi cố định sang giờ. | Việc quy đổi SP sang giờ có thể khiến quản lý lấy 52 giờ làm cam kết, tạo áp lực sai lệch lên đội và đánh mất tính tương đối của SP, gây sai lệch kỳ vọng và quản lý dự án. |
| P5 | Chưa hợp lý | 1. PBI chưa đủ rõ ràng để ước lượng (chưa biết mã có dùng chung với khuyến mãi khác không). 2. Chốt theo đa số (13 SP) mà không làm rõ vấn đề chưa biết hoặc sự chênh lệch giữa các phiếu. | Ước lượng dựa trên thông tin chưa đầy đủ sẽ dẫn đến SP không chính xác, rủi ro phát sinh công việc ẩn trong Sprint. Đội có thể phải đối mặt với các vấn đề không lường trước được, làm chậm tiến độ hoặc yêu cầu sửa đổi lớn sau này. |

## Phần 2 - Sửa lỗi

**P1: Đăng nhập bằng số điện thoại**
Người chọn 3 SP và người chọn 5 SP cần giải thích quan điểm của mình (ví dụ: có gửi mã xác nhận qua tin nhắn không, có xử lý trường hợp số điện thoại chưa đăng ký không). Sau đó, Developers sẽ chọn lại thẻ cho đến khi đạt được sự đồng thuận trên thang điểm đã định (ví dụ: 3 hoặc 5 SP).

**P2: Thanh toán bằng ví RikkeiPay**
Đức (Product Owner) cần làm rõ phạm vi và giá trị của việc thanh toán bằng ví (ví dụ: có hoàn tiền không, hạn mức mỗi giao dịch là bao nhiêu, có cần xử lý các loại phí giao dịch không). Sau đó, người chọn 5 SP và 13 SP cần giải thích các giả định hoặc rủi ro mà họ nhìn thấy (ví dụ: rủi ro tích hợp với hệ thống ví RikkeiPay). Developers sẽ chọn lại thẻ, và Product Owner không được quyết định con số SP cuối cùng.

**P4: Theo dõi vị trí tài xế trên bản đồ**
Giữ nguyên 13 SP vì đội đã đạt được sự đồng thuận sau khi giải thích. Tuy nhiên, cần loại bỏ ngay ghi chú "13 SP = 52 giờ" để tuân thủ quy tắc SP là độ lớn tương đối, không quy đổi sang giờ. Không cần chọn lại vì con số đã thống nhất, chỉ sửa ghi chú.

**P5: Áp mã giới thiệu bạn bè**
Đức (Product Owner) cần làm rõ các câu hỏi chưa biết (ví dụ: mã có được dùng chung với các khuyến mãi khác không, mỗi người dùng được mấy lần, có cần bổ sung Acceptance Criteria liên quan đến các trường hợp sử dụng mã). Sau khi PBI đã đủ rõ ràng, Developers mới tiến hành ước lượng lại.