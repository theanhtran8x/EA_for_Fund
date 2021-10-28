EA Lot_management_for_currency_v01.ex4
- Chức năng: Dùng cho quản lý số lệnh, quản lý tổng số lot và tự động tính số lot, tự động tính điểm TP/SL
- Khuyến cáo khi sử dụng: 
  + Sử dụng trên MT4 và cho các cặp tiền tệ (không đúng khi sử dụng cho tiền ảo, vàng, dầu, chỉ số, chứng khoán)
  + Số tiền càng nhỏ và số percent_default càng nhỏ, thì EA sẽ không chính xác. Vì số lot tối thiểu sẽ là 0.01 lot.
- Nút "SellMarket" và "BuyMarket" là dùng để sell/buy ngay lập tức tại giá hiện tại
- Nút "CloseAll" dùng để đóng tất cả các lệnh đang mở của 1 cặp tiền

- Các biến quan trọng:
+ percent_default: Phần trăm lợi nhuận mong đợi của 1 lệnh. Mặc định là 1%
+ limit_lot_number: Tổng số lot tối đa được phép mở. Nếu tổng số lot đã đạt giới hạng, thì nút "SellMarket" và "BuyMarket" không còn tác dụng
+ limit_lot_check: Nếu biến này = true, thì limit_lot_number mới có hiệu lực.
+ ratio_loss: Tỉ lệ lỗ so với lợi nhuận. Ví dụ nếu giá trị là 100, nghĩa là lỗ và lời sẽ bằng nhau, khi đó độ dài TP và SL bằng nhau.
+ limit_order_each_pair: Số lệnh tối đa được phép mở cho 1 cặp tiền. Nếu số lệnh đã đạt giới hạng, thì nút "SellMarket" và "BuyMarket" không còn tác dụng
+ limit_order_check: Nếu biến này = true, thì limit_order_each_pair mới có hiệu lực.
+ lengh_of_takeprofit: Mặc định là TP = 1.5*(điểm vào lệnh +/- H4 MA200 or H4 BoligerBand). Số này càng cao, thì số lot sẽ càng nhỏ
