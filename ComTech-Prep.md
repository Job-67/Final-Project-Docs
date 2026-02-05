### วัฒนธรรมและกฎในการเขียนโค้ดรวมถึงการทำงานร่วมกันภายในทีม
 ---
### วัฒนธรรมการทำงานร่วมกัน (Collaboration Culture)

 - การแบ่งบทบาทหน้าที่อย่างชัดเจน (Task Assignment): ทีมมีการแบ่งงานออกเป็น 2 ฝ่ายหลัก คือ ==ทีม A (ฝ่ายเนื้อหาและกราฟิก) ที่ดูแลเรื่อง Storyboarding และการหา Asset== และ ==ทีม B (ฝ่ายพัฒนาโปรแกรม) ที่ดูแล Database, Frontend และ Game Logic==
 - การสื่อสารผ่านโครงสร้างข้อมูลที่เป็นมาตรฐาน: ทีมใช้ไฟล์ Excel เป็นสื่อกลางในการส่งต่อเนื้อหาบทสนทนา (Scripts) ระหว่างทีมเนื้อหาและทีมพัฒนา โดยต้องระบุข้อมูลให้ครบ 7 หัวข้อหลัก (เช่น Scene ID, Character, Text) เพื่อให้ทีมพัฒนาสามารถนำไปลงฐานข้อมูลได้ทันที
 - การวิเคราะห์ความปลอดภัยล่วงหน้า: สมาชิกในทีมต้องทำงานร่วมกันเพื่อสร้าง ==แบบจำลองภัยคุกคาม (Threat Modeling)== และ==แผนผังกระแสข้อมูล (DFD)== เพื่อวิเคราะห์ความเสี่ยงของแอปพลิเคชันก่อนหรือระหว่างการพัฒนา
 - การรักษาเวลา (Punctuality): มีเกณฑ์การส่งงานตรงเวลา 

---
### กฎของการเขียน Code และการพัฒนา (Coding & Development Rules)

kebab-case = ตัวพิมพ์เล็กทั้งหมด คั่นด้วย `-`

- ชื่อโฟลเดอร์
- ชื่อไฟล์ static
- class ของ CSS / Tailwind (แนวคิดเดียวกัน)
- ชื่อ markdown

PascalCase = ตัวอักษรตัวแรกของทุกคำเป็นตัวพิมพ์ใหญ่

 - React Component
- Class
- Type / Interface
- Enum

camelCase = คำแรกตัวเล็ก คำถัดไปขึ้นต้นตัวใหญ่

- ตัวแปร (variable)
- ฟังก์ชัน (function)
- props
- state
- custom hooks (ขึ้นต้นด้วย `use`)

snake_case = ตัวพิมพ์เล็ก คั่นด้วย `_`

- backend
- database
- API response  
- ไม่แนะนำใน React / Frontend

SCREAMING_SNAKE_CASE

- constant
- environment variable

Comment

เขียนแบบ English โดยใช้พิมเล็กทั้งหมด ยกเว้น ชื่อย่อ เช่น API JWT

---

| ใช้กับ | Case |
|------|------|
| Folder | kebab-case |
| Component | PascalCase |
| File Component | PascalCase.tsx |
| Variable / Function | camelCase |
| Hook | camelCase (`useX`) |
| Type / Interface | PascalCase |
| Constant | SCREAMING_SNAKE_CASE |
| Tailwind class | kebab-case |




