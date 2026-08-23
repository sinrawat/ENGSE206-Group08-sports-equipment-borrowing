# 08 — Validation, Traceability and Change Management

> **Week 8 deliverable**
>
> **Project:** Equipment Borrow–Return System (EQP)
>
> **Case:** Case-08 — ระบบยืม–คืนอุปกรณ์กีฬาและกิจกรรม
>
> **Team:** Team 08

---

# 1. Validation Plan

| Validation Activity | Artefact | Participants | Criteria | Evidence |
|---|---|---|---|---|
| Peer Review / Stakeholder Simulation / Checklist | docs/01 ถึง docs/05 และ SRS v1 | นักศึกษา (ศิลวัต, กฤตเมธ, กิตติภพ), อาจารย์ผู้สอน, ตัวแทนผู้ใช้งาน (ผู้ดูแลอุปกรณ์/ชมรม) | completeness, consistency, feasibility, testability, traceability, scope alignment, MoSCoW rationale | ../evidence/week-08/ |

---

# 2. Requirements Quality Checklist

| Check | Result | Evidence / Note |
|---|---|---|
| Requirement มี ID และไม่ซ้ำกัน | Pass | FR-EQP-01 ถึง FR-EQP-08 และ NFR-EQP-01 ถึง NFR-EQP-03 มี ID แยกกันชัดเจน |
| ใช้ถ้อยคำชัดเจน ไม่กำกวม | Pass | ใช้คำว่า "ระบบต้อง..." / "ระบบควร..." และระบุพฤติกรรมที่ระบบต้องรองรับ (ปรับจาก CR-01, CR-02 ใน Week 5) |
| ตรวจรับหรือวัดผลได้ | Pass | FR-EQP-06 (≤3s) และ NFR-EQP-03 (≤5 คลิก/375px) วัดผลได้ชัดเจนแล้ว ส่วน FR-EQP-01, 02, 03, 04, 05, 08 เคยถูกตั้งเป็น CR-03 (Week 5 Peer Cross-Review) |
| มี source/rationale | Pass | Requirement เชื่อมโยงกับ Evidence (E-01..E-08), Need (N-01..N-06) และ Requirement Candidate (RC-01..RC-06) ตาม 04-requirement-candidates.md |
| Scope เหมาะสม | Pass | ครอบคลุมการยืม–คืน การตรวจสภาพอุปกรณ์ การอนุมัติอุปกรณ์พิเศษ การเรียกคืนก่อนกำหนด การจองล่วงหน้า และรายงานสรุป — ไม่รวมบัญชี/ค่าปรับ/QR จริงตาม Week 2 Scope Statement |

---

# 3. Traceability Matrix

