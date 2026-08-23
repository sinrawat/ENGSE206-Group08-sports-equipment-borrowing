# ใบตรวจข้ามทีม (Peer Cross-Review Form) — ช่วงที่ 4

> **Case Project:** Case-08 — ระบบยืม–คืนอุปกรณ์กีฬาและกิจกรรม
> **Review Date:** 23 สิงหาคม 2569
> **Reviewing Sub-team / Peer Group:** Claude (AI Cross-Reviewer) — สวมบทบาทเป็นทีมตรวจข้ามตามคำขอของทีม 08
> **Target Artefacts Reviewed:** `02-stakeholder-context-scope.md`, `04-negotiation-record.md`, `04-requirement-candidates.md`, `05-open-questions-and-issues.md`, `05-prioritization-rationale.md`, `05-requirement-backlog-v0.2.md`

---

## 1. ผลการตรวจข้ามทีม (Checklist Evaluation)

| # | สิ่งที่ตรวจ | ผลการประเมิน (ผ่าน / ไม่ผ่าน) | ข้อเสนอแนะ / หมายเหตุ (อ้าง ID เสมอ) |
|---|---|---|---|
| 1 | **ทุก Must มีสาย traceable ครบ** (Problem → Evidence → Need → FR/NFR → Priority) — ตรวจกับ Must จริง: `FR-EQP-01, FR-EQP-02, FR-EQP-03, FR-EQP-06, FR-EQP-07, NFR-EQP-01` | **[x] ผ่าน** &nbsp;&nbsp;&nbsp; `[ ]` ไม่ผ่าน | ทุกตัวมีสายโยงชัดเจนใน `05-requirement-backlog-v0.2.md` คอลัมน์ "Evidence / Need Trace": FR-EQP-01 → E-01→N-01; FR-EQP-02/03 → E-02,E-05→N-02; FR-EQP-06/07 → E-06,E-07→N-05; NFR-EQP-01 → ระบุชัดว่าเป็น policy-derived constraint จาก Week2 Scope Statement ไม่ใช่ E-ID (ซึ่งเอกสารเองก็ระบุไว้ตรงไปตรงมา ไม่ได้แอบอ้างว่ามาจาก evidence) ถือว่าโปร่งใสและ pass ได้ — **ข้อควรระวัง:** ผู้ตรวจไม่เคยเห็นถ้อยคำดิบของ E-01..E-08 ใน `04-evidence-log.md` จึงตรวจได้แค่ระดับ "อ้างอิง ID สอดคล้องกัน" ยังไม่ใช่ "ยืนยันคำต่อคำว่าหลักฐานพูดแบบนั้นจริง" |
| 2 | **FR/NFR วัด/ทดสอบได้** (มีตัวเลข/เงื่อนไขเชิงปริมาณชัดเจน) | `[ ]` ผ่าน &nbsp;&nbsp;&nbsp; **[x] ไม่ผ่าน (บางส่วน)** | มีเฉพาะ **FR-EQP-06** (≤ 3 วินาที) และ **NFR-EQP-03** (≤ 5 คลิก, 375px) ที่วัดผลได้ชัดเจนแล้ว ส่วนที่ยัง **ไม่มีตัวเลข/เกณฑ์ตรวจรับ** และควรแก้ก่อนล็อก baseline: <br>• **FR-EQP-01** — "ค้นหาประวัติย้อนหลังได้" ไม่ระบุช่วงเวลาย้อนหลังหรือเวลาตอบสนอง (backlog เองก็ยัง flag เป็น Open Question) <br>• **FR-EQP-02** — ไม่ระบุจำนวน/ขนาดไฟล์ภาพถ่ายขั้นต่ำ (เทียบเคส CLF ที่ระบุ ≤10MB) <br>• **FR-EQP-03** — "ดูภาพถ่ายได้" ไม่ระบุเงื่อนไขเวลา/สิทธิ์ที่วัดได้ <br>• **FR-EQP-04** — ไม่มี SLA เวลาอนุมัติ (unresolved อยู่แล้วตาม negotiation N-02) <br>• **FR-EQP-05** — ไม่มีตัวเลขระยะเวลาแจ้งล่วงหน้าขั้นต่ำ (unresolved ตาม negotiation N-01) <br>• **FR-EQP-08** — ไม่ระบุความถี่รายงาน (รายวัน/สัปดาห์/เรียลไทม์) |
| 3 | **ไม่มี requirement กำกวม/ซ้ำ** (Atomic & Unambiguous) | **[x] ผ่าน (มีข้อเสนอแนะ)** &nbsp;&nbsp;&nbsp; `[ ]` ไม่ผ่าน | จุดแข็ง: ทีมแยก FR-EQP-02 (บันทึก) ออกจาก FR-EQP-03 (ดู/access) และแยก FR-EQP-06 (แสดงสถานะ) ออกจาก FR-EQP-07 (ป้องกันจองซ้ำ) ได้ atomic ดีมาก เป็นแนวปฏิบัติที่ดี <br>**ข้อเสนอแนะ:** **FR-EQP-01** ยังรวม 2 ความสามารถไว้ในข้อเดียว คือ "บันทึกประวัติ" + "ค้นหาประวัติ" — ควรพิจารณาแยกตามแนวทางเดียวกับ RC-02→FR-EQP-02/03 เพื่อความ atomic และตรวจรับแยกกันได้ง่ายขึ้น |
| 4 | **Scope ตรงกับ Case Card** (ไม่บวมเกินขอบเขตที่ได้รับมอบหมาย) | **[x] ผ่าน** &nbsp;&nbsp;&nbsp; `[ ]` ไม่ผ่าน | ทีมจัดการ scope creep ได้ดี: **FR-EQP-08** (dashboard) ถูกลด priority เป็น Could และมีการแยก **ISSUE-EQP-01** (คำแนะนำจัดซื้อ/งบประมาณ) ออกเป็น "Won't yet" ทันทีที่พบว่าใกล้เคียงส่วนบัญชีที่ Week 2 Scope Statement กันไว้นอกขอบเขต — เป็นตัวอย่างวินัยเรื่อง scope ที่ดี ไม่เดา requirement เกินหลักฐาน **NFR-EQP-01** ยังตอกย้ำ boundary เดิม (ไม่เชื่อมระบบบัญชี/ค่าปรับ, ไม่เก็บ PII เกินจำเป็น) สอดคล้องกับ scope ต้นฉบับ |
| 5 | **MoSCoW มีเหตุผลรองรับ** (Rationale สมเหตุสมผลจาก Value/Risk) | **[x] ผ่าน** &nbsp;&nbsp;&nbsp; `[ ]` ไม่ผ่าน | `05-prioritization-rationale.md` ใช้กรอบ Value/Risk/Urgency/Dependency ชัดเจนกับทุกข้อ ตัวอย่างที่แข็งแรง: FR-EQP-06/07 ได้ Must เพราะชมรมจัดอันดับปัญหาจองซ้ำเป็นอันดับ 1 (E-07/Q-07) และมีหลักฐานเชิงตัวเลขรองรับ (E-06); FR-EQP-08 ได้แค่ Could เพราะเป็น need ใหม่ที่ยังไม่ยืนยันผลกระทบต่อ scope เดิม — เหตุผลไม่ได้มาจากความชอบส่วนตัว มีหลักฐานรองรับทุกข้อ |

