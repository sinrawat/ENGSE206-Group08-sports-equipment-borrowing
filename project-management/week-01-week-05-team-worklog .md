# Week 01-05 Worklog — Team 08 (Case 08: ระบบยืม–คืนอุปกรณ์กีฬาและกิจกรรม)



**สมาชิกทีม** (จาก `03-elicitation-plan.md` §5): ศิลวัต อาซอง, กฤตเมธ สินธุใส, กิตติภพ สว่างเจริญทรัพย์

| Week | Date | Name | Role | Files / Task | Evidence / Commit | Time spent | Reflection |
|---|---|---|---|---|---|---:|---|
| 01 | 13/07/2569 | กฤตเมธ สินธุใส | Facilitator | วิเคราะห์ Case 08 และจัดทำ Problem Brief: pain points (PP-01–04), stakeholders เริ่มต้น, initial user needs | `docs/01-problem-brief-v0.1.md` | 2.0 h | *(ร่าง)* การแยก pain point ของแต่ละกลุ่ม (ผู้ดูแล/ผู้ยืม/ชมรม/เจ้าหน้าที่) ตั้งแต่ต้นช่วยให้เห็นว่าปัญหาจองซ้ำซ้อนกับข้อพิพาทความชำรุดเป็นคนละเรื่องที่ต้องแก้แยกกัน |
| 01 | 13/07/2569 | ศิลวัต อาซอง | Lead Interviewer | จัดทำ `docs/00-project-profile.md` (elevator pitch, scope ระดับสูง, success criteria เริ่มต้น) | `docs/00-project-profile.md` | 1.0 h | *(ร่าง)* การเขียน elevator pitch สั้นๆ บังคับให้ทีมตกลงกันก่อนว่าจะเน้นแก้ปัญหาอะไรเป็นหลัก ไม่ใช่พยายามทำทุกอย่างในระบบเดียว |
| 02 | 13/07/2569 | กฤตเมธ สินธุใส | Facilitator | ร่วมวิเคราะห์ Stakeholder, Context และ Scope กับทีม | Draft discussion | 1.0 h | *(ร่าง)* การคุยร่วมกันช่วยให้เห็นมุมมองของผู้ดูแลอุปกรณ์และชมรมที่ต่างกันชัดขึ้น โดยเฉพาะเรื่องอำนาจอนุมัติที่ยังไม่ชัดตั้งแต่ Week 1 |
| 02 | 13/07/2569 | กิตติภพ สว่างเจริญทรัพย์ | Evidence controller | จัดทำเอกสาร `02-stakeholder-context-scope.md`: Stakeholder Map, System Context, Scope Statement (In/Out), Business Rules BR-01–05 | `docs/02-stakeholder-context-scope.md` | 2.0 h | *(ร่าง)* การแยก In/Out of scope ชัดเจนตั้งแต่ตอนนี้ (เช่น กันบัญชี/ค่าปรับออก) ช่วยไม่ให้ทีมหลงไปออกแบบฟีเจอร์ที่เกินขอบเขตวิชาในสัปดาห์ถัดไป |
| 02 | 13/07/2569 | ศิลวัต อาซอง | Lead Interviewer | สร้าง Stakeholder Map / System Context diagram | `diagrams/stakeholder/stakeholder-map.png`, `diagrams/context/system-context.png` | 1.5 h | *(ร่าง)* ตอนวาด diagram พบว่าควรระบุช่องทางแจ้งเตือนภายนอก (อีเมลมหาวิทยาลัย) เป็นสมมติฐานไว้ชัดเจน เพราะยังไม่มีหลักฐานว่าใช้ได้จริง |
| 03 | 21/07/2569 | กฤตเมธ สินธุใส | Facilitator / Timekeeper | เชื่อม Open Questions (OQ-01–05) กับ Elicitation Objectives (EO-01–06) และวางแผนเก็บข้อมูล; รับผิดชอบ EO-02 | `docs/03-elicitation-plan.md` | 1.5 h | *(ร่าง)* การผูก EO แต่ละข้อกับ OQ เดิมทำให้เห็นว่าคำถามไหนสำคัญที่สุด โดยเฉพาะเรื่องหลักฐานสภาพอุปกรณ์ที่เป็นความเสี่ยงข้อพิพาทสูงสุด |
| 03 | 21/07/2569 | ศิลวัต อาซอง | Lead Interviewer / Note-taker | ออกแบบคำถามสัมภาษณ์ Q-01–Q-08, Opening/Closing script, Consent Plan; รับผิดชอบ EO-01, EO-04 | `docs/03-interview-guide.md` | 2.0 h | *(ร่าง)* คำถามปลายเปิด (เช่น Q-02 เรื่องตรวจสภาพอุปกรณ์) ช่วยให้ผู้ตอบเล่าเหตุการณ์จริงมากกว่าถามตรงว่า "อยากได้ฟีเจอร์อะไร" |
| 03 | 21/07/2569 | กิตติภพ สว่างเจริญทรัพย์ | Evidence controller / Quality Reviewer | รับผิดชอบ EO-03, EO-05; ตรวจคำถามไม่ให้ชี้นำ | `docs/03-elicitation-plan.md` §3 | 1.5 h | *(ร่าง)* ตอนตรวจคำถามพบว่าบางข้อเสี่ยงชี้นำ (เช่นถามนำเรื่องถ่ายรูป) จึงปรับเป็นคำถามปลายเปิดก่อนนำไปสัมภาษณ์จริง |
| 04 | 21/07/2569 | กิตติภพ สว่างเจริญทรัพย์ | Evidence controller | สัมภาษณ์จริง 4 กลุ่ม stakeholder และบันทึกเป็น Evidence Log (E-01–E-08) พร้อม tag และ confidence | `docs/04-evidence-log.md` | 2.0 h | *(ร่าง)* การแยก statement กับ interpretation ของทีมออกจากกันในตารางเดียวกัน ทำให้ตรวจย้อนได้ง่ายว่าอันไหนคือคำพูดจริงของผู้ให้สัมภาษณ์ |
| 04 | 21/07/2569 | ศิลวัต อาซอง | Lead Interviewer | แปลง Evidence เป็น Need (N-01–N-06) และ Requirement Candidates (RC-01–RC-06) พร้อม traceability matrix | `docs/04-requirement-candidates.md` | 1.5 h | *(ร่าง)* RC-02 กับ RC-05 มี evidence จาก stakeholder มากกว่า 1 กลุ่มยืนยันตรงกัน ทำให้มั่นใจในสอง candidate นี้มากกว่าข้ออื่น |
| 04 | 21/07/2569 | กฤตเมธ สินธุใส | Facilitator | วิเคราะห์ conflict 3 ประเด็น (เรียกคืนก่อนกำหนด, อนุมัติอุปกรณ์พิเศษ, ขอบเขต reporting) และบันทึกผลเจรจา | `docs/04-negotiation-record.md` | 1.5 h | *(ร่าง)* การแยก Position กับ Interest ของแต่ละฝ่ายออกจากกันทำให้เห็นว่าทางเลือกที่ดีที่สุดไม่ใช่การเลือกข้างใดข้างหนึ่งเสมอไป เช่นกรณีเรียกคืนก่อนกำหนดที่ให้ผู้ดูแลอุปกรณ์ตัดสินใจแทนระบบอัตโนมัติ |
| 05 | 11/08/2569 | กิตติภพ สว่างเจริญทรัพย์ | Quality Reviewer | จัดลำดับ requirement ด้วย MoSCoW (v0.1) และตรวจว่า scope ไม่ขยายเกิน Scope Statement เดิม | `docs/05-requirement-backlog.md` | 1.5 h | *(ร่าง)* การเทียบ RC-06 (dashboard) กับ Scope Statement เดิมทำให้เห็นว่าเป็น need ใหม่ที่ต้องตรวจสอบก่อนใส่เป็น Must |
| 05 | 11/08/2569 | ศิลวัต อาซอง | Lead Interviewer | จัดทำ Prioritization Rationale (เหตุผล value/risk/urgency/dependency รายข้อ) | `docs/05-prioritization-rationale.md` | 1.0 h | *(ร่าง)* การเขียนเหตุผลแยกเป็น 4 มิติบังคับให้ทีมอธิบายได้ว่าทำไม requirement หนึ่งถึง Must อีกอันถึง Should แทนที่จะเดาจากความรู้สึก |
| 05 | 11/08/2569 | กฤตเมธ สินธุใส | Facilitator | รวบรวม Open Questions ใหม่ (OQ-W05-01–06) และ Issues ที่ต้อง Hold | `docs/05-open-questions-and-issues.md` | 1.0 h | *(ร่าง)* พบว่า OQ-03 เดิม (เรื่องคืนอุปกรณ์ล่าช้า) ไม่มี evidence ตอบเลยทั้งที่ตั้งใจถามไว้ตั้งแต่ Week 3 ต้องวางแผนสัมภาษณ์เพิ่ม |
| 05 | 18/08/2569 | ทั้งทีม | — | ทำ Requirement Baseline Review self-directed studio: Artefact Health Check, Traceability Audit, Quality & MoSCoW Check | `evidence/week-05/baseline-review/` | 4.0 h (รวมทีม) | *(ร่าง)* พบว่า NFR เดิมใช้คำว่า "ใช้งานง่าย" แบบไม่มีตัวเลขวัดผล และ FR เรื่องสถานะอุปกรณ์รวมสองความสามารถไว้ข้อเดียว เป็นบทเรียนสำคัญเรื่องการเขียน requirement ให้ตรวจสอบได้ |
| 05 | 18/08/2569 | กิตติภพ สว่างเจริญทรัพย์ | Quality Reviewer | แก้ requirement backlog เป็น v0.2 ให้วัดผลได้ (เติมตัวเลข, แยก atomic requirement) | `docs/05-requirement-backlog.md` (v0.2) | 1.5 h | *(ร่าง)* การแยก FR ที่รวมสองเรื่องออกเป็นสองข้อทำให้ปิด acceptance criteria ได้ง่ายขึ้นมากในขั้นถัดไป |
| 05 | 18/08/2569 | ศิลวัต อาซอง | Lead Interviewer | ปรับปรุง Interview Guide (เพิ่ม Q-09–Q-12 + Bias Check) และ Evidence Log (เพิ่ม Tag system + Triangulation) เป็น v0.2 | `docs/03-interview-guide.md`, `docs/04-evidence-log.md` (v0.2) | 1.5 h | *(ร่าง)* การเพิ่มคำถามเรื่องคืนล่าช้าโดยเฉพาะ (แยกจากเรื่องเรียกคืนก่อนกำหนด) ช่วยปิดช่องว่างที่หลุดไปตั้งแต่ Week 3 |
| 05 | 20/08/2569 | กฤตเมธ สินธุใส | Facilitator | เตรียมแบบฟอร์ม Peer Cross-Review และตรวจสถานะ Readiness Gate เทียบกับ GitHub repo จริง | `ENGSE206_RBR_PeerReview_Template_Case08.xlsx` | 1.0 h | *(ร่าง)* การเปิด repo จริงเทียบกับสิ่งที่คุยกันในแชททำให้รู้ว่าไฟล์ที่แก้แล้วยังไม่ถูก push เข้า repo จริงเลย ต้องรีบ commit ก่อน deadline |
| 05 | 20/08/2569 | ศิลวัต อาซอง | Lead Interviewer | กรอก `docs/00-project-profile.md` ให้ครบ | `docs/00-project-profile.md` | 0.5 h | *(ร่าง)* ยังขาดข้อมูลภาคการศึกษาและชื่ออาจารย์ผู้สอนที่ต้องถามเพิ่มก่อนส่งงานจริง |