| Stakeholder Need | FR / NFR | User Story / Use Case (proposed — รอยืนยันกับของจริง Week 06) | Design Element | Verification / Review |
|---|---|---|---|---|
| N-01 ผู้ดูแลอุปกรณ์ต้องการบันทึก/ค้นประวัติการยืม–คืนแบบดิจิทัลแทนสมุด | FR-EQP-01 | US-01 / UC-01 บันทึกและค้นประวัติอุปกรณ์ | Equipment History Log Screen | Functional Review |
| N-02 ผู้ดูแลอุปกรณ์และผู้ยืมต้องการหลักฐานสภาพอุปกรณ์ก่อน–หลังยืมที่น่าเชื่อถือ | `FR-EQP-02`, FR-EQP-03 | US-02 / UC-02 บันทึกและตรวจสอบสภาพอุปกรณ์ | Condition Report Form + Evidence Viewer | Acceptance Criteria Review |
| N-03 ต้องควบคุมการยืมอุปกรณ์ประเภทพิเศษ/ราคาสูง | FR-EQP-04 | US-03 / UC-03 ขออนุมัติยืมอุปกรณ์พิเศษ | Approval Request Component | Scenario Review |
| N-04 ผู้ดูแลอุปกรณ์ต้องการเรียกคืนอุปกรณ์ก่อนกำหนดเมื่อจำเป็น | FR-EQP-05 | US-04 / UC-04 เรียกคืนอุปกรณ์ก่อนกำหนด | Early Recall Component | Alternate Flow Review |
| N-05 ชมรมต้องการจองอุปกรณ์ล่วงหน้าโดยไม่ถูกจองซ้ำ | `FR-EQP-06`, FR-EQP-07 | US-05 / UC-05 จองอุปกรณ์ล่วงหน้า | Booking Calendar / Availability Component | Workflow Review |
| N-06 เจ้าหน้าที่ต้องการรายงานสรุปการใช้งาน/ความชำรุด | FR-EQP-08 | US-06 / UC-06 ดูรายงานสรุปการใช้งานอุปกรณ์ | Equipment Usage Dashboard | Report Review |
| N-07 ต้องจำกัดสิทธิ์เข้าถึงหลักฐานภาพถ่ายเฉพาะผู้เกี่ยวข้อง | NFR-EQP-02 | US-07 / UC-07 Access Control | Role-based Access Control Component | Security Review |
| N-08 ผู้ยืมใหม่ต้องใช้งานได้เองโดยไม่ต้องฝึกอบรม | NFR-EQP-03 | US-08 / UC-01 ทำรายการยืมด่วน | Mobile-responsive Quick-Borrow UI | Usability Review |
| N-09 ต้องไม่เชื่อมข้อมูลกับระบบบัญชี/ค่าปรับ และเก็บข้อมูลเท่าที่จำเป็น | NFR-EQP-01 | — (Design constraint ไม่ใช่หน้าจอ) | Data Boundary / Integration Constraint | Privacy & Compliance Review |

> **หมายเหตุ:** การจัดการ "ผู้คืนอุปกรณ์ล่าช้า" (สถานะค้างคืน/แจ้งเตือนทวงคืน) ยังไม่ถูกกำหนดเป็น Requirement เนื่องจาก OQ-EQP-06 ยังไม่มี evidence รองรับเลยจนถึงขณะนี้

---

# 4. Traceability Exceptions / Open Questions

| ID | Requirement | Gap / Unknown | Action |
|---|---|---|---|
| OQ-EQP-01 | FR-EQP-04 | ยังไม่ยืนยันเกณฑ์ราคา/รายการที่ถือเป็น "อุปกรณ์พิเศษ" และผู้มีอำนาจอนุมัติคือใครกันแน่ | สอบถามหัวหน้าศูนย์กีฬา/อาจารย์ผู้รับผิดชอบ |
| OQ-EQP-02 | `FR-EQP-02`, FR-EQP-03 | ยังไม่ยืนยันว่าใครเป็นผู้ถ่ายภาพหลักฐาน และเก็บ/รักษาไว้ที่ไหนนานเท่าใด | สัมภาษณ์ผู้ดูแลอุปกรณ์เพิ่มเติม |
| OQ-EQP-03 | FR-EQP-05 | ยังไม่ยืนยันเกณฑ์ "ความจำเป็นเร่งด่วนกว่า" และระยะเวลาแจ้งล่วงหน้าขั้นต่ำ | ยืนยันกับผู้ดูแลอุปกรณ์/หัวหน้าศูนย์กีฬา |
| OQ-EQP-04 | `FR-EQP-06`, FR-EQP-07 | ยังไม่ยืนยันว่าระยะเวลาจองล่วงหน้า 5–7 วันเป็นค่ามาตรฐานของทุกชมรมหรือเฉพาะกลุ่มที่สัมภาษณ์ | สัมภาษณ์ชมรมเพิ่มอย่างน้อย 1 กลุ่มที่มีลักษณะกิจกรรมต่างกัน |
| OQ-EQP-05 | FR-EQP-08 | ยังไม่ยืนยันความถี่รายงานที่ต้องการ และผู้อนุมัติงบจัดซื้อคือใคร | ขอคำยืนยันจากผู้สอน/scope owner |
| OQ-EQP-06 | — (gap; ไม่มี FR รองรับ) | ยังไม่มี evidence ตอบว่าควรจัดการผู้คืนอุปกรณ์ล่าช้าอย่างไร | สัมภาษณ์เพิ่มด้วยคำถามใหม่ที่ตรงประเด็นเรื่องการคืนล่าช้าโดยเฉพาะ |

