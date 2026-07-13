ENGSE203 LAB 02 — Modern JavaScript Dashboard
ผู้จัดทำ
Student ID: 68543210001-2

Name: นาย กฤษณพงศ์ ชัยสุ

Operating system: Windows + WSL

GitHub Repository: https://github.com/Kitsanapong-F/engse203-lab02-68543210001-2

วัตถุประสงค์ของงาน
โปรเจกต์นี้เป็นส่วนหนึ่งของ Lab 02 ในรายวิชา ENGSE203 (Modern JavaScript, Modules & Async Data) โดยเป็นการพัฒนา Learning Dashboard ด้วย JavaScript สมัยใหม่ (Vanilla JavaScript / ES Modules) เพื่อฝึกการออกแบบโครงสร้างโค้ดที่เป็นระเบียบ (Separation of Concerns) และรองรับการดึงข้อมูลแบบ Asynchronous โดย Dashboard แสดงผลข้อมูลการเรียนรู้แบบไดนามิก รองรับทั้งสถานะปกติและสถานะเมื่อเกิดข้อผิดพลาด พร้อมทั้ง deploy ขึ้น GitHub Pages เพื่อให้เข้าถึงได้จริง

โครงสร้างโมดูล (Modules)
NO.	Module	หน้าที่ความรับผิดชอบ
1	api.js	ดึงข้อมูล (data fetching) จาก learning-tasks.json พร้อมจัดการ error handling
2	main.js	Entry point ของแอป, จัดการ state และ event listeners
3	ui.js	รับผิดชอบการ render UI ทั้งหมด และป้องกัน XSS ด้วย escapeHtml()
4	utils.js	ฟังก์ชันช่วยเหลือสำหรับการกรองข้อมูล (filter) และคำนวณสถิติ
วิธีติดตั้งและรันโปรเจกต์
ข้อกำหนดเบื้องต้น (Prerequisites)
Node.js (v22+)

npm

ขั้นตอนการทำ
Bash
# 1. Clone repository
git clone https://github.com/Kitsanapong-F/engse203-lab02-68543210001-2.git
cd engse203-lab02-68543210001-2

# 2. ติดตั้ง dependencies
npm install

# 3. รันโปรเจกต์
npm run dev
คำสั่งที่ใช้งานได้
คำสั่ง	คำอธิบาย
npm install	ติดตั้ง dependencies ทั้งหมดของโปรเจกต์
npm run dev	รันเซิร์ฟเวอร์สำหรับพัฒนา (development server)
npm run build	สร้าง build output สำหรับ production
GitHub Pages URL
🔗 Dashboard ที่ deploy แล้ว: https://kitsanapong-f.github.io/engse203-lab02-68543210001-2/

ปัญหาที่พบและวิธีแก้ไข
ปัญหาที่พบ	สาเหตุ	วิธีแก้ไข
npm command not found	เครื่องที่ใช้ไม่มี Node.js หรือไม่ได้ติดตั้งสภาพแวดล้อมพัฒนา	ติดตั้ง Node.js ผ่าน nvm หรือใช้งานผ่าน GitHub Codespaces
Permission denied	สิทธิ์การเข้าถึงโฟลเดอร์ในเครื่องส่วนกลางจำกัด	ใช้ GitHub Codespaces แทนการติดตั้งลงเครื่องส่วนกลาง
References & AI Assistance
References
async-await_and_error-handling.md

destructuring_array_map_filter_reduce.md

AI Assistance Disclosure
เครื่องมือที่ใช้: Gemini / Claude

ลักษณะการใช้งาน: ช่วยอธิบายแนวคิด ES Modules, ช่วย Debug Error, และช่วยร่างโครงสร้างไฟล์ README

ส่วนที่เขียน/แก้ไขเองโดยผู้เรียน: โค้ดส่วน Logic ทั้งหมดใน src/, การทำ Deployment, และการตั้งค่าโปรเจกต์ตามโจทย์ Lab
