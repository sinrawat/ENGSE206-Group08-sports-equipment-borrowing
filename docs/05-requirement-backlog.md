# 05 — Requirement Backlog v0.1: ระบบยืม–คืนอุปกรณ์กีฬาและกิจกรรม (Case 08)

> **Case:** ระบบยืม–คืนอุปกรณ์กีฬาและกิจกรรม
> **Source:** Week04 — `04-evidence-log.md` (E-01..E-08, N-01..N-06), `04-requirement-candidates.md` (RC-01..RC-06), `04-negotiation-record.md` (Negotiation N-01..N-03)
> **Status:** Draft สำหรับ Week05
> **Goal:** จัดประเภท จัดลำดับ และแยกสิ่งที่พร้อมใช้ต่อ Week06 ออกจากสิ่งที่ยังต้องถามต่อ

## 1. Project Metadata

| Field | Value |
|---|---|
| Course / Week | ENGSE206 / Week05 |
| Team | Team 08 |
| Case | Case 08 — ระบบยืม–คืนอุปกรณ์กีฬาและกิจกรรม |
| Source Week04 files | `04-evidence-log.md`, `04-requirement-candidates.md`, `04-negotiation-record.md` |
| Backlog version | `v0.1` |
| Date | 11/08/2569 |

> **หมายเหตุการอ้างอิง ID:** เอกสาร Week04 มีการใช้รหัส `N-xx` สองความหมาย — `N-01..N-06` ใน `04-evidence-log.md` หมายถึง **Need** ส่วน `N-01..N-03` ใน `04-negotiation-record.md` หมายถึง **ประเด็นเจรจา (conflict record)**. เอกสารนี้จะระบุแหล่งกำกับไว้ทุกครั้งว่าเป็น "Need" หรือ "Negotiation" เพื่อไม่ให้สับสน

## 2. Prioritization Method

ใช้ MoSCoW โดยไม่ใช้ความรู้สึกของทีมเป็นหลัก แต่ดูจาก 4 มิติ

| Dimension | วิธีใช้ในเคสนี้ |
|---|---|
| Value | ช่วยผู้ยืม/ผู้ดูแลอุปกรณ์/ชมรม/เจ้าหน้าที่แก้ pain point หลักได้หรือไม่ (อ้างอิง PP-01..PP-04) |
| Risk | ถ้าขาด requirement นี้ จะเกิดข้อพิพาทความชำรุด จองซ้ำซ้อน หรืออุปกรณ์สูญหายโดยไม่มีผู้รับผิดชอบหรือไม่ |
| Urgency | จำเป็นต่อ workflow รุ่นแรกของระบบ หรือเป็นเรื่องปรับปรุงภายหลัง |
| Dependency | ต้องรอเกณฑ์/นโยบาย (เช่น เกณฑ์ "อุปกรณ์พิเศษ", ขอบเขต reporting) จากผู้มีอำนาจก่อนหรือไม่ |

## 3. Requirement Backlog v0.1

