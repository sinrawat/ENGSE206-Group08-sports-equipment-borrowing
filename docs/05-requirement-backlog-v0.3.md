# 05 — Requirement Backlog v0.3: ระบบยืม–คืนอุปกรณ์กีฬาและกิจกรรม (Case 08)

> **Case:** ระบบยืม–คืนอุปกรณ์กีฬาและกิจกรรม
> **Source:** v0.2 (`05-requirement-backlog-v0.2.md`) + ขอบเขต Use Case แบบง่ายใน `06-requirement-models-v2.md`
> **Status:** v0.3 — เพิ่ม FR รองรับ UC-01..04 (เพิ่ม/ดูอุปกรณ์, ยืม, คืน, ดูข้อมูลสรุป)
> **Goal:** เพิ่ม FR ที่ขาดสำหรับขอบเขตใหม่แบบง่าย โดยไม่ลบ FR เดิม (เก็บไว้เพื่อประวัติ)

## 1. Project Metadata

| Field | Value |
|---|---|
| Course / Week | ENGSE206 / Week06 |
| Team | Team 08 |
| Case | Case 08 — ระบบยืม–คืนอุปกรณ์กีฬาและกิจกรรม |
| Source | `05-requirement-backlog-v0.2.md`, `06-requirement-models-v2.md` |
| Backlog version | `v0.3` |

## 2. Prioritization Method

ใช้ MoSCoW โดยพิจารณา Value, Risk, Urgency และ Dependency ตามเดิม

## 3. Requirement Backlog v0.3