---

# 5. Change Request Log

| CR-ID | Date | Requested Change | Reason / Evidence | Impacted Artefacts | Decision | Owner |
|---|---|---|---|---|---|---|
| CR-01 | 18/08/2569 | ปรับ RC-01 ถึง RC-06 ให้สอดคล้องกับ Evidence และ Need Summary | ผลจากการตรวจสอบ Traceability ระหว่าง Evidence → Need → Requirement | `04-evidence-log.md`, `04-requirement-candidates.md`, 05-requirement-backlog.md | Accepted | ทีม 08 |
| CR-02 | 18/08/2569 | ปรับ NFR-EQP-03 ให้มีเกณฑ์วัดผลได้ (≤5 คลิก, 375px) แทน "ใช้งานง่าย" | ผล Quality Audit พบถ้อยคำกำกวม | 05-requirement-backlog.md | Accepted | กิตติภพ (Quality Checker) |
| CR-03 | 23/08/2569 | เติมเกณฑ์เชิงตัวเลขให้ FR-EQP-01, 02, 03, 04, 05, 08 | Peer Cross-Review พบ Verifiability gap | `05-requirement-backlog.md`, 08-validation-traceability.md | **Needs Follow-up** — [[ TODO: ยืนยันว่าปิดแล้วระหว่างทำ Use Case/AC Week06-07 หรือยัง ]] | ทีม 08 |
| CR-04 | 18/08/2569 | ยังไม่กำหนด "การจัดการผู้คืนอุปกรณ์ล่าช้า" เป็น Requirement อย่างเป็นทางการ | OQ-EQP-06 ยังไม่มี evidence รองรับเลย | `05-requirement-backlog.md`, 08-validation-traceability.md | Accepted | ทีม 08 |
| CR-05 | 18/08/2569 | ตรวจสอบ Requirement ที่เกี่ยวข้องกับการอนุมัติอุปกรณ์พิเศษ (`FR-EQP-04`) และการเรียกคืนก่อนกำหนด (`FR-EQP-05`) ก่อนจัดทำ Use Case | ต้องยืนยันเกณฑ์อุปกรณ์พิเศษ/SLA และระยะเวลาแจ้งล่วงหน้าก่อน | `05-requirement-backlog.md`, 08-validation-traceability.md | Needs Follow-up | ทีม 08 |

---

# 6. Baseline Decision

- **Baseline name:** srs-v1.0
- **Date:** [[ TODO: วันที่จริงที่ tag ]]
- **Approved/Reviewed by:** Team 08 — ศิลวัต อาซอง, กฤตเมธ สินธุใส, กิตติภพ สว่างเจริญทรัพย์
- **Status:** Draft Baseline
- **Remaining open issues:** OQ-EQP-01 ถึง OQ-EQP-06

### Baseline Decision

Requirement ที่มี Evidence รองรับชัดเจนสามารถนำไปใช้ต่อใน Design และขั้นตอนถัดไปได้

ส่วน Requirement ที่ยังมี Open Question เช่น

