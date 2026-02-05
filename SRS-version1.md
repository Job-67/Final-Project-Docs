# Software Requirements Specification (SRS) - Version 1.0

**Project Name:** ComTech Prep (Computer Technology Preparatory Platform)  

**Date:** February 4, 2026  

**Status:** MVP / Client-Side Implementation

  

## 1. Introduction

### 1.1 Purpose

The purpose of ComTech Prep is to provide an interactive, gamified web application for students to learn fundamental computer logic, flowchart design, and Python programming. The platform aims to lower the barrier to entry for coding by running entirely in the browser without complex environment setup.

  

### 1.2 Scope

- **Frontend-Focused:** The current version operates primarily as a Single Page Application (SPA) using React.

- **Client-Side Execution:** Code execution utilizes Pyodide (WebAssembly) to run Python in the browser securely.

- **Target Audience:** Beginners in Computer Science and Technology.

  

## 2. Functional Requirements

  

### 2.1 User Authentication

- Users can register for a new account.

- Users can log in to access the dashboard and missions.

- **Current State:** UI/UX implementation for Login/Register pages exists.

  

### 2.2 Dashboard & Progression

- **Overview:** Displays user profile, current level, XP, and rank.

- **Visualization:** Charts (Radar, Line) showing skills analysis (Logic, Syntax, Algorithm, Debugging).

- **Gamification:**

    - XP System: Users gain experience points from completing tasks.

    - Daily Quests: List of daily tasks to encourage engagement.

    - Leaderboard: Ranking display of top learners.

  

### 2.3 Learning System (Missions)

- **Mission Map:** A visual roadmap of learning stages (locked/unlocked states).

- **Interactive Lessons:**

    - **Visual Novel Style:** Learning concepts through dialogue with a "Mentor" character.

    - **Step-by-Step Logic:** Pseudocode and Logic Flow visualization.

    - **Feedback:** Real-time feedback on user answers.

  

### 2.4 Laboratory (Standalone Tools)

#### 2.4.1 Python Code Editor Lab

- **Environment:** Browser-based Python 3.10 runtime (via Pyodide).

- **Features:**

    - Syntax Highlighting (Custom Tokyo Night theme).

    - Auto-indentation and basic code formatting.

    - **Interactive Input:** Custom modal for handling Python `input()` functions.

    - **Console Output:** Real-time standard output and error display.

    - **Templates:** Pre-filled code for For-Loops, Functions, etc.

  

#### 2.4.2 Flowchart Builder Lab

- **Canvas:** Interactive drag-and-drop canvas (via ReactFlow).

- **Nodes:** Support for Start, End, Process, Decision (Diamond), Input/Output nodes.

- **Features:**

    - Dynamic connection lines.

    - Templates (For Loop, If-Else, Sequential).

    - Export to JSON functionality.

    - Minimap and Zoom controls.

  

## 3. Non-Functional Requirements

- **Performance:** Code execution must happen within the client browser to ensure speed and reduce server cost.

- **Usability:** Interface must support Dark Mode by default for eye comfort during long coding sessions.

- **Responsive Design:** Application acts as a web app accessible on desktop and tablet resolutions.

  

## 4. Technology Stack (Current)

- **Frontend:** React, TypeScript, Vite

- **Styling:** Tailwind CSS

- **State Management:** Context API

- **Core Libraries:**

    - `pyodide`: Python execution.

    - `reactflow`: Flowchart generation.

    - `@monaco-editor/react`: Code editing interface.

    - `recharts`: Data visualization.
 

---

# เอกสารข้อกำหนดความต้องการทางซอฟต์แวร์ (SRS) - เวอร์ชัน 1.0

**ชื่อโครงการ:** ComTech Prep (แพลตฟอร์มเตรียมความพร้อมด้านเทคโนโลยีคอมพิวเตอร์)

**วันที่:** 4 กุมภาพันธ์ 2026

**สถานะ:** ผลิตภัณฑ์ขั้นต่ำ (MVP) / การพัฒนาระบบฝั่งผู้ใช้งาน (Client-Side)

---