| Req ID | Source RC | Evidence / Need Trace | Requirement Statement | Type | Priority | Rationale | Status | Open Question | Week06 Use |
|---|---|---|---|---|---|---|---|---|---|
| FR-EQP-01 | RC-01 | E-01 → Need N-01 | ระบบต้องให้ผู้ดูแลอุปกรณ์บันทึกประวัติการยืม–คืนของอุปกรณ์แต่ละชิ้นแบบดิจิทัล และค้นหาประวัติย้อนหลังของอุปกรณ์แต่ละชิ้นได้ | Functional | Must | เป็น core workflow และแทนที่สมุดบันทึกกระดาษโดยตรง | Needs Follow-up | ยืนยันระยะเวลาย้อนหลังที่ต้องค้นได้ และค้นตามผู้ยืมด้วยหรือไม่ | User Story + Use Case |
| FR-EQP-02 | RC-02 | E-02, E-05 → Need N-02 | ระบบต้องให้ผู้ดูแลอุปกรณ์บันทึกสภาพอุปกรณ์พร้อมภาพถ่าย ณ ตอนส่งมอบและตอนรับคืน | Functional | Must | หลักฐานจาก stakeholder 2 ฝ่ายสนับสนุนการแก้ข้อพิพาทความชำรุด | Needs Follow-up | ใครเป็นผู้ถ่ายภาพ และหลักฐานเก็บที่ใด/นานเท่าใด | Use Case + Acceptance Criteria |
| FR-EQP-03 | RC-02 follow-up | E-02, E-05 → Need N-02 | ระบบต้องให้ผู้ยืมที่เกี่ยวข้องและผู้ดูแลอุปกรณ์ดูภาพถ่ายและบันทึกสภาพของรายการยืมที่เกี่ยวข้องได้ | Functional | Must | แยก access/use concern ออกจาก FR-EQP-02 เพื่อให้ atomic | Needs Follow-up | ยืนยันบทบาทที่มีสิทธิ์ดูหลักฐานเพิ่มเติม | Use Case + Acceptance Criteria |
| FR-EQP-04 | RC-03 | E-03 → Need N-03; Negotiation N-02 (Option B) | ระบบต้องส่งคำขออนุมัติให้ผู้มีอำนาจเมื่อคำขอเกี่ยวข้องกับอุปกรณ์ประเภทพิเศษ/ราคาสูง และต้องบันทึกผลการอนุมัติ | Functional / Authorization | Should | มีคุณค่าด้านการควบคุมความเสี่ยง แต่เกณฑ์อุปกรณ์พิเศษยังไม่ยืนยัน | Needs Follow-up | เกณฑ์ราคา/รายการ และผู้มีอำนาจคือใคร | Use Case Extension |
| FR-EQP-05 | RC-04 | E-04 → Need N-04; Negotiation N-01 (Provisional) | ระบบต้องรองรับการเรียกคืนอุปกรณ์ก่อนกำหนดโดยผู้ดูแลอุปกรณ์ และบันทึกเหตุผลการเรียกคืน | Functional / Business Rule | Should | ทิศทาง negotiation ชัดระดับหนึ่ง แต่เกณฑ์เร่งด่วนยังไม่ครบ | Needs Follow-up | เกณฑ์เร่งด่วนและระยะเวลาแจ้งล่วงหน้า | Alternate Flow + State Rule |
| FR-EQP-06 | RC-05 | E-06, E-07 → Need N-05 | ระบบต้องแสดงสถานะว่าง/ถูกจองของอุปกรณ์ตามช่วงเวลาที่ผู้ใช้เลือกภายใน 3 วินาทีหลังเลือกช่วงเวลา | Functional | Must | แก้ pain point การมองสถานะอุปกรณ์และทำให้ตรวจรับได้ | Ready for Week06 | ยืนยันว่าช่วงเวลาจองล่วงหน้า 5–7 วันใช้กับทุกประเภทชมรมหรือไม่ | User Story + Use Case |
| FR-EQP-07 | RC-05 | E-06, E-07 → Need N-05 | ระบบต้องป้องกันการสร้างรายการจองอุปกรณ์ชิ้นเดียวกันที่ช่วงเวลาทับซ้อนกับรายการจองที่ยืนยันแล้ว | Functional / Integrity | Must | แยกจากการแสดงสถานะให้เป็น atomic requirement และตรงกับ pain point จองซ้ำ | Ready for Week06 | ยืนยันกติกากรณีคำขอรออนุมัติทับซ้อนกัน | Use Case + Acceptance Criteria |
| FR-EQP-08 | RC-06 (เฉพาะส่วนสรุปการใช้งาน/สถานะ) | E-08 → Need N-06; Negotiation N-03 (Unresolved) | ระบบต้องมีรายงาน/แดชบอร์ดให้เจ้าหน้าที่ดูจำนวนครั้งที่อุปกรณ์แต่ละชิ้นถูกยืม ประวัติความชำรุด สถานะ/ผู้ถือครองปัจจุบัน และกำหนดคืน | Functional / Reporting | Could | เป็น need ใหม่จากเจ้าหน้าที่ แต่ยังต้องตรวจผลกระทบต่อ Scope Statement | Needs Follow-up | ความถี่รายงานและผลกระทบต่อ scope เดิม | Follow-up only |
| NFR-EQP-01 | Scope Statement (Out of Scope: บัญชี/ค่าปรับ, ข้อมูลส่วนบุคคล) | Week 2 Scope Statement + Ethics | ระบบต้องเก็บข้อมูลผู้ยืมเฉพาะข้อมูลที่จำเป็นต่อการยืม–คืน และต้องไม่เชื่อมโยง/ประมวลผลร่วมกับระบบบัญชีหรือค่าปรับ | NFR / Policy-derived Constraint | Must | เป็น policy-derived constraint จาก Scope/ethics ไม่ได้เกิดจาก E-ID โดยตรง | Ready for Week06 | — | Quality Scenario + Constraint |
| NFR-EQP-02 | RC-02 follow-up | E-02, E-05 + Ethics | ระบบต้องจำกัดสิทธิ์การเข้าถึงภาพถ่ายและบันทึกสภาพอุปกรณ์เฉพาะผู้ดูแลอุปกรณ์และผู้ยืมที่เกี่ยวข้องกับรายการนั้น | NFR / Access Control | Should | รองรับความน่าเชื่อถือของหลักฐานและแยกจาก functional record | Needs Follow-up | ยืนยันบทบาทและขอบเขตสิทธิ์เพิ่มเติม | Quality Scenario |
| NFR-EQP-03 | Problem Brief §9 | Week 1 — Non-functional Expectations | ผู้ใช้ใหม่ต้องสามารถทำรายการยืมอุปกรณ์สำเร็จภายใน 5 คลิก โดยไม่ต้องได้รับการฝึกอบรมจากผู้ดูแล และหน้าจอหลักต้องรองรับการแสดงผลบนโทรศัพท์มือถือที่ความกว้าง 375 px | NFR | Should | แทนคำว่า "ใช้งานง่าย" ด้วยเกณฑ์ตรวจรับได้ และคง mobile requirement จาก Week 1 | Needs Follow-up | ยืนยันว่า 5 คลิกและ 375 px เป็นเกณฑ์ที่ทีม/ผู้สอนยอมรับหรือควรปรับ | Quality Scenario |
| ISSUE-EQP-01 | RC-06 (เฉพาะส่วนคำแนะนำจัดซื้อ/งบประมาณ) | E-08 → Need N-06 | คำแนะนำเรื่องการซ่อมบำรุง/จัดซื้อ และผู้อนุมัติงบประมาณ | Issue | Won't yet | อยู่นอก scope เดิมและยังไม่มี scope owner ยืนยัน | Hold | ผู้สอน/scope owner ยืนยันผลกระทบต่อ scope หรือไม่ | Follow-up only |
| FR-EQP-09 | RC-NEW-01 (v2 scope) | มาจาก `06-requirement-models-v2.md` UC-01 | ระบบต้องให้ผู้ดูแลอุปกรณ์เพิ่มรายการอุปกรณ์ใหม่เข้าสู่ระบบ โดยระบุชื่อ หมวดหมู่ และจำนวน | Functional | Must | จำเป็นเพื่อให้ระบบมีข้อมูลอุปกรณ์ก่อนจะยืม–คืนได้ | Ready for Week06 | ยืนยัน validation ฟิลด์บังคับ | User Story + Use Case |
| FR-EQP-10 | RC-NEW-01 (v2 scope) | มาจาก `06-requirement-models-v2.md` UC-01 | ระบบต้องแสดงรายการอุปกรณ์ทั้งหมดพร้อมสถานะปัจจุบัน (ว่าง/ถูกยืม) ให้ผู้ยืมและชมรม/ผู้จัดกิจกรรมดูได้ | Functional | Must | จำเป็นให้ผู้ใช้งานเห็นอุปกรณ์ก่อนตัดสินใจยืม | Ready for Week06 | — | User Story + Use Case |
| FR-EQP-11 | RC-NEW-02 (v2 scope) | มาจาก `06-requirement-models-v2.md` UC-02 | ระบบต้องให้ผู้ยืมหรือชมรม/ผู้จัดกิจกรรมยืมอุปกรณ์ที่มีสถานะว่าง และเปลี่ยนสถานะอุปกรณ์เป็น "ถูกยืม" ทันทีเมื่อยืนยัน | Functional | Must | เป็น core workflow ของขอบเขตใหม่ | Ready for Week06 | ยืนยันจำนวนชิ้น/ระยะเวลายืมสูงสุดต่อครั้ง | User Story + Use Case + Acceptance Criteria |
| FR-EQP-12 | RC-NEW-03 (v2 scope) | มาจาก `06-requirement-models-v2.md` UC-03 | ระบบต้องให้ผู้ดูแลอุปกรณ์ยืนยันรับคืนอุปกรณ์ และเปลี่ยนสถานะอุปกรณ์กลับเป็น "ว่าง" พร้อมบันทึกวันเวลาที่คืน | Functional | Must | เป็น core workflow ของขอบเขตใหม่ | Ready for Week06 | ยืนยันว่าต้องตรวจสภาพอุปกรณ์ตอนคืนหรือไม่ (นอก scope v2 ปัจจุบัน) | User Story + Use Case + Acceptance Criteria |

