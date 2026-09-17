# Domain Models

ใส่ conceptual domain model ก่อนลงรายละเอียด class

## Checklist

- [x] มี source file ที่แก้ไขได้
- [x] มี PNG/PDF export สำหรับใช้ในเอกสาร
- [x] ชื่อไฟล์สื่อถึง purpose
- [x] เชื่อมโยงกับ requirement/design document

## Domain Model (ภาพรวม) — v2

![Domain Model — ระบบยืม–คืนอุปกรณ์กีฬาและกิจกรรม](domain-model-overview-v2.png)

Source: [`domain-model-overview-v2.svg`](domain-model-overview-v2.svg) · เชื่อมโยงกับ [docs/06-requirement-models.md](../../docs/06-requirement-models.md)

## หมายเหตุ

- v2 ตัด class ที่เกี่ยวข้องกับการจองล่วงหน้า/อนุมัติพิเศษ/หลักฐานสภาพแยกออก เหลือเฉพาะ entity หลักที่รองรับ เพิ่ม/ดูอุปกรณ์ → ยืม → คืน → สรุปการใช้งาน
- ไฟล์เวอร์ชันเดิม (`domain-model-overview.svg/png`) ยังเก็บไว้ในโฟลเดอร์นี้เป็นข้อมูลอ้างอิง ไม่ได้ลบ
