# 08 — Validation, Traceability and Change Management

> **Week 8 deliverable**
> เวอร์ชัน: v1.0 | สถานะ: Draft | ทีม: Team 08 | วันที่: 20/08/2569

## 1. Validation Plan

| Validation Activity | Artefact | Participants | Criteria | Evidence |
|---|---|---|---|---|
| Requirement Baseline Review (self-directed studio) | `05-requirement-backlog-v0.2.md` | ทีม 08 ทั้งหมด (5 บทบาท: Facilitator, Traceability Auditor, Quality Checker, Scribe, Timekeeper) | completeness, consistency, feasibility, testability | `evidence/week-05/baseline-review/` |
| Peer review / Cross-Review | `05-requirement-backlog-v0.2.md`, ตาราง Traceability (§3 ของเอกสารนี้) | ทีมข้างเคียง | ทุก Must มีสาย traceable ครบ, FR/NFR วัดได้, ไม่ซ้ำ/กำกวม, scope ตรง Case Card, MoSCoW มีเหตุผล | `ENGSE206_RBR_PeerReview_Template_Case08.xlsx` (แบบฟอร์มเตรียมไว้ รอผลจริง) |
| Stakeholder simulation / checklist | SRS v1 (`07-srs-v1.md`) | [roles — รอกำหนดเมื่อยืนยัน Open Issues] | completeness, consistency, feasibility, testability | `../evidence/week-08/` |

## 2. Requirements Quality Checklist

> ประเมินจาก requirement statement ใน `05-requirement-backlog-v0.2.md` โดยใช้เกณฑ์ 4 ข้อจากเอกสาร Requirement Baseline Review (Verifiable, Unambiguous, Atomic, Traceable) รวมกับ 5 check ตาม template

| Check | Result | Evidence / Note |
|---|---|---|
| Requirement มี ID และไม่ซ้ำกัน | Pass | FR-EQP-01 ถึง 08, NFR-EQP-01 ถึง 03 ไม่มี ID ซ้ำ |
| ใช้ถ้อยคำชัดเจน ไม่กำกวม | Pass with note | FR-EQP-06/07 และ NFR-EQP-01 ชัดเจนแล้ว; FR-EQP-01/02/03/04/05/08 และ NFR-EQP-02/03 ยังมีคำที่ต้องยืนยันตัวเลข (เช่น "ระยะเวลาย้อนหลัง", "ระยะเวลาแจ้งล่วงหน้า") — ระบุเป็น Draft ไว้แล้ว ไม่ได้ฟันธงเอง |
| ตรวจรับหรือวัดผลได้ | Pass with note | FR-EQP-06 (≤3 วินาที), FR-EQP-07 (ปฏิเสธทันที), NFR-EQP-01 (ตรวจ integration list) วัดผลได้แล้ว; ที่เหลือมี Draft AC ใน `06-requirement-model.md` รอปิด Open Question ก่อนวัดผลได้เต็มรูปแบบ |
| มี source/rationale | Pass | ทุก Req ID อ้าง Source RC และ Evidence/Need Trace หรือระบุว่าเป็น policy-derived constraint (NFR-EQP-01) |
| Scope เหมาะสม | Pass with flag | ISSUE-EQP-01 (คำแนะนำจัดซื้อ/งบประมาณ) ถูกกันไว้นอก backlog อย่างถูกต้อง รอ scope owner ยืนยันก่อนพิจารณาใหม่ |

## 3. Traceability Matrix

| Stakeholder Need | FR / NFR | User Story / Use Case | Design Element | Verification / Review |
|---|---|---|---|---|
| N-01 (ผู้ดูแลอุปกรณ์ — ค้นประวัติ) | FR-EQP-01 | US-01 / UC-01 (supporting flow) | [ยังไม่ออกแบบ — Week 10] | Draft AC — รอ OQ ระดับการค้น |
| N-02 (ผู้ดูแลอุปกรณ์+ผู้ยืม — หลักฐานสภาพ) | FR-EQP-02 | US-02 / UC-02 (main flow) | [ยังไม่ออกแบบ] | Draft AC — รอ OQ-W05-02 |
| N-02 (สิทธิ์เข้าถึงหลักฐาน) | FR-EQP-03, NFR-EQP-02 | US-03 / UC-02 (step 4) | [ยังไม่ออกแบบ] | Draft AC — รอ OQ-W05-02 |
| N-03 (อนุมัติอุปกรณ์พิเศษ) | FR-EQP-04 | US-04 / UC-01 (alt flow A2) | [ยังไม่ออกแบบ] | Draft AC — รอ OQ-W05-01 |
| N-04 (เรียกคืนก่อนกำหนด) | FR-EQP-05 | US-05 / UC-03 | [ยังไม่ออกแบบ] | Draft AC — รอ OQ-W05-03 |
| N-05 (แสดงสถานะ/ป้องกันจองซ้ำ) | FR-EQP-06 | US-06 / UC-01 (step 2) | [ยังไม่ออกแบบ] | AC-06 Ready — review แล้วผ่านเกณฑ์ Verifiable |
| N-05 (ป้องกันจองซ้ำ) | FR-EQP-07 | US-07 / UC-01 (step 4/A1) | [ยังไม่ออกแบบ] | AC-07 Ready — review แล้วผ่านเกณฑ์ Verifiable |
| N-06 (รายงานสรุป) | FR-EQP-08 | US-08 / UC-04 | [ยังไม่ออกแบบ] | Draft AC — รอ OQ-W05-05 |
| Policy (Scope Statement Week 2) | NFR-EQP-01 | Quality Scenario (`06-requirement-model.md` §4) | [ยังไม่ออกแบบ] | AC-NFR-01 Ready — review แล้วผ่านเกณฑ์ Verifiable |