## 4. Priority Summary

| Priority | Count | Requirement IDs |
|---|---:|---|
| Must | 10 | FR-EQP-01, FR-EQP-02, FR-EQP-03, FR-EQP-06, FR-EQP-07, NFR-EQP-01, FR-EQP-09, FR-EQP-10, FR-EQP-11, FR-EQP-12 |
| Should | 4 | FR-EQP-04, FR-EQP-05, NFR-EQP-02, NFR-EQP-03 |
| Could | 1 | FR-EQP-08 |
| Won't yet | 1 | ISSUE-EQP-01 |

## 5. Ready / Follow-up / Hold

| Status | Requirement IDs | สิ่งที่ต้องทำต่อ |
|---|---|---|
| Ready for Week06 | FR-EQP-06, FR-EQP-07, NFR-EQP-01, FR-EQP-09, FR-EQP-10, FR-EQP-11, FR-EQP-12 | ทำ User Story / Use Case / Quality Scenario ได้ |
| Needs Follow-up | FR-EQP-01, FR-EQP-02, FR-EQP-03, FR-EQP-04, FR-EQP-05, FR-EQP-08, NFR-EQP-02, NFR-EQP-03 | ยืนยัน open questions ก่อนล็อก acceptance criteria/model แบบเต็ม |
| Hold | ISSUE-EQP-01 | รอ scope owner ยืนยัน |

## 6. Review Checklist

- [x] ทุก requirement มี Source RC หรือ Evidence/Policy source
- [x] ทุก requirement มี Evidence / Need Trace หรือระบุว่าเป็น policy-derived constraint
- [x] Requirement ที่รวมหลายเรื่องถูกแยกให้เป็น Atomic
- [x] Requirement ที่ใช้คำกำกวมถูกปรับให้มีตัวเลข/เงื่อนไขตรวจรับ
- [x] Priority มี rationale จาก value/risk/urgency/dependency
- [x] Unknown หรือ scope issue ไม่ถูกยกระดับเป็น requirement โดยไม่มีหลักฐาน
- [x] มี Week06 Use สำหรับรายการที่พร้อมทำ model

## 7. Week06 Handoff

| Week06 artefact | Input ที่เหมาะสม |
|---|---|
| User Story | FR-EQP-01, FR-EQP-06, FR-EQP-07, FR-EQP-09, FR-EQP-10, FR-EQP-11, FR-EQP-12 |
| Use Case | FR-EQP-09/FR-EQP-10 เป็น main flow ของ UC-01; FR-EQP-11 เป็น main flow ของ UC-02; FR-EQP-12 เป็น main flow ของ UC-03; FR-EQP-08 เป็น main flow ของ UC-04 |
| Acceptance Criteria | FR-EQP-02, FR-EQP-03 หลังยืนยันรายละเอียดหลักฐาน/สิทธิ์ |
| Quality Scenario | NFR-EQP-01, NFR-EQP-03 |
| Extension / Alternate Flow | FR-EQP-04, FR-EQP-05 หลังยืนยันเกณฑ์ (ไม่ได้ใช้ใน scope v2 ปัจจุบัน) |