## สถานะความน่าเชื่อถือของแต่ละคอลัมน์

| คอลัมน์ | ความน่าเชื่อถือ |
|---|---|
| Files / Task, Evidence / Commit | สูง — อิงจากชิ้นงานจริงที่มีอยู่ |
| Name, Role (แถว Week 03) | สูง — มีหลักฐานจาก `03-elicitation-plan.md` §5 |
| Name, Role (แถวอื่นๆ) | ต่ำ — เดาจากบทบาทที่แต่ละคนถืออยู่ใน Week 03 ไม่มีหลักฐานตรง |
| Time spent | ต่ำ — ประมาณจากรูปแบบงานที่คล้ายกัน ไม่ใช่เวลาจริง |
| Reflection | ต่ำที่สุด — Claude แต่งให้เข้ากับเนื้อหา **ไม่ใช่ความคิดจริงของใคร ต้องเขียนใหม่เอง** |

## สิ่งที่ยังต้องทำจริง (ไม่ใช่แค่กรอกเอกสาร)

- [ ] commit + tag `baseline-v1.0` — ยังไม่มีแถวสำหรับสิ่งนี้เพราะยังไม่เกิดขึ้นจริง (ดู `ENGSE206_Team08_LiveStatus_Check.xlsx`)
- [ ] แก้ Name/Time spent/Reflection ทุกแถวให้ตรงกับความจริงก่อนส่ง — ไฟล์นี้เป็นแค่โครงร่างเริ่มต้น