**หมายเหตุ Gap:** ทุกแถวในคอลัมน์ "Design Element" ยังว่าง เพราะทีมยังไม่เริ่มงาน Week 10 (Design Strategy/Architecture) — เป็นไปตาม Roadmap ปกติ ไม่ใช่ gap ที่ต้องแก้ตอนนี้

## 4. Change Request Log

| CR-ID | Date | Requested Change | Reason / Evidence | Impacted Artefacts | Decision | Owner |
|---|---|---|---|---|---|---|
| CR-01 | 18/08/2569 | ปรับ requirement statement ของ FR-EQP-01, FR-EQP-05 (เดิม), NFR-EQP-03 ให้วัดผลได้ และแยก FR-EQP-02 (เดิม) เป็น FR-EQP-02/03, แยก FR-EQP-05 (เดิม) เป็น FR-EQP-06/07 | ผลตรวจ Quality & MoSCoW Check (ช่วงที่ 3 ของ Requirement Baseline Review) พบว่า requirement เดิมไม่ผ่านเกณฑ์ Verifiable/Atomic เช่น NFR-EQP-03 เดิมใช้คำว่า "ใช้งานง่าย" แบบลอยๆ และ FR-EQP-05 เดิมรวม 2 ความสามารถไว้ข้อเดียว | `05-requirement-backlog.md` (v0.1 → v0.2), `06-requirement-model.md` | Accepted | Team 08 |
| CR-02 | [รอวันที่] | [กรอกเมื่อมีการเปลี่ยนแปลงจริงหลัง Peer Cross-Review] | [กรอก] | [กรอก] | [Accepted/Rejected/Deferred] | [ชื่อ] |

## 5. Baseline Decision

- Baseline name: `srs-v1.0`
- Date: 20/08/2569 (backlog v0.2 ล็อกเป็น baseline candidate; SRS v1 อ้างอิงจาก backlog นี้)
- Approved/Reviewed by: **ยังไม่ approve** — รอผล Peer Cross-Review และการยืนยัน Open Issues อย่างน้อยข้อที่กระทบ requirement ระดับ Must
- Remaining open issues: OQ-W05-01 ถึง OQ-W05-06 และ ISSUE-EQP-01 (ดู `07-srs-v1.md` §8) — requirement ที่เป็น Must ทั้งหมด (FR-EQP-01, 02, 03, 06, 07, NFR-EQP-01) มี 3 ใน 6 ข้อที่ยังเป็น Draft (01, 02, 03) เพราะรอ OQ-W05-02 และรายละเอียดระดับการค้นประวัติ — **ยังไม่ควรประกาศ baseline v1.0 อย่างเป็นทางการจนกว่าจะปิด Open Question ของ Must requirement เหล่านี้**

## 6. Follow-up Backlog

- [ ] ยืนยัน OQ-W05-01 ถึง OQ-W05-06 กับ stakeholder ที่เกี่ยวข้อง (ดูเจ้าของคำถามใน `05-open-questions-and-issues.md`)
- [ ] ทำ Peer Cross-Review จริงกับทีมข้างเคียงโดยใช้ `ENGSE206_RBR_PeerReview_Template_Case08.xlsx` แล้วบันทึกผลลง `evidence/week-05/baseline-review/`
- [ ] เลื่อน Draft AC ใน `06-requirement-model.md` เป็น Ready หลังปิด Open Question แต่ละข้อ
- [ ] ขอคำยืนยันจากผู้สอน/scope owner เรื่อง ISSUE-EQP-01 (คำแนะนำจัดซื้อ/งบประมาณ)
- [ ] เมื่อ Must requirement ทั้งหมดเป็น Ready แล้ว จึงประกาศ `baseline-v1.0` อย่างเป็นทางการ พร้อม commit + git tag ตามขั้นตอนในเอกสาร Requirement Baseline Review §9
- [ ] เริ่มออกแบบ Use Case Diagram / Activity Diagram / Domain Model ใน `diagrams/` ก่อนเข้า Week 10 (Design Strategy)