| Req ID | Source RC | Evidence / Need Trace | Requirement Statement | Type | Priority | Rationale | Status | Open Question | Week06 Use |
|---|---|---|---|---|---|---|---|---|---|
| FR-EQP-01 | RC-01 | E-01 → Need N-01 | ระบบต้องให้ผู้ดูแลอุปกรณ์บันทึกและค้นหาประวัติการยืม–คืนของอุปกรณ์แต่ละชิ้นแบบดิจิทัล แทนที่สมุดบันทึกกระดาษ | Functional | Must | เป็น core capability ที่แทนที่ workflow กระดาษเดิมโดยตรง และเป็นฐานข้อมูลที่ requirement อื่นเกือบทั้งหมดต้องอ้างอิง | Needs Follow-up | ยืนยันว่าการค้นประวัติที่ต้องการคือระดับรายอุปกรณ์ รายผู้ยืม หรือทั้งสองแบบ | Use Case + User Story |
| FR-EQP-02 | RC-02 | E-02, E-05 → Need N-02 | ระบบต้องให้ผู้ดูแลอุปกรณ์บันทึกสภาพอุปกรณ์พร้อมหลักฐานภาพถ่ายทั้งตอนส่งมอบและตอนรับคืน โดยให้ทั้งผู้ดูแลอุปกรณ์และผู้ยืมดูข้อมูลนี้ได้ | Functional / Accountability | Must | หลักฐานตรงกันจาก stakeholder 2 ฝ่าย (ผู้ดูแลอุปกรณ์ + ผู้ยืม) แก้ pain point เรื่องข้อพิพาทความชำรุดโดยตรง (PP-01, E-02, E-05) | Needs Follow-up | ใครเป็นผู้ถ่ายภาพ และจะเก็บ/รักษาหลักฐานไว้ที่ไหน | Use Case + Acceptance Criteria |
| FR-EQP-03 | RC-03 | E-03 → Need N-03; Negotiation N-02 (Needs Validation, Option B) | ระบบต้องส่งคำขอไปให้ผู้มีอำนาจระดับสูง (หัวหน้าศูนย์กีฬา/อาจารย์ผู้รับผิดชอบ) อนุมัติ เมื่อคำขอเกี่ยวข้องกับอุปกรณ์ที่จัดเป็นประเภทพิเศษ/ราคาสูง พร้อมหลักฐานกิจกรรมที่ได้รับอนุมัติและวันคืนที่ชัดเจน | Functional / Authorization | Should | สำคัญต่อการควบคุมความเสียหายทางการเงิน แต่เกณฑ์ "อุปกรณ์พิเศษ" ยังไม่ยืนยัน (dependency สูง) จึงยังไม่ครบสมบูรณ์พอเป็น Must | Needs Follow-up | เกณฑ์ราคา/รายการที่นับเป็น "อุปกรณ์พิเศษ", ผู้มีอำนาจระดับสูงคือใครกันแน่, SLA เวลาอนุมัติ | Use Case Extension |
| FR-EQP-04 | RC-04 | E-04 → Need N-04; Negotiation N-01 (Provisional, Option B) | ระบบต้องรองรับการเรียกคืนอุปกรณ์ก่อนกำหนด โดยให้ผู้ดูแลอุปกรณ์เป็นผู้อนุมัติ พร้อมบันทึกเหตุผลและแจ้งล่วงหน้าแก่ผู้ยืมเดิม | Functional / Business Rule | Should | negotiation ได้ทิศทาง Provisional แล้ว (ผู้ดูแลอุปกรณ์ตัดสินใจแทน auto-recall) แต่เกณฑ์ความจำเป็นเร่งด่วนและระยะเวลาแจ้งล่วงหน้าขั้นต่ำยังไม่ยืนยัน | Needs Follow-up | เกณฑ์ "ความจำเป็นเร่งด่วนกว่า", ระยะเวลาแจ้งล่วงหน้าขั้นต่ำ, การชดเชยผู้ยืมเดิม | Use Case Extension + State Rule |
| FR-EQP-05 | RC-05 | E-06, E-07 → Need N-05 | ระบบต้องแสดงสถานะความพร้อมของอุปกรณ์แบบเรียลไทม์ และป้องกันการจองซ้ำซ้อนของอุปกรณ์ชิ้นเดียวกันจากคำขอจองล่วงหน้าที่ทับซ้อนกันของชมรมต่าง ๆ | Functional / Integrity | Must | ชมรม/ผู้จัดกิจกรรมจัดเป็นปัญหาอันดับ 1 (Q-07) และมีหลักฐานยืนยันสองชั้น (ตัวเลขวันจอง + priority ranking) | Ready for Week06 | ยืนยันว่าช่วงเวลาจองล่วงหน้า (ปัจจุบันอ้างอิงจากชมรมเดียว 5–7 วัน) สอดคล้องกันทุกประเภทชมรมหรือไม่ | Use Case (main flow) + User Story |
| FR-EQP-06 | RC-06 (เฉพาะส่วนสรุปการใช้งาน/สถานะ) | E-08 → Need N-06; Negotiation N-03 (Unresolved, รับได้เฉพาะส่วนพื้นฐาน) | ระบบต้องมีรายงาน/แดชบอร์ดสรุปให้เจ้าหน้าที่ดูจำนวนครั้งที่อุปกรณ์แต่ละชิ้นถูกยืม ประวัติความชำรุด สถานะ/ผู้ถือครองปัจจุบัน และกำหนดคืน (ไม่รวมคำแนะนำจัดซื้อ/งบประมาณ) | Functional / Reporting | Could | เป็น need ใหม่ที่เพิ่งปรากฏจากการสัมภาษณ์เจ้าหน้าที่ ยังไม่เคยอยู่ในขอบเขตเดิม Week 2 ต้องตรวจผลกระทบต่อ Scope Statement ก่อน แม้จะมาจากผู้มีอำนาจตัดสินใจสูง | Needs Follow-up | ความถี่ของรายงานที่ต้องการ (รายสัปดาห์/รายเดือน/เรียลไทม์), ผลกระทบต่อ Scope Statement Week 2 | Follow-up only จนกว่าจะยืนยัน scope |
| NFR-EQP-01 | Scope Statement (Out of Scope: บัญชี/ค่าปรับ, ข้อมูลส่วนบุคคล) | Week 2 Scope Statement + Ethics section | ระบบต้องเก็บข้อมูลผู้ยืมเท่าที่จำเป็นต่อการยืม–คืนเท่านั้น และต้องไม่เชื่อมโยง/ประมวลผลร่วมกับระบบบัญชีหรือค่าปรับ | NFR / Constraint | Must | เป็นหลัก data minimization ที่ทีมตกลงไว้ชัดเจนตั้งแต่ Week 2 และครอบคลุม requirement อื่นหลายข้อ | Ready for Week06 | — | Quality Scenario + Constraint |
| NFR-EQP-02 | RC-02 (follow-up ด้าน access control) | E-02, E-05 + Ethics section (Week 2) | ระบบต้องจำกัดสิทธิ์การเข้าถึงหลักฐานสภาพอุปกรณ์ (ภาพถ่าย/บันทึก) เฉพาะผู้ดูแลอุปกรณ์และผู้ยืมที่เกี่ยวข้องกับรายการนั้นเท่านั้น | NFR / Constraint | Should | ป้องกันข้อพิพาทเรื่องความน่าเชื่อถือของหลักฐาน แต่รายละเอียดยังต้องรอผลจาก FR-EQP-02 (ใครถ่ายภาพ/เก็บที่ไหน) | Needs Follow-up | รายละเอียดจาก FR-EQP-02 เรื่องผู้ถ่ายภาพและสถานที่เก็บหลักฐาน | Quality Scenario |
| NFR-EQP-03 | Problem Brief §9 (Non-functional Expectations) | Week 1 — Non-functional Expectations | ระบบต้องใช้งานง่ายสำหรับนักศึกษาที่ใช้งานครั้งแรกโดยไม่ต้องมีการฝึกอบรม และแสดงผลได้ดีบนโทรศัพท์มือถือ | NFR | Should | ผู้ใช้ส่วนใหญ่เข้าถึงผ่านมือถือตามที่ระบุใน Week 1 แต่ยังไม่มีหลักฐานเชิงปริมาณยืนยันจากการสัมภาษณ์ Week 4 | Needs Follow-up | ยืนยันสัดส่วน/พฤติกรรมการใช้อุปกรณ์มือถือจริงจากผู้ใช้ | Quality Scenario |
| ISSUE-EQP-01 | RC-06 (เฉพาะส่วนคำแนะนำจัดซื้อ/งบประมาณ) | E-08 → Need N-06 | คำแนะนำเรื่องการซ่อมบำรุง/จัดซื้อ และผู้อนุมัติงบประมาณ | Issue | Won't yet | เชื่อมโยงใกล้กับส่วนบัญชี/จัดซื้อที่ Week 2 Scope Statement กันไว้นอกขอบเขตอย่างชัดเจน ห้ามฟันธงเป็น requirement โดยไม่มี scope owner ยืนยัน | Hold | ผู้สอน/scope owner ยืนยันผลกระทบต่อ scope เดิมหรือไม่ | Follow-up only |

