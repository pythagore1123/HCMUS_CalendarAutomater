# HCMUS_CalendarAutomater
*A kindly simple way to have your HCMUS's timetable posted on Google Calendar*
>(Vietnamese in [README-vi.md](README-vi.md))

## Note

Because each event will be set to recursion event, the schedule will repeat weekly forever. If you enter a new semester with a new schedule, please delete those recursion events by hand.

## Installation

Clone this repository, then run this line on *command prompt/terminal* to install dependencies

>pip install --upgrade google-api-python-client google-auth-httplib2 google-auth-oauthlib

After that, go to [this link](https://developers.google.com/calendar/quickstart/python) to download your `credentials.json` file to the current folder (and/or you can start reading tutorials from there and modify as you wish).

Then, access the [school's portal](http://portal.hcmus.edu.vn/), log in and go to `Đăng kí học phần > Kết quả ĐKHP`. Save the page's html with `Ctrl + s` as `TKB.html` in the cloned folder, which is `HCMUS_CalendarAutomater`.

Uptill now, files existing in current folder(`HCMUS_CalendarAutomater`) are:
* HCMUS_CalendarAutomater.py
* config.json
* crawlHTML.py
* postCalendar.py
* credentials.json
* TKB.html

Then run the code with command `python main.py` 

## Config

If you want to update timetable of the current week, set `week` attribute as `this` inside `config.json` file, and if you want to update the upcoming week, set `week` as `that`. 

If you want to loop the schedule forever (you can delete it later), set `loop` to `true`, otherwise you can set it to anything.

## Contribution

Thanks [Duy Thuc Le](https://github.com/leduythuccs) for parsing from raw HTML to JSON database.

Thanks [Dinh Hai Le](https://github.com/pythagore1123) for uploading database with Calendar API.