## 1. บทนำ (Introduction)

### 1.1 วัตถุประสงค์ (Purpose)

วัตถุประสงค์ของโครงการ ComTech Prep คือการสร้างเว็บแอปพลิเคชันรูปแบบ **Gamified** (การใช้กลไกเกม) เพื่อให้ผู้เรียนสามารถศึกษากระบวนการคิดเชิงตรรกะทางคอมพิวเตอร์ การออกแบบผังงาน (Flowchart) และการเขียนโปรแกรมภาษา Python แพลตฟอร์มนี้มุ่งเน้นการลดอุปสรรคในการเริ่มต้นเรียนรู้การเขียนโปรแกรม โดยสามารถทำงานผ่านเบราว์เซอร์ได้ทันทีโดยไม่ต้องติดตั้งสภาพแวดล้อมการทำงานที่ซับซ้อน

### 1.2 ขอบเขตของโครงการ (Scope)

- **เน้นการพัฒนาฝั่งหน้าบ้าน (Frontend-Focused):** ในเวอร์ชันปัจจุบัน ระบบถูกพัฒนาในรูปแบบ Single Page Application (SPA) โดยใช้ React
    
- **การประมวลผลฝั่งผู้ใช้งาน (Client-Side Execution):** ใช้เทคโนโลยี Pyodide (WebAssembly) เพื่อประมวลผลโค้ด Python บนเบราว์เซอร์ของผู้ใช้อย่างปลอดภัย
    
- **กลุ่มเป้าหมาย:** ผู้เริ่มต้นศึกษาในสาขาวิชาวิทยาการคอมพิวเตอร์และเทคโนโลยี
    

---

## 2. ความต้องการด้านฟังก์ชัน (Functional Requirements)

### 2.1 ระบบยืนยันตัวตนผู้ใช้งาน (User Authentication)

- ผู้ใช้สามารถลงทะเบียนเพื่อสร้างบัญชีใหม่ได้
    
- ผู้ใช้สามารถเข้าสู่ระบบเพื่อเข้าถึงแผงควบคุม (Dashboard) และบทเรียน (Missions)
    
- **สถานะปัจจุบัน:** ดำเนินการออกแบบ UI/UX สำหรับหน้าเข้าสู่ระบบและหน้าลงทะเบียนเรียบร้อยแล้ว
    

### 2.2 ระบบแผงควบคุมและความคืบหน้า (Dashboard & Progression)

- **ภาพรวม:** แสดงข้อมูลส่วนตัวของผู้ใช้ ระดับปัจจุบัน (Level) แต้มประสบการณ์ (XP) และอันดับ (Rank)
    
- **การแสดงผลข้อมูล:** ใช้แผนภูมิ (Radar Chart, Line Chart) เพื่อวิเคราะห์ทักษะในด้านต่าง ๆ อาทิ ตรรกะ (Logic), ไวยากรณ์ (Syntax), อัลกอริทึม (Algorithm) และการหาข้อผิดพลาด (Debugging)
    
- **กลไกเกม (Gamification):**
    
    - **ระบบ XP:** ผู้ใช้จะได้รับแต้มประสบการณ์เมื่อปฏิบัติภารกิจสำเร็จ
        
    - **ภารกิจรายวัน (Daily Quests):** รายการงานประจำวันเพื่อกระตุ้นการใช้งานอย่างต่อเนื่อง
        
    - **ตารางอันดับ (Leaderboard):** แสดงรายชื่อผู้เรียนที่มีคะแนนสูงสุด
        

### 2.3 ระบบการเรียนรู้ (Learning System/Missions)

- **แผนที่ภารกิจ (Mission Map):** แสดงเส้นทางการเรียนรู้ในรูปแบบ Visual Roadmap (รองรับสถานะการล็อก/ปลดล็อกบทเรียน)
    