## 4. Priority Summary

| Priority | Count | Requirement IDs | เหตุผลรวม |
|---|---:|---|---|
| Must | 4 | FR-EQP-01, FR-EQP-02, FR-EQP-05, NFR-EQP-01 | เป็นแกน workflow หลัก, แก้ pain point ข้อพิพาทและจองซ้ำซ้อนโดยตรง, และคุมขอบเขตข้อมูลส่วนบุคคลตามที่ตกลงไว้ตั้งแต่ Week 2 |
| Should | 4 | FR-EQP-03, FR-EQP-04, NFR-EQP-02, NFR-EQP-03 | มีคุณค่าสูง แต่ยังต้องยืนยันเกณฑ์/authority/รายละเอียดก่อนเขียนเป็น rule ที่สมบูรณ์ |
| Could | 1 | FR-EQP-06 | มีประโยชน์และมาจากผู้มีอำนาจตัดสินใจสูง แต่ยังไม่ยืนยันผลกระทบต่อ scope เดิม |
| Won't yet | 1 | ISSUE-EQP-01 | เสี่ยงทับซ้อนกับส่วนบัญชี/จัดซื้อที่กันไว้นอกขอบเขต ต้องมี scope owner ยืนยันก่อน |

## 5. Ready / Follow-up / Hold

