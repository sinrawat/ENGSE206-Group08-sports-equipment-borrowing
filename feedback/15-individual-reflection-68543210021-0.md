# 15 — Individual Reflection (Requirement Baseline Review v1.0)

> **Case Project:** Case-08 — ระบบยืม–คืนอุปกรณ์กีฬาและกิจกรรม
> **Course / Week:** ENGSE206 / Week 05 Consolidation Studio
> **Date:** 18 สิงหาคม 2569
> (ฉบับร่างจากข้อมูลโปรเจกต์จริงของทีม — โปรดอ่านทบทวนและปรับให้ตรงกับความรู้สึก/ประสบการณ์จริงของตนเองก่อนส่ง)

---

## กิตติภพ สว่างเจริญทรัพย์

### Student Information
| Field | Detail |
|---|---|
| Student ID | 68543210021-0 |
| Name | กิตติภพ สว่างเจริญทรัพย์ |
| Primary Role(s) | Evidence Controller, Quality Reviewer, Scribe |

### 1. My Contribution
รับหน้าที่เป็น Evidence Controller/Quality Reviewer ตั้งแต่ Week 3 (ตรวจสอบความครบถ้วนและความน่าเชื่อถือของหลักฐาน และตรวจว่าคำถามสัมภาษณ์ไม่ชี้นำ ตาม `03-elicitation-plan.md`) และในรอบ Baseline Review รับหน้าที่ Scribe บันทึกผลการตรวจคุณภาพ พร้อมตรวจสอบว่า Requirement แต่ละข้อเป็น Atomic ไม่กำกวม โดยเฉพาะการแยก RC-02 เป็น FR-EQP-02 (บันทึกสภาพ) กับ FR-EQP-03 (ดู/เข้าถึงหลักฐาน) และแยก RC-05 เป็น FR-EQP-06 (แสดงสถานะ) กับ FR-EQP-07 (ป้องกันจองซ้ำ)

### 2. What I Learned About Requirements and Design
วันนี้เข้าใจชัดขึ้นว่าความสามารถของระบบที่ดูเหมือนเป็นเรื่องเดียวกัน (เช่น "บันทึกสภาพอุปกรณ์" กับ "ดูหลักฐาน") จริงๆ แล้วเป็นคนละ concern กัน ควรแยกเป็น requirement คนละข้อเพื่อให้ตรวจรับและ trace ไปยัง Acceptance Criteria ได้อย่างชัดเจน ไม่ปนกันจนทดสอบยาก

### 3. A Decision I Influenced
เสนอให้แยก Evidence-based scope ของ FR-EQP-08 (dashboard) ออกเป็นสองส่วนอย่างชัดเจน — ส่วนสรุปการใช้งาน/สถานะที่มี evidence รองรับ (`E-08`) ให้เข้า backlog ได้ที่ priority Could ส่วนคำแนะนำจัดซื้อ/งบประมาณให้แยกเป็น ISSUE-EQP-01 และ Hold ไว้รอ scope owner ยืนยัน เพื่อไม่ให้ requirement บวมเกินขอบเขตเดิมของ Week 2

### 4. Feedback I Received and How I Responded
ได้รับ Feedback จาก Peer Cross-Review ว่า FR-EQP-01 ยังรวมสองความสามารถไว้ในข้อเดียว (บันทึก + ค้นหา) ไม่ atomic เท่าที่ควรเมื่อเทียบกับ `FR-EQP-02`/`03` จึงรับไปเสนอในที่ประชุมทีมว่าควรแยกตามแนวทางเดียวกันในรอบแก้ไขก่อนล็อก baseline

### 5. What I Would Improve Next Time
จะจัดทำ checklist ตรวจ Atomicity (1 requirement = 1 ความสามารถที่ตรวจรับแยกได้) ให้เป็นขั้นตอนมาตรฐานตั้งแต่ตอนร่าง Requirement Candidate ใน Week 04 แทนที่จะมาพบปัญหาตอน Quality Review ของ Week 05

### 6. Answers to Reflection Questions
1. **วันนี้ฉันเข้าใจอะไรชัดขึ้นเกี่ยวกับ requirement ของทีม?**
   เข้าใจว่าการตรวจ "ไม่กำกวม/ซ้ำ" (Atomic & Unambiguous) ไม่ใช่แค่เรื่องถ้อยคำ แต่คือการแยกความรับผิดชอบของแต่ละ requirement ให้ทดสอบและตรวจรับแยกจากกันได้จริง
2. **จุดที่ทีมเรายังอ่อนที่สุดคืออะไร และจะทำอย่างไรต่อ?**
   เกณฑ์ "อุปกรณ์พิเศษ" (`ISSUE-EQP-03`) ยังไม่มีตัวเลข/รายการยืนยัน การเดาเกณฑ์เองเสี่ยงออกแบบ role/permission ผิด ทีมจะขอเอกสารเกณฑ์ราคาหรือรายการอุปกรณ์จากหัวหน้าศูนย์กีฬาก่อน Week 06
3. **คำถามที่อยากถามอาจารย์ในคาบหน้า (Week 6) คือ...**
   ในการเขียน Acceptance Criteria ของ `FR-EQP-02`/`FR-EQP-03` (หลักฐานภาพถ่ายสภาพอุปกรณ์) ควรใช้ Gherkin scenario แยกเป็นคนละไฟล์ตาม requirement หรือรวมเป็น scenario เดียวที่ครอบคลุมทั้ง flow บันทึกและเข้าถึง?
