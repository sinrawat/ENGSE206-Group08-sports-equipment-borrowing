# 15 — Individual Reflection (Requirement Baseline Review v1.0)

> **Case Project:** Case-08 — ระบบยืม–คืนอุปกรณ์กีฬาและกิจกรรม
> **Course / Week:** ENGSE206 / Week 05 Consolidation Studio
> **Date:** 18 สิงหาคม 2569
> (ฉบับร่างจากข้อมูลโปรเจกต์จริงของทีม — โปรดอ่านทบทวนและปรับให้ตรงกับความรู้สึก/ประสบการณ์จริงของตนเองก่อนส่ง)

---

## กฤตเมธ สินธุใส

### Student Information
| Field | Detail |
|---|---|
| Student ID | 68543210062-4 |
| Name | กฤตเมธ สินธุใส |
| Primary Role(s) | Facilitator, Timekeeper, Session Lead (Quality Check) |

### 1. My Contribution
รับหน้าที่เป็น Facilitator/Timekeeper ตั้งแต่ Week 3 (สัมภาษณ์+สังเกตการณ์ผู้ดูแลอุปกรณ์ตาม EO-02 ใน `03-elicitation-plan.md`) และในรอบ Baseline Review คุมลำดับและเวลาของ Session Quality Check ที่ปรับถ้อยคำ 05-requirement-backlog.md ให้มีเกณฑ์วัดได้ เช่น FR-EQP-06 (≤ 3 วินาที) และ NFR-EQP-03 (≤ 5 คลิก, 375px)

### 2. What I Learned About Requirements and Design
วันนี้เรียนรู้ว่าคำว่า "ใช้งานง่าย" หรือ "รวดเร็ว" เป็นคำกำกวมทางวิศวกรรมซอฟต์แวร์ที่ทำให้ผู้พัฒนาและผู้ทดสอบเข้าใจไม่ตรงกัน การปรับถ้อยคำให้ระบุเงื่อนไขเวลาและจำนวนคลิกที่ชัดเจนช่วยลดความผิดพลาดตอนออกแบบ UI และ State Diagram ในสัปดาห์ถัดไป

### 3. A Decision I Influenced
นำเสนอ Option B ใน Negotiation Record (`N-01`) ให้ผู้ดูแลอุปกรณ์เป็นผู้อนุมัติการเรียกคืนอุปกรณ์ก่อนกำหนดพร้อมแจ้งเหตุผลและแจ้งล่วงหน้า แทน Option C (auto-recall อัตโนมัติ) เพราะประเมินว่า auto-recall เสี่ยงเรียกคืนผิดกรณีและไม่มีดุลพินิจของมนุษย์ ทำให้ FR-EQP-05 ได้สถานะ Provisional แทนที่จะถูกดันเป็น Approved ทันที

### 4. Feedback I Received and How I Responded
ได้รับ Feedback จาก Peer Cross-Review ว่า FR-EQP-04 และ FR-EQP-05 ยังไม่มีตัวเลข SLA เวลาอนุมัติ และระยะเวลาแจ้งล่วงหน้าขั้นต่ำ จึงรับไปร่างเป็น "ค่าที่เสนอ รอยืนยัน" (proposed value pending confirmation) แทนการปล่อยว่างไว้ เพื่อให้อย่างน้อยมีจุดตั้งต้นให้ผู้มีอำนาจยืนยัน/แก้ไขในการสัมภาษณ์รอบถัดไป

### 5. What I Would Improve Next Time
จะปรับปรุงการบริหารเวลา (Timekeeping) ให้กระชับขึ้นในช่วงอภิปราย Quality Check เพื่อให้เหลือเวลาสำหรับร่าง User Stories ล่วงหน้าสำหรับ Week 06

### 6. Answers to Reflection Questions
1. **วันนี้ฉันเข้าใจอะไรชัดขึ้นเกี่ยวกับ requirement ของทีม?**
   เข้าใจกระบวนการ Traceability Audit ที่ต้องสอบทานให้แน่ใจว่า Requirement สอดคล้องกันตลอดทั้งสาย ตั้งแต่ Stakeholder/Scope Statement, Evidence, Negotiation ไปจนถึง Backlog
2. **จุดที่ทีมเรายังอ่อนที่สุดคืออะไร และจะทำอย่างไรต่อ?**
   การกำหนดเกณฑ์ "ความจำเป็นเร่งด่วนกว่า" สำหรับการเรียกคืนอุปกรณ์ก่อนกำหนด (`FR-EQP-05`) ยังไม่มีตัวเลขชัดเจน ทีมจะสอบถามผู้ดูแลอุปกรณ์/หัวหน้าศูนย์กีฬาเพิ่มเติมก่อน Week 06
3. **คำถามที่อยากถามอาจารย์ในคาบหน้า (Week 6) คือ...**
   ในการทำ State Diagram ของสถานะอุปกรณ์ ควรแยกสถานะ "ถูกเรียกคืนก่อนกำหนด" ออกจากสถานะ "ค้างคืน" (คืนล่าช้าตามปกติ) อย่างชัดเจน หรือใช้สถานะร่วมกันแล้วแยกด้วยเหตุผลประกอบ?
