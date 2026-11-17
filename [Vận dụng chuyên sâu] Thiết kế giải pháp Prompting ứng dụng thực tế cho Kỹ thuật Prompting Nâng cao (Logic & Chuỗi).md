
# 1.Thiết kế giải pháp prompting , kỹ thuật prompting nâng cao

## **Bước 1: Thiết kế giải pháp (I/O)**

Em chọn giải pháp tự động hóa xử lý đơn hàng bằng kỹ thuật Prompting Nâng cao 

**1. Input (Dữ liệu đầu vào)**

-   Mã đơn hàng.
    
-   Tên khách hàng.
    
-   Tên sản phẩm.
    
-   Số lượng sản phẩm.
    
-   Đơn giá.
    
-   Địa chỉ giao hàng.
    
-   Trạng thái thanh toán.
    

**2. Output (Kết quả đầu ra)**

AI trả về bảng gồm các thông tin:

 -   Mã đơn hàng.

 -   Tên khách hàng
    
 -   Tổng tiền đơn hàng
   
 -   Trạng thái đơn hàng
    
 -   Lỗi dữ liệu (nếu có)
    
 -   Hướng xử lý đề xuất

## **Bước 2: Viết prompt và chạy thử**

**1. Prompt hoàn chỉnh**

Em sử dụng prompt sau:

Bạn là nhân viên hỗ trợ quản lý đơn hàng cho cửa hàng.

**Nhiệm vụ:** Phân tích và xử lý thông tin đơn hàng theo từng bước.

**Input:**

-   Mã đơn hàng: [MA_DON_HANG]
    
-   Tên khách hàng: [TEN_KHACH_HANG]
    
-   Sản phẩm: [TEN_SAN_PHAM]
    
-   Số lượng: [SO_LUONG]
    
-   Đơn giá: [DON_GIA]
    
-   Địa chỉ: [DIA_CHI]
    
-   Thanh toán: [TRANG_THAI_THANH_TOAN]
    

**Quy trình xử lý (Prompt Chaining):**

1.  Kiểm tra tính đầy đủ và hợp lệ của dữ liệu.
    
2.  Nếu dữ liệu hợp lệ, tính tổng tiền = số lượng × đơn giá.
    
3.  Xác định trạng thái đơn hàng.
    
4.  Tổng hợp kết quả và đề xuất hướng xử lý

**2. Chạy thử thực tế**

Dữ liệu đầu vào:

-   Mã đơn hàng: DH001
    
-   Tên khách hàng: Nguyễn Văn A
    
-   Sản phẩm: Bàn phím
    
-   Số lượng: 2
    
-   Đơn giá: 300.000 đồng
    
-   Địa chỉ: Hà Nội
    
-   Thanh toán: Đã thanh toán

**Thử nghiệm dữ liệu lỗi:**

Nếu số lượng bị bỏ trống, AI trả về:

-   Trạng thái: Thiếu dữ liệu.
    
-   Lỗi: Chưa có số lượng sản phẩm.
    
-   Hướng xử lý: Yêu cầu bổ sung số lượng trước khi tính tiền