| Status | Requirement IDs | สิ่งที่ต้องทำต่อ |
|---|---|---|
| Ready for Week06 | FR-EQP-05, NFR-EQP-01 | ทำ Use Case / User Story / Quality Scenario ได้เลย |
| Needs Follow-up | FR-EQP-01, FR-EQP-02, FR-EQP-03, FR-EQP-04, FR-EQP-06, NFR-EQP-02, NFR-EQP-03 | ถาม stakeholder เพิ่ม (ดู `05-open-questions-and-issues.md`) แล้วปรับ requirement ก่อนเขียน model แบบเต็ม |
| Hold | ISSUE-EQP-01 | เก็บเป็น issue รอ scope owner ยืนยัน ยังไม่เขียนเป็น requirement หรือ design |

## 6. Review Checklist

- [x] ทุก requirement มี Source RC หรือ Evidence source
- [x] ทุก requirement อ้าง Evidence / Need Trace
- [x] Type แยกเป็น Functional / NFR / Business Rule / Constraint / Issue
- [x] Priority มี rationale จาก value/risk/urgency/dependency
- [x] Unknown หรือ scope issue ไม่ถูกยกระดับเป็น requirement โดยไม่มีหลักฐาน (ISSUE-EQP-01)
- [x] มี Week06 Use สำหรับรายการที่พร้อมทำ model

## 7. Week06 Handoff

Week06 ควรเริ่มจาก requirement ที่พร้อมก่อน:

| Week06 artefact | Input ที่เหมาะสม |
|---|---|
| User Story | FR-EQP-01, FR-EQP-05 |
| Use Case | FR-EQP-05 เป็น main flow (จองอุปกรณ์ป้องกันซ้ำซ้อน); FR-EQP-01 เป็น supporting flow (ค้นประวัติ) |
| Acceptance Criteria | FR-EQP-02 หลังยืนยันผู้ถ่ายภาพ/สถานที่เก็บหลักฐาน |
| Quality Scenario | NFR-EQP-01, NFR-EQP-03 |
| Extension / Alternate Flow | FR-EQP-03, FR-EQP-04 หลังยืนยันเกณฑ์ "อุปกรณ์พิเศษ" และเกณฑ์เรียกคืนก่อนกำหนด |