---

## 2. ข้อเสนอแนะเพื่อการปรับปรุงและเตรียมพร้อม Week 06 (Constructive Feedback)

1. **ด้าน Traceability (อ้างอิง FR-EQP-01, FR-EQP-02/03, NFR-EQP-01):**
   - สายเชื่อมโยงจาก Evidence → Need → RC → FR/NFR ทำได้ดีและสอดคล้องกันตลอดทั้ง 3 เอกสาร (negotiation record, requirement candidates, backlog) แต่เพราะผู้ตรวจไม่เคยเห็นถ้อยคำดิบของ `04-evidence-log.md` แนะนำให้ทีมเปิดไฟล์นั้นตรวจซ้ำเองอีกรอบว่า E-01 ถึง E-08 เขียนสอดคล้องกับที่ negotiation record/requirement candidates อ้างถึงจริง ก่อน tag baseline-v1.0
2. **ด้าน Quality & Verifiability (อ้างอิง FR-EQP-01, FR-EQP-02, FR-EQP-04, FR-EQP-05, FR-EQP-08):**
   - นี่คือจุดที่ต้องแก้ก่อนล็อก baseline จริงจัง — requirement เกือบครึ่งใน Must/Should list ยังไม่มีตัวเลขตรวจรับได้ แนะนำเติมอย่างน้อย: (ก) FR-EQP-01 ระบุช่วงเวลาย้อนหลังที่ต้องค้นได้ + เวลาตอบสนอง, (ข) FR-EQP-02 ระบุจำนวน/ขนาดไฟล์ภาพถ่ายขั้นต่ำ, (ค) FR-EQP-08 ระบุความถี่รายงาน แม้ยังไม่รู้คำตอบสุดท้ายก็ควรใส่เป็น "ค่าที่เสนอ รอยืนยัน" แทนการเว้นว่างไว้เฉยๆ เพื่อให้ผ่านเกณฑ์ "วัดผลได้" ของ Baseline Review
3. **ด้านการเตรียมต่อยอดสู่ Requirement Modeling (Week 06 Handoff):**
   - แนะนำนำ `FR-EQP-06` และ `FR-EQP-07` ไปทำ Use Case หลักก่อน เพราะเป็น Must ที่ priority สูงสุด (ปัญหาอันดับ 1 ของชมรม) และพร้อมที่สุด (สถานะ "Ready for Week06")
   - นำ `FR-EQP-02`/`FR-EQP-03` ไปทำ Acceptance Criteria ได้ทันทีที่ยืนยันเรื่องผู้ถ่ายภาพ/สถานที่เก็บหลักฐาน (OQ-EQP-02)
   - นำ `NFR-EQP-01` และ `NFR-EQP-03` ไปทำ Quality Scenario ได้เลยเพราะพร้อมและมีเกณฑ์วัดผลชัดเจนแล้ว

---

## 3. สรุปผลการประเมิน (Gate Assessment Result)

- **สถานะ:** **ผ่านแบบมีเงื่อนไข (Conditional Pass) — 4/5 ข้อผ่าน, ข้อ 2 (Verifiability) ยังไม่ผ่านเต็มรูปแบบ** ต้องเติมเกณฑ์เชิงตัวเลขให้ FR-EQP-01, FR-EQP-02, FR-EQP-03, FR-EQP-04, FR-EQP-05, FR-EQP-08 ก่อน tag `baseline-v1.0` เป็นทางการ (หรือถ้าจะ tag ตอนนี้ ต้องระบุใน Decision Log ว่ายอมรับ gap นี้ชั่วคราวและจะแก้ใน Week 06)
- **ผู้ตรวจสอบ (Cross-Reviewers):** Claude (AI Cross-Reviewer) ตามคำขอของทีม 08
- **วันที่ยืนยันผล:** 23 สิงหาคม 2569