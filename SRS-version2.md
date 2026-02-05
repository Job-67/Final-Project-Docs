# Software Requirements Specification (SRS) - Version 2.0 (Proposed)

**Project Name:** ComTech Prep - Enhanced Edition  

**Focus:** Backend Integration, AI Assistance, and Collaboration  

  

## 1. Introduction

Version 2.0 aims to transform the standalone learning tool into a fully integrated educational platform. This version introduces backend persistence, real-time collaboration between users, and AI-driven tutoring to provide personalized learning experiences.

  

## 2. Advanced Functional Requirements

  

### 2.1 Backend & Data Persistence

- **Database Integration:** Connect to PostgreSQL to save:

    - User progress, XP, and inventory.

    - Saved code snippets and flowchart projects.

    - Mission completion history.

- **API Development:** RESTful or GraphQL API for data synchronization between client and server.

- **Security:** JWT-based authentication and secure session management.

  

### 2.2 Intelligent Tutoring System (AI)

- **Code Analysis:** Integration with LLMs (e.g., OpenAI, Gemini API) to analyze student code.

    - *Feature:* "Get Hint" button that provides context-aware suggestions without revealing the answer.

    - *Feature:* Automatic code optimization suggestions.

- **Personalized Path:** Adjust mission difficulty based on user performance (Adaptive Learning).

  

### 2.3 Integrated Logic-to-Code System

- **Flowchart-to-Python Converter:**

    - Users can draw a flowchart, and the system automatically generates the corresponding Python syntax.

- **Python-to-Flowchart Visualization:**

    - Users paste Python code, and the system renders a visual flowchart to explain the logic.

- **Sync Mode:** Split-screen view where changes in the flowchart update the code in real-time (and vice versa).

  

### 2.4 Collaboration & Social Features

- **Real-time Multiplayer Lab:**

    - Pair Programming: Two users can edit the same code file simultaneously (using WebSockets/Yjs).

    - Collaborative Flowcharting: Teams can design logic diagrams together.

- **Classrooms:**

    - Teachers can create rooms, assign missions, and view student analytics.

    - Code Review system for peer-to-pair reviews.

  

### 2.5 Advanced Assessment

- **Unit Testing Engine:**

    - Ability to run hidden test cases against student code to verify correctness beyond simple output matching.

- **Plagiarism Detection:**

    - Heuristic analysis to check if code submission is too similar to other students.

  

### 2.6 Enhanced Gamification

- **Shop System:** Spend earned XP to buy avatar customizations or themes.

- **Achievements:** Badges for specific milestones (e.g., "Bug Hunter", "Speed Coder").

  

## 3. Technical Architecture Upgrades

- **Backend:** Node.js with Express/NestJS or Python FastAPI.

- **Database:** PostgreSQL with Prisma or TypeORM.

- **Real-time:** Socket.io for collaboration features.

- **AI:** LangChain for orchestrating LLM interactions.

- **Deployment:** Docker containers for consistent environment deployment.

  

## 4. User Scenarios (Version 2)

1.  **Scenario A:** A student is stuck on a loop logic. They ask the AI Assistant, which highlights the specific line causing the infinite loop and explains *why* it's happening.

2.  **Scenario B:** A teacher assigns a "Sorting Algorithm" mission. Students build the flowchart collaboratively in groups of two. Once finished, they convert it to Python code with one click and submit it for automated grading.


---

# เอกสารข้อกำหนดความต้องการทางซอฟต์แวร์ (SRS) - เวอร์ชัน 2.0 (ฉบับเสนอปรับปรุง)

**ชื่อโครงการ:** ComTech Prep - Enhanced Edition (ฉบับยกระดับประสิทธิภาพ)

**ขอบเขตเน้นพัฒนา:** การบูรณาการระบบหลังบ้าน, ระบบช่วยเหลือด้วย AI และการทำงานร่วมกัน

**วันที่:** 4 กุมภาพันธ์ 2026

---

## 1. บทนำ (Introduction)

วัตถุประสงค์ของเวอร์ชัน 2.0 คือการเปลี่ยนผ่านจากเครื่องมือการเรียนรู้แบบสแตนด์อโลน (Standalone) สู่การเป็น **แพลตฟอร์มการศึกษาแบบบูรณาการเต็มรูปแบบ** โดยจะมีการเพิ่มระบบจัดเก็บข้อมูลหลังบ้าน (Backend Persistence) การทำงานร่วมกันแบบเรียลไทม์ระหว่างผู้ใช้งาน และระบบติวเตอร์อัจฉริยะที่ควบคุมด้วย AI เพื่อมอบประสบการณ์การเรียนรู้ที่เหมาะสมกับบุคคล (Personalized Learning)

---

## 2. ความต้องการด้านฟังก์ชันระดับก้าวหน้า (Advanced Functional Requirements)

### 2.1 ระบบหลังบ้านและการจัดเก็บข้อมูลถาวร (Backend & Data Persistence)

- **การบูรณาการฐานข้อมูล:** เชื่อมต่อกับ PostgreSQL เพื่อจัดเก็บข้อมูลดังนี้:
    
    - ความคืบหน้าของผู้ใช้, แต้มประสบการณ์ (XP) และไอเทมในคลัง
        
    - ส่วนของโค้ด (Code Snippets) และโปรเจกต์ผังงานที่บันทึกไว้
        
    - ประวัติการทำภารกิจสำเร็จ
        
