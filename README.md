# AirVision Analytics

**AirVision Analytics** là một ứng dụng trực quan hóa dữ liệu chất lượng không khí và khí tượng theo thời gian thực. Ứng dụng cho phép người dùng theo dõi chất lượng không khí và các yếu tố khí tượng liên quan, với dữ liệu được thu thập và phân tích từ các nguồn đáng tin cậy.

## Tính năng chính
- Trực quan hóa dữ liệu chất lượng không khí và khí tượng theo thời gian thực.
- Hỗ trợ theo dõi các chỉ số như PM2.5, PM10, nhiệt độ, độ ẩm, tốc độ gió, v.v.
- Cung cấp biểu đồ và đồ thị dễ hiểu, giúp người dùng nắm bắt thông tin nhanh chóng.
- Cập nhật dữ liệu thường xuyên từ các nguồn khí tượng và chất lượng không khí.

## Cài đặt

### Prerequisites

1. Python 3.x
2. Thư viện yêu cầu:
   - `requests`
   - `pandas`
   - `matplotlib`
   - `plotly`

### Cài đặt môi trường

```bash
# Tạo môi trường ảo (tùy chọn)
python -m venv venv
source venv/bin/activate  # Trên macOS/Linux
venv\Scripts\activate     # Trên Windows

# Cài đặt các thư viện yêu cầu
pip install -r requirements.txt
```
## Cách sử dụng
### Chạy ứng dụng
```bash
python app.py
```

## Truy cập qua API
### Để truy cập dữ liệu qua API, bạn có thể sử dụng token được cung cấp. Cấu trúc API như sau:

### URL truy cập: https://example.com/data

## Cách sử dụng token trong URL:
``` bash
import requests

# URL và token
url = "https://example.com/data"
token = "2wIdHLEeJI9sBLsjQ3Lkt30ZYkT_33pMAYJokqqqyypmD9Zz9"

# Truy cập qua URL với token
response = requests.get(f"{url}?token={token}")

# Kiểm tra kết quả trả về
if response.status_code == 200:
    print("Dữ liệu: ", response.json())  # Hoặc .text tùy vào kiểu dữ liệu trả về
else:
    print("Lỗi khi truy cập: ", response.status_code)
```
### Truy cập qua header
``` bash
import requests

# URL và token
url = "https://example.com/data"
token = "2wIdHLEeJI9sBLsjQ3Lkt30ZYkT_33pMAYJokqqqyypmD9Zz9"

# Thiết lập header với token
headers = {
    'Authorization': f'Bearer {token}'
}

# Gửi yêu cầu GET với header
response = requests.get(url, headers=headers)

# Kiểm tra kết quả trả về
if response.status_code == 200:
    print("Dữ liệu: ", response.json())  # Hoặc .text tùy vào kiểu dữ liệu trả về
else:
    print("Lỗi khi truy cập: ", response.status_code)
```
## Liên hệ
### Tác giả: Quỳnh Phương

### Email: dinhlequynhphuong@gmail.com

## Giấy phép
### Ứng dụng này được phát hành dưới giấy phép [Tên giấy phép]. Xem LICENSE.md để biết thêm chi tiết.
