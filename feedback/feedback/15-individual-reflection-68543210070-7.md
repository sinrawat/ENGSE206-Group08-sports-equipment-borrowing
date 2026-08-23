# 15 — Individual Reflection (Requirement Baseline Review v1.0)

> **Case Project:** Case-08 — ระบบยืม–คืนอุปกรณ์กีฬาและกิจกรรม
> **Course / Week:** ENGSE206 / Week 05 Consolidation Studio
> **Date:** 18 สิงหาคม 2569

---

## ศิลวัต อาซอง

### Student Information
| Field | Detail |
|---|---|
| Student ID | 68543210070-7 |
| Name | ศิลวัต อาซอง |
| Primary Role(s) | Lead Interviewer, Requirements Lead, Traceability Auditor |

### 1. My Contribution
รับหน้าที่เป็น Lead Interviewer ตั้งแต่ Week 3–4 (สัมภาษณ์นักศึกษา/ผู้ยืม และเจ้าหน้าที่/ผู้บริหาร ตาม `03-interview-guide.md`) และในรอบ Baseline Review รับหน้าที่ Traceability Auditor ไล่สายย้อนกลับจาก Must Requirements (`FR-EQP-01, FR-EQP-02, FR-EQP-03, FR-EQP-06, FR-EQP-07, NFR-EQP-01`) ไปยัง Evidence (`E-01, E-02, E-05, E-06, E-07`) และ Need (`N-01, N-02, N-05`) ใน 05-requirement-backlog-v0.2.md

### 2. What I Learned About Requirements and Design
วันนี้เข้าใจชัดขึ้นว่า Baseline ไม่ใช่แค่การรวบรวมไฟล์ให้ครบ แต่คือการหยุดตรวจสอบว่าความต้องการทุกข้อมีที่มาจากหลักฐานจริง และไม่หลุด Scope จาก Case Card การล็อก Baseline v1.0 ช่วยให้ทีมมีฐานความต้องการที่สะอาดและมั่นใจก่อนนำไปสร้าง User Story และ Use Case ใน Week 06

### 3. A Decision I Influenced
ผลักดันให้ทีมไม่ฟันธงเกณฑ์ "อุปกรณ์พิเศษ" (ราคา/รายการ) เองในตอนที่ทำ FR-EQP-04 แม้จะเสียเวลากว่าการเดา แต่ยืนยันให้คงไว้เป็น Open Question (`OQ-EQP-01`) และ Priority ที่ Should แทน Must เพราะ evidence (`E-03`) ยังไม่ยืนยันเกณฑ์ชัดเจน ช่วยให้ Requirement Backlog สะท้อนเฉพาะความต้องการที่มีหลักฐานรองรับจริง

### 4. Feedback I Received and How I Responded
ได้รับ Feedback จาก Peer Cross-Review ว่า FR-EQP-01 ("บันทึกและค้นหาประวัติการยืม–คืน") ยังไม่มีตัวเลขตรวจรับได้ (ไม่ระบุช่วงเวลาย้อนหลังหรือเวลาตอบสนอง) จึงรับไปร่างข้อเสนอเบื้องต้นว่าควรค้นย้อนหลังได้อย่างน้อยกี่เดือน ภายในกี่วินาที เพื่อนำเข้าที่ประชุมทีมก่อนล็อก baseline

### 5. What I Would Improve Next Time
ในคาบถัดไปจะเตรียมแยก FR-EQP-01 ออกเป็นสองความสามารถ (บันทึก vs ค้นหา) ตามแนวทางเดียวกับที่ทีมเคยแยก RC-02 เป็น `FR-EQP-02`/`FR-EQP-03` เพื่อให้ atomic และตรวจรับได้ง่ายขึ้น

### 6. Answers to Reflection Questions
1. **วันนี้ฉันเข้าใจอะไรชัดขึ้นเกี่ยวกับ requirement ของทีม?**
   เข้าใจว่า Requirement ที่ดีต้องวัดผลได้จริง (Verifiable) และทุกข้อลากย้อนกลับไปยังหลักฐานการสัมภาษณ์และ Pain Point ของผู้ใช้ได้โดยไม่มี Requirement ลอย
2. **จุดที่ทีมเรายังอ่อนที่สุดคืออะไร และจะทำอย่างไรต่อ?**
   จุดที่ยังอ่อนที่สุดคือ "การจัดการผู้คืนอุปกรณ์ล่าช้า" (`ISSUE-EQP-04` / `OQ-EQP-06`) ซึ่งไม่มี evidence จากการสัมภาษณ์ Week 4 มารองรับเลย ทีมจึงยังออกแบบสถานะ "ค้างคืน" ไม่ได้ ต้องสัมภาษณ์เพิ่มก่อน Week 06 ด้วยคำถามที่ตรงประเด็นกว่าเดิม
3. **คำถามที่อยากถามอาจารย์ในคาบหน้า (Week 6) คือ...**
   การเรียกคืนอุปกรณ์ก่อนกำหนด (`FR-EQP-05`) กับการคืนล่าช้าของผู้ยืม (`ISSUE-EQP-04`) ควรออกแบบเป็น State Machine เดียวกันของสถานะการยืม หรือแยกเป็นสองกลไกที่ทำงานอิสระต่อกัน?
