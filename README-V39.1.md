# PE League V39.1 — Tournament & Google Sheets safety update

ฐานจาก V39 เท่านั้น

## Google Sheets
- `Leaderboard` แสดงเฉพาะรายการ/Season ที่กำลังเลือกและกำลังแข่งขันอยู่
- `Leaderboard_History` เก็บตารางของรายการที่จบแล้วแยกออกจาก Leaderboard ปัจจุบัน
- การสร้าง Season ใหม่จะไม่ทำให้ประวัติ Leaderboard เก่าหายจากข้อมูลสำรอง
- `Seasons`, `Matches`, `Standings` ระบุประเภทและเลข Tournament เพื่อแยก League / UCL / FA Cup
- UCL ใช้เลข `UCL 1, UCL 2, ...` แยกจาก `Season 1, Season 2, ...`
- FA Cup ใช้เลข `FA Cup 1, FA Cup 2, ...` แยกจาก League เช่นกัน

## สำคัญ
หลังติดตั้งไฟล์นี้ ให้แทนโค้ด Apps Script เดิมด้วย `google-apps-script.gs` ใน ZIP และ Deploy เป็น Web App เวอร์ชันใหม่
