Lot_management_for_currency_v02.ex4==================================================================================================
- Chức năng: Dùng cho quản lý số lệnh, quản lý tổng số lot và tự động tính số lot, tự động tính điểm TP/SL và đóng tất cả lệnh đang mở
- Khuyến cáo khi sử dụng: 
   - Sử dụng trên MT4 và cho các cặp tiền tệ, vàng XAUUSD (Số lot sẽ không đúng khi sử dụng cho tiền ảo, dầu, bạc, chỉ số, chứng khoán)
   - Số tiền càng nhỏ và số percent_profit càng nhỏ, thì EA sẽ tính số lot không chính xác. Vì số lot tối thiểu luôn luôn là 0.01 lot, nên số tiền nhỏ thì rủi ro sẽ cao.
- Nút "SellMarket" và "BuyMarket" là dùng để sell/buy ngay lập tức tại giá hiện tại
- Nút "CloseAll" dùng để đóng tất cả các lệnh đang mở của 1 cặp tiền
- Các biến quan trọng:
   - percent_loss: Phần trăm loss mong đợi của 1 lệnh. Mặc định là 1%
   - ratio_loss: Tỉ lệ lỗ so với lợi nhuận. Ví dụ nếu giá trị là 100, nghĩa là lỗ và lời sẽ bằng nhau, khi đó độ dài TP và SL bằng nhau.
   - limit_lot_number: Tổng số lot tối đa được phép mở. Nếu tổng số lot đã đạt giới hạn, thì nút "SellMarket" và "BuyMarket" không còn tác dụng
   - limit_lot_check: Nếu biến này bằng true, thì limit_lot_number mới có hiệu lực.
   - limit_order_each_pair: Số lệnh tối đa được phép mở cho 1 cặp tiền. Nếu số lệnh đã đạt giới hạn, thì nút "SellMarket" và "BuyMarket" không còn tác dụng
   - limit_order_check: Nếu biến này = true, thì limit_order_each_pair mới có hiệu lực.
   - lengh_of_takeprofit_H4: Mặc định là TP = 1.5*(điểm vào lệnh +/- khung giờ H4 MA200 or H4 BolingerBand). Số này càng cao, thì số lot sẽ càng nhỏ và rủi ro càng nhỏ
   - fix_pips_takeprofit: Giá trị takeprofit theo pips. Mặt định là 200 pips. Số này càng cao, thì số lot sẽ càng nhỏ và rủi ro càng nhỏ
   - fix_pips_enable: Mở tính năng take profit theo pips. Nếu biến này bằng true, thì fix_pips_takeprofit mới có hiệu lực và lengh_of_takeprofit_H4 không có ý nghĩa

Lot_management_for_currency_v04.ex4==================================================================================================
- Thêm vào nút "SellLimit" và "BuyLimit"


Lưu ý: Nêm kiểm tra lại và so sánh với kết quả trên https://www.cashbackforex.com/vi/tools/position-size-calculator
