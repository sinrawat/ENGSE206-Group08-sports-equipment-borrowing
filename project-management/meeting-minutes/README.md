# Meeting — 2026-07-21 — Week 04

## Participants
- ศิลวัต อาซอง
- กฤตเมธ สินธุใส
- กิตติภพ สว่างเจริญทรัพย์

> เวลาประชุม: เริ่ม 11:00 น.

## Agenda
1. ทบทวนผลการเก็บ evidence ของ Week 4 (คำตอบ Q-01–Q-08 ตาม Interview Guide)
2. ตรวจสอบวิธีเก็บข้อมูล — ยืนยันว่าใช้ AI roleplay simulation ไม่ใช่การสัมภาษณ์บุคคลจริง
3. ทบทวนไฟล์ที่จัดทำ: `04-evidence-log.md`, `04-requirement-candidates.md`, `ai-conversation-excerpt.md`
4. วางแผนสิ่งที่ต้องตรวจสอบเพิ่มกับบุคคลจริงใน Week 5

## Notes
- ทีมใช้ AI roleplay จำลองคำตอบของ 4 บทบาท (ผู้ดูแลอุปกรณ์, นักศึกษา/ผู้ยืม, ชมรม/ผู้จัดกิจกรรม, เจ้าหน้าที่/ผู้บริหาร) ตาม prompt ที่ควบคุมไม่ให้ AI สร้างข้อมูลนอกขอบเขตของแต่ละบทบาท
- แปลงคำตอบเป็น Evidence Log (E-01–E-08) พร้อมแยก Observation กับ Interpretation และผูกกลับไปที่ OQ/EO/BR เดิมจาก Week 2–3
- พบว่าคำตอบจาก roleplay สอดคล้องกับสมมติฐานเดิมหลายจุด (เช่น BR-03 ระยะเวลายืม 2–3 วัน, BR-05 จองล่วงหน้า 5–7 วัน) แต่ **ยังไม่ถือเป็นการยืนยันจากบุคคลจริง**
- พบ need ใหม่ที่ไม่เคยอยู่ใน scope เดิมของ Week 2 คือเรื่อง reporting/dashboard สำหรับเจ้าหน้าที่ (E-08 / RC-06) — ต้องตรวจสอบว่ากระทบขอบเขตโครงงานหรือไม่
- สร้าง Requirement Candidate 6 ข้อ (RC-01–RC-06) ส่วนใหญ่มีสถานะ `Candidate` หรือ `Needs Validation`
- แก้ไข wording ในเอกสารทั้งหมดจาก "ยืนยัน" เป็น "สอดคล้องกับสมมติฐาน (ยังไม่ยืนยันกับคนจริง)" เพื่อความถูกต้องตาม Responsible AI plan

## Decisions
- D-01: ใช้ AI roleplay เป็นวิธีเก็บ evidence เบื้องต้นของ Week 4 และจะต้องตรวจสอบซ้ำกับบุคคลจริงก่อนสรุปเป็น requirement ฉบับสมบูรณ์
- D-02: เก็บไฟล์ evidence ทั้งหมดไว้ที่ `evidence/week-04/` ตาม convention เดิมของทีม
- D-03: RC-06 (reporting/dashboard) จะยังไม่ถูกดันเข้า backlog แบบเต็มจนกว่าจะตรวจสอบผลกระทบต่อ Scope Statement (Week 2)

## Action Items
| Task | Owner | Due | Related File |
|---|---|---|---|
| เติมวันที่รัน AI roleplay ให้ครบในไฟล์ evidence | [ชื่อผู้รับผิดชอบ] | Week 05 | `ai-conversation-excerpt.md`, `04-evidence-log.md` |
| นัดสัมภาษณ์บุคคลจริงเพื่อตรวจสอบ OQ-06 ถึง OQ-09 | [ชื่อผู้รับผิดชอบ] | Week 05 | `04-evidence-log.md` |
| ตรวจสอบว่า RC-06 กระทบ Scope Statement เดิมหรือไม่ | [ชื่อผู้รับผิดชอบ] | Week 05 | `04-requirement-candidates.md`, `02-stakeholder-context-scope.md` |
| แนบไฟล์ evidence ต้นฉบับลงใน `evidence/week-04/` ตาม path ที่อ้างอิงไว้ | [ชื่อผู้รับผิดชอบ] | Week 05 | `04-evidence-log.md` |
