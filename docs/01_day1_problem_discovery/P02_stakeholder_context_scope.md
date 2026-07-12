P02 — Stakeholder, Context and Scope
1. Stakeholder Map
Stakeholder	Role / Interest	Goal	Concern / Conflict
Meter Reader (พนักงานจดมิเตอร์)	ผู้เดินบันทึกข้อมูลดัชนีมิเตอร์ไฟฟ้าตามห้องพักหน้างาน	สแกนและบันทึกเลขมิเตอร์ได้รวดเร็ว ถูกต้อง โดยไม่ต้องพกกระดาษหรือพิมพ์ข้อมูลเอง	แสงสะท้อนจากฝาครอบบังตัวเลข, สัญญาณอินเทอร์เน็ตอับตามซอกตึก, ตัวเลขจานหมุนก้ำกึ่งเลื่อนหลักอ่านยาก
Billing Officer (ฝ่ายบัญชี/ออกบิล)	ผู้ตรวจสอบตัวเลขและคำนวณยอดเพื่อออกบิลค่าใช้จ่ายประจำเดือน	ได้รับข้อมูลตัวเลขมิเตอร์ที่แม่นยำเพื่อออกบิลได้ตรงเวลา	พนักงานจดเลขผิดหรือคีย์สลับจนออกบิลผิดพลาด ทำให้ต้องยกเลิกและออกบิลใหม่
Building Owner (เจ้าของหอพัก)	ผู้ควบคุม ติดตาม และตรวจสอบรายได้และประสิทธิภาพพลังงาน	ติดตามรายได้ค่าไฟ และมีหลักฐานรูปถ่ายย้อนหลังสำหรับตรวจสอบ	เกิดข้อพิพาทกับผู้เช่าเกี่ยวกับค่าไฟ หรือข้อมูลสูญหายและทุจริต
Tenant (ผู้เช่าห้องพัก)	ผู้ใช้งานไฟฟ้าและผู้รับภาระค่าใช้จ่าย	ได้รับบิลค่าไฟถูกต้องตรงตามการใช้งานจริง	ค่าไฟแพงเกินจริงจากความผิดพลาดของระบบหรือมนุษย์ และขาดความโปร่งใส
System Administrator	ผู้ดูแลระบบ ฐานข้อมูล และความปลอดภัย	ระบบทำงานต่อเนื่อง มีเสถียรภาพ และปลอดภัย	ความถูกต้องของข้อมูล OCR และการจัดการสิทธิ์เข้าถึงข้อมูลส่วนบุคคล
2. System Context
Context Diagram
                         Building Owner
                                │
                                ▼
                     ┌───────────────────┐
                     │ Web Admin Portal  │
                     └─────────┬─────────┘
                               ▲
                               │
                     ตรวจสอบข้อมูล/รายงาน
                               │
                               ▼

┌──────────────┐     ส่งข้อมูล      ┌───────────────────┐
│ Meter Reader │ ───────────────▶ │ OCR Meter App     │
└──────────────┘                  └─────────┬─────────┘
                                             │
                                             ▼
                                   ┌───────────────────┐
                                   │ Cloud Database    │
                                   │ & OCR Service     │
                                   └─────────┬─────────┘
                                             │
                                             ▼
                                   ┌───────────────────┐
                                   │ Web Admin Portal  │
                                   └─────────┬─────────┘
                                             │
                                             ▼
                                   ┌───────────────────┐
                                   │ Billing Officer   │
                                   └───────────────────┘
Process Flow
Meter Reader ถ่ายรูปมิเตอร์ผ่าน OCR Meter App
แอปประมวลผล OCR และบันทึกข้อมูลพร้อมรูปภาพ
ข้อมูลถูกส่งไปยัง Cloud Database
Billing Officer ตรวจสอบและอนุมัติข้อมูล
Building Owner ดูรายงานสรุปและสถิติการใช้ไฟฟ้า
3. Scope
In Scope
Mobile Camera UI (Anti-Reflection Guide)

หน้ากล้องพร้อมกรอบ Bounding Box และระบบช่วยแนะนำการเอียงกล้อง 15–30 องศาเพื่อลดแสงสะท้อน

Image Pre-processing Engine

ใช้เทคนิคเช่น Perspective Transform และ Image Enhancement เพื่อปรับภาพก่อน OCR

OCR Meter Reader Model

ระบบ AI อ่านตัวเลข 5 หลักจากมิเตอร์ไฟฟ้าแบบจานหมุน

Local Validation Logic

ตรวจสอบค่าผิดปกติ เช่น

ค่าน้อยกว่าเดือนก่อน
ค่าเพิ่มขึ้นผิดปกติ
ค่าเกิน Threshold ที่กำหนด
Offline Data Storage

เก็บข้อมูลและรูปภาพไว้ในเครื่องเมื่อไม่มีสัญญาณอินเทอร์เน็ต และซิงค์ภายหลัง

Web Admin Portal

ระบบหลังบ้านสำหรับ

จัดการห้องพัก
ดูประวัติรูปถ่าย
ตรวจสอบข้อมูลย้อนหลัง
ออกรายงานสรุป
Out of Scope
Paper Printing System

ระบบพิมพ์บิลหรือใบเสร็จโดยตรง

Online Payment Gateway

ระบบชำระเงินออนไลน์ เช่น QR Payment หรือ Credit Card

Direct Tenant Notification

การส่ง SMS, Email หรือ LINE แจ้งบิลค่าไฟให้ผู้เช่าโดยตรง

Smart Meter Integration

การเชื่อมต่อกับ Smart Meter หรือ IoT Meter

4. Constraints and Ethics / Privacy
Constraint / Issue	Impact	Response
แสงสะท้อนจากฝาครอบมิเตอร์	OCR อ่านตัวเลขผิด	Anti-Reflection Guide + Perspective Transform
พื้นที่อับสัญญาณอินเทอร์เน็ต	ส่งข้อมูลไม่ได้	Offline-First Architecture
ตัวเลขก้ำกึ่งช่วงเปลี่ยนหลัก	OCR สับสน	Human-in-the-loop ให้ผู้ใช้ยืนยันก่อนบันทึก
มิเตอร์เก่าหรือเลขจาง	OCR ล้มเหลว	Manual Key-in
ข้อมูลส่วนบุคคลของผู้เช่า	เสี่ยงต่อการละเมิดความเป็นส่วนตัว	RBAC และระบบ Login
การเข้าถึงข้อมูลโดยไม่ได้รับอนุญาต	ข้อมูลรั่วไหล	Authentication และ Access Control
ข้อมูลสูญหายระหว่างซิงค์	ขาดความถูกต้องของข้อมูล	Backup และ Data Validation
Ethics and Privacy
Human-in-the-loop

ระบบจะไม่บันทึกผล OCR อัตโนมัติทันที ผู้ใช้งานต้องตรวจสอบและยืนยันผลทุกครั้งก่อนบันทึก

Data Privacy

ข้อมูลผู้เช่าและประวัติการใช้ไฟฟ้าจะถูกเข้าถึงได้เฉพาะผู้มีสิทธิ์เท่านั้น

Transparency

ทุกค่าที่ถูกบันทึกจะมีรูปภาพหลักฐานแนบเพื่อใช้ตรวจสอบย้อนหลังได้

Accountability

ทุกการแก้ไขข้อมูลจะถูกบันทึก Log เพื่อสามารถตรวจสอบผู้ดำเนินการย้อนหลังได้

Primary Stakeholders

Meter Reader
Billing Officer

Secondary Stakeholders

Building Owner
Tenant
System Administrator