- **การพัฒนา API:** พัฒนา RESTful หรือ GraphQL API เพื่อประสานข้อมูลระหว่างเครื่องผู้ใช้และเซิร์ฟเวอร์
    
- **ความปลอดภัย:** ใช้ระบบยืนยันตัวตนแบบ JWT (JSON Web Token) และการจัดการเซสชันที่ปลอดภัย
    

### 2.2 ระบบการสอนอัจฉริยะ (Intelligent Tutoring System - AI)

- **การวิเคราะห์รหัสโปรแกรม:** บูรณาการกับโมเดลภาษาขนาดใหญ่ (LLMs เช่น OpenAI, Gemini API) เพื่อวิเคราะห์โค้ดของนักเรียน
    
    - **ฟีเจอร์ "คำใบ้" (Get Hint):** ให้คำแนะนำตามบริบทโดยไม่เฉลยคำตอบโดยตรง
        
    - **ฟีเจอร์การเพิ่มประสิทธิภาพโค้ด:** ให้ข้อเสนอแนะในการปรับปรุงโค้ดให้ดีขึ้นอัตโนมัติ
        
- **เส้นทางการเรียนรู้เฉพาะบุคคล:** ปรับระดับความยากของภารกิจตามความสามารถของผู้ใช้ (Adaptive Learning)
    

### 2.3 ระบบเชื่อมโยงตรรกะสู่รหัสโปรแกรม (Integrated Logic-to-Code System)

- **ตัวแปลงผังงานเป็น Python (Flowchart-to-Python):** ผู้ใช้สามารถวาดผังงาน และระบบจะสร้างไวยากรณ์ Python ที่สอดคล้องกันโดยอัตโนมัติ
    
- **ตัวแปลง Python เป็นผังงาน (Python-to-Flowchart):** เมื่อผู้ใช้วางโค้ด Python ระบบจะสร้างผังงานเพื่ออธิบายตรรกะให้เห็นเป็นภาพ
    
- **โหมดซิงค์ (Sync Mode):** หน้าจอแยก (Split-screen) ที่การแก้ไขในผังงานจะอัปเดตโค้ดแบบเรียลไทม์ (และในทางกลับกัน)
    

### 2.4 ฟีเจอร์การทำงานร่วมกันและสังคม (Collaboration & Social Features)

- **ห้องปฏิบัติการแบบผู้เล่นหลายคนเรียลไทม์:**
    
    - **การเขียนโปรแกรมคู่ (Pair Programming):** ผู้ใช้สองคนสามารถแก้ไขไฟล์โค้ดเดียวกันได้พร้อมกัน (ผ่าน WebSockets)
        
    - **การสร้างผังงานร่วมกัน:** ทีมสามารถช่วยกันออกแบบแผนภาพตรรกะได้ในเวลาเดียวกัน
        
- **ระบบห้องเรียน (Classrooms):**
    
    - ผู้สอนสามารถสร้างห้องเรียน มอบหมายภารกิจ และดูสถิติการเรียนรู้ของนักเรียนได้
        
    - ระบบตรวจทานโค้ด (Code Review) สำหรับการตรวจทานระหว่างเพื่อนร่วมชั้น
        

### 2.5 การประเมินผลขั้นสูง (Advanced Assessment)

- **ระบบทดสอบหน่วยโปรแกรม (Unit Testing Engine):** ความสามารถในการรันชุดทดสอบที่ซ่อนอยู่ (Hidden Test Cases) เพื่อตรวจสอบความถูกต้องของโค้ดมากกว่าแค่การดูผลลัพธ์
    
- **การตรวจจับการคัดลอก (Plagiarism Detection):** ใช้การวิเคราะห์ฮิวริสติกเพื่อตรวจสอบความคล้ายคลึงของซอร์สโค้ดระหว่างผู้เรียน
    

---

## 3. การปรับปรุงสถาปัตยกรรมทางเทคนิค (Technical Architecture Upgrades)

| **องค์ประกอบ**       | **เทคโนโลยีที่เลือกใช้**                            |
| -------------------- | --------------------------------------------------- |
| **Backend**          | Node.js (Express/NestJS) หรือ Python (FastAPI)      |
| **Database**         | PostgreSQL พร้อม Prisma หรือ TypeORM                |
| **Real-time**        | Socket.io สำหรับฟีเจอร์การทำงานร่วมกัน              |
| **AI Orchestration** | LangChain สำหรับจัดการการโต้ตอบกับ LLM              |
| **Deployment**       | Docker containers เพื่อความเสถียรของสภาพแวดล้อมระบบ |

---

## 4. สถานการณ์จำลองผู้ใช้ (User Scenarios)

1. **สถานการณ์ ก:** นักเรียนติดปัญหาเรื่องตรรกะการวนซ้ำ (Loop) จึงกดขอความช่วยเหลือจาก AI Assistant ซึ่งจะทำการไฮไลต์บรรทัดที่ทำให้เกิดการวนซ้ำไม่สิ้นสุด (Infinite Loop) พร้อมอธิบายสาเหตุที่เกิดขึ้น
    
2. **สถานการณ์ ข:** ผู้สอนมอบหมายภารกิจ "อัลกอริทึมการเรียงลำดับ" นักเรียนร่วมกันสร้างผังงานเป็นคู่ เมื่อเสร็จสิ้นสามารถแปลงเป็นโค้ด Python ได้ในคลิกเดียวและส่งงานเพื่อรับการตรวจคะแนนอัตโนมัติ
    

---
