# ใบส่งงานสอบปลายภาค — ส่วน ก งานกลุ่ม (Change-to-Design)

> วางไฟล์นี้ที่ `final-exam/final-exam-submission.md` ใน branch `final-exam` ของ Team Repo · ถ้อยคำในวงเล็บเป็นคำแนะนำ ลบได้

| รายการ | กรอก |
|---|---|
| กลุ่ม / Case | Group 08 · Case 08 |
| ชื่อระบบ | ระบบยืม–คืนอุปกรณ์กีฬาและกิจกรรม |
| CR เสริมที่เลือก | CR-FX-02B — เวลารุ่นแรกเหลือครึ่งหนึ่ง |
| Branch | `final-exam` |
| Pull Request | `submit(final): change-to-design take-home` |
| Commit hash ฉบับคำตอบที่อ้างอิง | `f31b05d57557006bfd5bda3629e7a9512186785b` |
| สถานะ SRS ที่ใช้เป็นฐาน | Draft — ตาม SRS §0 |

## งานเดิมที่ใช้เป็นฐาน

| งาน | ไฟล์และ commit หรือวันที่ |
|---|---|
| SRS (W07) | `docs/07-srs-v1.md` ณ `f5e19eb28903781b7d0f3d14a5a9fcdeb98af788` |
| งาน W08 (review · trace · CR) | `docs/08-validation-traceability.md` ณ `f5e19eb28903781b7d0f3d14a5a9fcdeb98af788`; ID บางจุดเป็นรุ่นเก่า ให้เทียบ W06 v2/SRS |
| Design Strategy + Design Spine (W10) | `design/10-design-strategy.md`, `design/00-design-spine.md` ณ `f5e19eb28903781b7d0f3d14a5a9fcdeb98af788` ยังเป็น template |
| Conceptual Architecture (W11) | ใช้ `design/11-conceptual-architecture.md` ณ `f5e19eb28903781b7d0f3d14a5a9fcdeb98af788`; `.docx` v0.1 ยังเป็น template |

## ไฟล์ที่ส่ง

- [x] `final-exam/final-exam-group-answer.docx`
- [x] `final-exam/diagrams/context-after.drawio` + `.png`
- [x] `final-exam/diagrams/container-after.drawio` + `.png`
- [x] `final-exam/final-exam-submission.md` (ไฟล์นี้)
- [x] `final-exam/ai-use-log.md`

## สมาชิกและส่วนที่รับผิดชอบ

| ชื่อ–สกุล | รหัส | รับผิดชอบ (G / ข้อ) | หลักฐาน (commit หรือส่วนในไฟล์) |
|---|---|---|---|
| Kirttamet (GitHub) | ไม่ลงรหัสใน repo สาธารณะ | G1–G2 | G1/G2 ใน Word; commit `1105f5a29f9baa53d308f474e19ba2b3cf4e6c82` |
| sinrawat (GitHub) | ไม่ลงรหัสใน repo สาธารณะ | G3 และ G5; ร่วมตรวจ G6 | G3/G5 ใน Word; commit `fcf997e6d38f60329f134f020ff2396494e14ba3` |
| kit77-atr (GitHub) | ไม่ลงรหัสใน repo สาธารณะ | G4 และจัดชุดส่ง; ร่วมตรวจ G6 | G4 ใน Word และภาพใน `final-exam/diagrams/`; commit `6eb8dbb56b1a8ba9297bcd43c9ef3f884f553bb5` |

## รับรอง

- [x] สมาชิกทุกคนอ่านคำตอบทั้งฉบับ และอธิบายส่วนใดก็ได้ใน oral spot-check
- [x] ไม่มีตัวเลข นโยบาย หรือ protocol ที่แต่งขึ้น — ค่าที่ไม่รู้เป็น TBD และมี OI หรือ DD รองรับ
- [x] ไม่อ้างว่า SRS หรือ CR ใด Approved
- [x] ไม่ได้แก้ไฟล์งานเดิมของแต่ละสัปดาห์ — ทุกอย่างอยู่ใน `final-exam/`
