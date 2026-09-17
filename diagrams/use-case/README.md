# Use Case Diagrams

ใส่ use case diagram และเชื่อมกับ UC-ID ใน docs/06

## Checklist

- [x] มี source file ที่แก้ไขได้
- [x] มี PNG/PDF export สำหรับใช้ในเอกสาร
- [x] ชื่อไฟล์สื่อถึง purpose
- [x] เชื่อมโยงกับ requirement/design document

## Use Case Diagram (ภาพรวมทั้งระบบ) — v2

![Use Case Diagram — ระบบยืม–คืนอุปกรณ์กีฬาและกิจกรรม](use-case-overview-v2.png)

Source: [`use-case-overview-v2.svg`](use-case-overview-v2.svg) · เชื่อมโยงกับ [docs/06-requirement-models.md](../../docs/06-requirement-models.md)

## Diagram แยกรายตัว

| UC | Diagram |
|---|---|
| UC-01 เพิ่ม/ดูรายการอุปกรณ์ | [UC-01-v2.svg](UC-01-v2.svg) · [UC-01-v2.png](UC-01-v2.png) |
| UC-02 ยืมอุปกรณ์ | [UC-02-v2.svg](UC-02-v2.svg) · [UC-02-v2.png](UC-02-v2.png) |
| UC-03 คืนอุปกรณ์ | [UC-03-v2.svg](UC-03-v2.svg) · [UC-03-v2.png](UC-03-v2.png) |
| UC-04 ดูข้อมูลสรุปการใช้งานอุปกรณ์ | [UC-04-v2.svg](UC-04-v2.svg) · [UC-04-v2.png](UC-04-v2.png) |

## หมายเหตุ

- v2 คือ diagram เวอร์ชันล่าสุดที่ตรงกับขอบเขต use case แบบง่าย (เพิ่ม/ดูอุปกรณ์ → ยืม → คืน → ดูข้อมูลสรุป)
- ไฟล์เวอร์ชันเดิม (`use-case-overview.svg/png`, `UC-01.svg`…`UC-08.svg/png`) ยังเก็บไว้ในโฟลเดอร์นี้เป็นข้อมูลอ้างอิง ไม่ได้ลบ
