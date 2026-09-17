# Use Case Diagrams

ใส่ use case diagram และเชื่อมกับ UC-ID ใน docs/06

## Checklist

- [x] มี source file ที่แก้ไขได้
- [x] มี PNG/PDF export สำหรับใช้ในเอกสาร
- [x] ชื่อไฟล์สื่อถึง purpose
- [x] เชื่อมโยงกับ requirement/design document

## Use Case Diagram (ภาพรวมทั้งระบบ) — v2

![Use Case Diagram — ระบบยืม–คืนอุปกรณ์กีฬาและกิจกรรม](use-case-overview-v2.png)

Source: [`use-case-overview-v2.svg`](use-case-overview-v2.svg) · เชื่อมโยงกับ [docs/06-requirement-models-v2.md](../../docs/06-requirement-models-v2.md)

## Diagram แยกรายตัว

| UC | Diagram |
|---|---|
| UC-01 เพิ่มรายการอุปกรณ์ | [UC-01-v2.svg](UC-01-v2.svg) · [UC-01-v2.png](UC-01-v2.png) |
| UC-02 ดูรายการอุปกรณ์ | [UC-02-v2.svg](UC-02-v2.svg) · [UC-02-v2.png](UC-02-v2.png) |
| UC-03 ยืมอุปกรณ์ | [UC-03-v2.svg](UC-03-v2.svg) · [UC-03-v2.png](UC-03-v2.png) |
| UC-04 คืนอุปกรณ์ | [UC-04-v2.svg](UC-04-v2.svg) · [UC-04-v2.png](UC-04-v2.png) |
| UC-05 ดูข้อมูลสรุปการใช้งานอุปกรณ์ | [UC-05-v2.svg](UC-05-v2.svg) · [UC-05-v2.png](UC-05-v2.png) |

## หมายเหตุ

- v2 คือ diagram เวอร์ชันล่าสุดที่ตรงกับขอบเขต use case แบบง่าย (เพิ่มอุปกรณ์ → ดูรายการ → ยืม → คืน → ดูข้อมูลสรุป) โดยแยก UC เพิ่ม/ดูออกจากกันเป็นคนละ use case
- ไฟล์เวอร์ชันเดิม (`use-case-overview.svg/png`, `UC-01.svg`…`UC-08.svg/png`) ยังเก็บไว้ในโฟลเดอร์นี้เป็นข้อมูลอ้างอิง ไม่ได้ลบ