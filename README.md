Bài 1 : Kiểm tra File Log Máy chủ Dung Lượng Lớn


Phần 1 — Phân tích

Trong PowerShell, cat là alias của Get-Content. Lệnh cat server_log_500MB.log vì thế đọc và in toàn bộ nội dung ra Terminal; nó không tự chia trang như less.

Notepad cũng không phù hợp với file 500 MB: việc nạp và hiển thị một lượng văn bản lớn có thể tốn nhiều bộ nhớ và khiến ứng dụng hoặc máy bị chậm, treo.

Phần 2 — Lệnh PowerShell

Xem toàn bộ file theo từng trang:

Get-Content .\server_log_500MB.log | more


Xem 10 dòng cuối:

Get-Content .\server_log_500MB.log -Tail 10

Get-Content phát nội dung theo từng dòng qua pipe; more nhận nội dung để hiển thị từng trang. Tùy chọn -Tail 10 yêu cầu PowerShell lấy 10 dòng cuối.
