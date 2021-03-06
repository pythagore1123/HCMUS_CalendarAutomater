# HCMUS_CalendarAutomater
*Project này hỗ trợ việc tự động đưa lịch học của sinh viên trường Đại học Khoa học Tự nhiên (HCMUS) lên Google Calendar*

## Lưu ý

Các sự kiện sẽ được để chế độ lặp lại, do đó lịch học sẽ được lặp lại mãi mãi. Vì vậy, khi qua học kì mới, ta cần xoá đi lịch của học kì cũ (có thể tự xoá bằng tay).

## Cài đặt

Tải repository này về máy (tạm gọi thư mục đó là `HCMUS_CalendarAutomater`), sau đó chạy dòng lệnh sau đây ở *command prompt/terminal* để cài đặt API.

>pip install --upgrade google-api-python-client google-auth-httplib2 google-auth-oauthlib

Sau đó, tới [link này](https://developers.google.com/calendar/quickstart/python) để download file `credentials.json` vào thư mục `HCMUS_CalendarAutomater`.

Sau đó, vào portal của trường ([tại đây](http://portal.hcmus.edu.vn)), đăng nhập tài khoản sinh viên, vào `Đăng ký học phần` -> `Kết quả ĐKHP`. Lưu HTML của trang đó vào thư mục `HCMUS_CalendarAutomater` bằng cách nhấn Ctrl + S, lưu với tên là `TKB.html`.

Tới bước này, trong thư mục `HCMUS_CalendarAutomater` cần có các file sau đây:
  - HCMUS_CalendarAutomater.py 
  - config.json
  - crawlHTML.py
  - postCalendar.py
  - credentials.json 
  - TKB.html 

Rồi chạy code bằng lệnh `python HCMUS_CalendarAutomater.py` ở *command prompt/terminal*

## Contribution

Thanks [Duy Thuc Le](https://github.com/leduythuccs) for parsing from raw HTML to JSON database.

Thanks [Dinh Hai Le](https://github.com/pythagore1123) for uploading database with Calendar API.
