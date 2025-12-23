# Marketing-and-Product-Performance-Dataset
## Tổng quan về dự án
Trong bối cảnh cạnh tranh ngày càng cao của thương mại điện tử, việc hiểu rõ hành vi người dùng và hiệu quả của các chiến dịch marketing trực tuyến đóng vai trò then chốt trong việc tối ưu tỷ lệ chuyển đổi và doanh thu. Bộ dữ liệu được sử dụng trong luận văn này ghi lại các tương tác của người dùng với các chiến dịch marketing trực tuyến của một website thương mại điện tử mang tính mô phỏng, trong khoảng thời gian từ ngày 01/06/2023 đến 30/06/2023.

### Nguồn dữ liệu
 Dữ liệu được lưu trữ dưới dạng tệp CSV với tên web_marketing_data.csv, trong đó mỗi quan sát đại diện cho một phiên truy cập (user session) của người dùng trên website.
 
### Mô tả dữ liệu
Bộ dữ liệu bao gồm nhiều nhóm biến phản ánh đầy đủ các khía cạnh liên quan đến hành vi người dùng và hiệu quả chiến dịch marketing, cụ thể như: thông tin thời gian truy cập, đặc điểm hành vi trong phiên, nguồn và kênh marketing, thiết bị sử dụng, vị trí địa lý cũng như kết quả chuyển đổi và doanh thu. Nhờ đó, dữ liệu cho phép thực hiện các phân tích chuyên sâu về hành vi người dùng, đánh giá hiệu quả các chiến dịch marketing và xây dựng các mô hình dự đoán khả năng chuyển đổi.
Các biến trong bộ dữ liệu:

Date: Ngày diễn ra phiên truy cập của người dùng (định dạng MM/DD/YYYY).

User_ID: Mã định danh duy nhất cho mỗi người dùng.

Session_Duration: Thời lượng của phiên truy cập, tính bằng giây.

Page_Views: Số trang được người dùng xem trong một phiên.

Source: Nguồn truy cập của người dùng, ví dụ: Referral, Social, Direct, Organic.

Medium: Kênh marketing được sử dụng, bao gồm Direct, Social Media, Organic Search và Referral. Lưu ý: Thuật ngữ “Referral” có thể xuất hiện ở cả hai biến Source và Medium, thể hiện các hình thức giới thiệu khác nhau.

Campaign: Chiến dịch marketing cụ thể gắn với phiên truy cập (ví dụ: Spring Promo, Summer Sale). Các giá trị trống biểu thị các phiên không liên kết trực tiếp với một chiến dịch cụ thể.

Device_Category: Loại thiết bị người dùng sử dụng để truy cập website (Desktop, Mobile, Tablet).

Country: Quốc gia của người dùng.

New_User: Biến nhị phân, trong đó giá trị 1 đại diện cho người dùng mới và 0 đại diện cho người dùng quay lại.

Conversions: Số lượt chuyển đổi được ghi nhận trong phiên truy cập.

Revenue: Doanh thu tạo ra từ phiên truy cập của người dùng, tính bằng USD.

Dựa trên tập dữ liệu này, bài luận tập trung phân tích hiệu quả của các kênh marketing và chiến dịch quảng cáo, cũng như hành vi người dùng trên các thiết bị khác nhau.
Trước khi tiến hành phân tích và xây dựng mô hình dự đoán, dữ liệu cần được kiểm tra và làm sạch nhằm đảm bảo tính nhất quán và độ tin cậy. Trong nghiên cứu này, Python được sử dụng để thực hiện các bước kiểm tra và làm sạch dữ liệu ban đầu do khả năng truy vấn hiệu quả và dễ tái lập trên tập dữ liệu lớn, đồng thời dùng để phân tích mối quan hệ giữa các biến và dự báo.