- เกณฑ์อุปกรณ์พิเศษและผู้มีอำนาจอนุมัติ (`OQ-EQP-01`)
- ผู้ถ่ายภาพและสถานที่เก็บหลักฐานสภาพอุปกรณ์ (`OQ-EQP-02`)
- เกณฑ์ความเร่งด่วนและระยะเวลาแจ้งล่วงหน้าของการเรียกคืนก่อนกำหนด (`OQ-EQP-03`)
- ระยะเวลาจองล่วงหน้ามาตรฐานของทุกชมรม (`OQ-EQP-04`)
- ความถี่รายงานและผู้อนุมัติงบจัดซื้อ (`OQ-EQP-05`)
- วิธีจัดการผู้คืนอุปกรณ์ล่าช้า (`OQ-EQP-06`)

จะยังไม่ถือว่าเป็น Final Requirement จนกว่าจะได้รับการยืนยันจาก Stakeholder

---

# 7. Follow-up Backlog

- [x] ตรวจสอบ Traceability ระหว่าง Evidence → Need → Requirement
- [x] ตรวจสอบ Requirement ID ไม่ให้ซ้ำกัน
- [x] แยก Open Question ออกจาก Final Requirement
- [x] ตรวจสอบ MoSCoW Priority ของ Requirement
- [ ] เติมเกณฑ์เชิงตัวเลขให้ FR-EQP-01, 02, 03, 04, 05, 08 (ปิด CR-03)
- [ ] ยืนยันเกณฑ์ราคา/รายการ "อุปกรณ์พิเศษ" และผู้มีอำนาจอนุมัติ
- [ ] ยืนยันผู้ถ่ายภาพและสถานที่เก็บหลักฐานสภาพอุปกรณ์
- [ ] ยืนยันเกณฑ์ความเร่งด่วนและระยะเวลาแจ้งล่วงหน้าของการเรียกคืนก่อนกำหนด
- [ ] ยืนยันระยะเวลาจองล่วงหน้ามาตรฐานของทุกชมรม
- [ ] ยืนยันความถี่รายงาน/สถิติที่เจ้าหน้าที่ต้องการ
- [ ] สัมภาษณ์เพิ่มเรื่องการจัดการผู้คืนอุปกรณ์ล่าช้า
- [ ] ตรวจสอบ SRS v1 หลังจาก Open Questions ได้รับคำตอบ

---

# 8. Validation Summary

จากการตรวจสอบ Requirements ใน Week 8 พบว่า Requirement หลักของระบบมีความสอดคล้องกับ Evidence และ Stakeholder Needs ในระดับที่สามารถนำไปพัฒนาต่อได้

อย่างไรก็ตาม Requirement บางรายการยังมีข้อมูลที่ต้องยืนยันเพิ่มเติม จึงถูกกำหนดสถานะเป็น Needs Follow-up แทนการกำหนดเป็น Final Requirement

โดยเฉพาะเรื่อง **การจัดการผู้คืนอุปกรณ์ล่าช้า (Late Return Handling)** ซึ่งต้องยืนยันก่อนว่าระบบควร:

1. ต่ออายุกำหนดคืนให้อัตโนมัติในบางเงื่อนไข (auto-extend)
2. ระงับสิทธิ์การยืมของผู้ค้างคืนชั่วคราวจนกว่าจะคืน
3. แจ้งเตือนทวงคืนแบบขั้นบันได (escalation) ให้ผู้ดูแลอุปกรณ์ทราบ
4. ให้ผู้ดูแลอุปกรณ์เป็นผู้ตัดสินใจเป็นรายกรณีโดยไม่มีกฎอัตโนมัติ

(หมายเหตุ: ตัวเลือกที่เกี่ยวกับการปรับค่าปรับ/ค่าเสียหายไม่รวมอยู่ในทางเลือกข้างต้น เนื่องจาก NFR-EQP-01 กำหนดไว้ชัดเจนตั้งแต่ Week 2 ว่าระบบต้องไม่เชื่อมโยงกับระบบบัญชี/ค่าปรับ)

ดังนั้นทีมจะนำประเด็นดังกล่าวไปตรวจสอบกับ Stakeholder ก่อนนำไปกำหนดเป็น Workflow และ Acceptance Criteria ในขั้นตอนถัดไป
