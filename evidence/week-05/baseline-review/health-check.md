# Artefact Health Check Summary (ช่วงที่ 1)

> **Case:** Case-08 — ระบบยืม–คืนอุปกรณ์กีฬาและกิจกรรม
> **Date:** 18 สิงหาคม 2569
> **Evaluator:** Facilitator & Quality Reviewer (Team 08) — กฤตเมธ สินธุใส, กิตติภพ สว่างเจริญทรัพย์

## 1. Audit Table

| เอกสาร / โฟลเดอร์ | ต้องมีอะไรอยู่ข้างใน | สถานะการตรวจ | หมายเหตุ / จุดที่ตรวจพบ |
|---|---|---|---|
| `docs/01-problem-brief-v0.1.md` | Goal เชิงผลลัพธ์, Pain points, Stakeholder เริ่มต้น, NFR เริ่มต้น | **[x] ครบ** | แยก Facts, Assumptions, Pain points (PP-01..PP-05) ชัดเจน |
| `docs/02-stakeholder-context-scope.md` | Stakeholder map, Context diagram, In/Out scope, Constraints | **[x] ครบ** | มี Stakeholder map 4 กลุ่ม, System context, In/Out scope ชัดเจน และ Business rules BR-01 ถึง BR-05 (บางข้อยังเป็นสมมติฐานที่ระบุไว้อย่างโปร่งใส) |
| `docs/03-elicitation-plan.md` + `docs/03-interview-guide.md` | Objectives, คำถามสัมภาษณ์, Bias/Privacy check | **[x] ครบ** | มี OQ-01..OQ-05 + AS-01, EO-01..EO-06 เชื่อมกับ Plan ตาราง, คำถามสัมภาษณ์ Q-01..Q-08 ครอบคลุม 4 stakeholder role, มี Privacy/Consent plan และ Elicitation risks |
| `docs/04-evidence-log.md` | หลักฐานติด Tag (E-ID), Conflict + ผลเจรจา, Requirement Candidates | **[x] ครบ** | `04-negotiation-record.md` (N-01..N-03) และ `04-requirement-candidates.md` (RC-01..RC-06) ตรวจแล้วครบ มี traceability ไป E-ID ชัดเจน |
| `docs/05-requirement-backlog.md` (จาก v0.2) | FR/NFR + Source + Priority + Acceptance measure | **[x] ครบ** | ปรับถ้อยคำให้มีเกณฑ์วัดได้แล้ว (เช่น FR-EQP-06 ≤ 3 วินาที, NFR-EQP-03 ≤ 5 คลิก / 375px) พร้อม Priority Summary และ Ready/Follow-up/Hold status — พร้อมล็อกเป็น Baseline v1.0 |

## 2. Summary & Self-Check Findings

1. **เอกสารช่วงไหนที่ทีม "ครบน้อยที่สุด"?**
   - ในช่วงแรก `docs/05-requirement-backlog.md` มีถ้อยคำเชิงคุณภาพกว้างๆ เช่น "ใช้งานง่าย" ซึ่งไม่สามารถตรวจรับได้ ทีมจึงปรับ NFR-EQP-03 ให้เป็นเกณฑ์เชิงปริมาณ (ทำรายการยืมสำเร็จภายใน 5 คลิก และรองรับหน้าจอความกว้าง 375px) ระหว่าง Quality Review
   - นอกจากนี้ RC-03 (อุปกรณ์พิเศษ), RC-04 (เรียกคืนก่อนกำหนด) และ RC-06 (dashboard) ยังต้องคง Priority ไว้ที่ Should/Could และสถานะ "Needs Follow-up" เพราะเกณฑ์หลัก (เช่น เกณฑ์ราคาอุปกรณ์พิเศษ) ยังไม่มี evidence ยืนยัน — ทีมเลือกไม่เดาเกณฑ์เองเพื่อไม่ให้ requirement เกินหลักฐาน
2. **มีหัวข้อใดที่เคยข้ามไปตอนทำจริงไหม?**
   - มี 1 gap ที่ทีมพบและบันทึกไว้อย่างตรงไปตรงมาใน `05-open-questions-and-issues.md` (OQ-W05-06 / ISSUE-EQP-04): **การจัดการผู้คืนอุปกรณ์ล่าช้า** ยังไม่มี evidence จากการสัมภาษณ์ Week 4 มารองรับเลย ทีมจึงยังไม่สามารถออกแบบสถานะ "ค้างคืน" หรือ workflow แจ้งเตือนได้ในตอนนี้ ต้องเก็บข้อมูลเพิ่มก่อน Week 06