- **บทเรียนเชิงโต้ตอบ:**
    
    - **รูปแบบวิชวลโนเวล (Visual Novel Style):** การสอนเนื้อหาผ่านบทสนทนาระหว่างผู้เรียนและตัวละคร "เมนเทอร์" (Mentor)
        
    - **ตรรกะแบบเป็นลำดับขั้นตอน:** การแสดงภาพรวมของรหัสเทียม (Pseudocode) และผังงาน (Logic Flow)
        
    - **ระบบตอบรับ:** การให้ข้อเสนอแนะแบบเรียลไทม์ตามคำตอบของผู้ใช้งาน
        

### 2.4 ห้องปฏิบัติการ (Laboratory - Standalone Tools)

#### 2.4.1 ห้องปฏิบัติการเขียนโค้ด Python (Python Code Editor Lab)

- **สภาพแวดล้อม:** ใช้ Python 3.10 Runtime ทำงานบนเบราว์เซอร์ผ่าน Pyodide
    
- **คุณสมบัติ:**
    
    - การเน้นไวยากรณ์ (Syntax Highlighting) ด้วยธีม Tokyo Night
        
    - ระบบเยื้องบรรทัดอัตโนมัติ (Auto-indentation) และการจัดรูปแบบโค้ดพื้นฐาน
        
    - **ส่วนรับข้อมูลเชิงโต้ตอบ:** ใช้ Modal หน้าต่างป๊อปอัปเพื่อรองรับฟังก์ชัน `input()` ของ Python
        
    - **ส่วนแสดงผล (Console):** แสดงผลลัพธ์มาตรฐาน (Standard Output) และข้อผิดพลาด (Error) แบบเรียลไทม์
        

#### 2.4.2 ห้องปฏิบัติการสร้างผังงาน (Flowchart Builder Lab)

- **พื้นที่ทำงาน:** พื้นที่ลากและวางส่วนประกอบแบบโต้ตอบ (พัฒนาโดย ReactFlow)
    
- **โหนด (Nodes):** รองรับโหนดประเภท Start, End, Process, Decision (สี่เหลี่ยมข้าวหลามตัด) และ Input/Output
    
- **คุณสมบัติ:**
    
    - เส้นเชื่อมต่อโหนดแบบไดนามิก (Dynamic Connection Lines)
        
    - แม่แบบสำเร็จรูป (Templates) เช่น For Loop, If-Else และ Sequential
        
    - ฟังก์ชันการส่งออกข้อมูล (Export) เป็นไฟล์ JSON
        
    - ระบบแผนที่ย่อ (Minimap) และการควบคุมการซูม (Zoom Controls)
        

---

## 3. ความต้องการที่มิใช่ฟังก์ชัน (Non-Functional Requirements)

- **ประสิทธิภาพ (Performance):** การประมวลผลโค้ดต้องเกิดขึ้นภายในเบราว์เซอร์ฝั่งผู้ใช้งาน เพื่อความรวดเร็วและลดภาระค่าใช้จ่ายของเซิร์ฟเวอร์
    
- **ความง่ายในการใช้งาน (Usability):** ส่วนต่อประสานผู้ใช้ต้องรองรับโหมดมืด (Dark Mode) เป็นค่าเริ่มต้น เพื่อถนอมสายตาขณะใช้งานเป็นเวลานาน
    
- **การออกแบบที่ยืดหยุ่น (Responsive Design):** แอปพลิเคชันต้องรองรับการแสดงผลทั้งบนคอมพิวเตอร์ตั้งโต๊ะ (Desktop) และแท็บเล็ต
    

---

## 4. รายการเทคโนโลยีที่ใช้ (Technology Stack)

- **ส่วนหน้าบ้าน (Frontend):** React, TypeScript, Vite
    
- **การตกแต่งสไตล์ (Styling):** Tailwind CSS
    
- **การจัดการสถานะ (State Management):** Context API
    
- **ห้องสมุดซอฟต์แวร์หลัก (Core Libraries):**
    
    - `pyodide`: สำหรับการประมวลผลภาษา Python
        
    - `reactflow`: สำหรับการสร้างผังงาน
        
    - `@monaco-editor/react`: สำหรับส่วนแก้ไขโค้ด (Code Editor)
        
    - `recharts`: สำหรับการแสดงผลแผนภูมิข้อมูล
        

---
