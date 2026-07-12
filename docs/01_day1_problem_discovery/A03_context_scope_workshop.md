# A03 — System Context and Scope Workshop

> กิจกรรมนี้ช่วยให้ทีมกำหนด “ขอบเขตที่ทำจริงได้” ภายในรายวิชา และไม่หลุดไปทำระบบใหญ่เกินจำเป็น

## วัตถุประสงค์

- สร้าง system context diagram แบบง่าย
- แยก in scope / out of scope ให้ชัด
- ระบุ constraints และประเด็น ethics/privacy เบื้องต้น
- เตรียมข้อมูลสำหรับ `P02_stakeholder_context_scope.md`

## เวลาแนะนำ

60–75 นาที

## วิธีทำ

### Step 1: วาด System Context แบบง่าย
ให้วาง “ระบบของเรา” ไว้ตรงกลาง แล้วเชื่อมกับ

- ผู้ใช้หลัก
- เจ้าหน้าที่/ผู้ปฏิบัติงาน
- ระบบภายนอก (ถ้ามี)
- นโยบาย/กฎ/ข้อกำหนด

ตัวอย่าง

```mermaid
flowchart LR
  U[ผู้ขอจอง] --> S[Campus Resource Booking]
  A[เจ้าหน้าที่] --> S
  S --> N[นโยบายการจอง]
  S --> X[ระบบปฏิทิน/อีเมล (ถ้ามี)]
```

### Step 2: ระบุ In Scope / Out of Scope
หลักคิดสำคัญคือ “อะไรจำเป็นต่อการแก้ปัญหาหลัก”

ตัวอย่างสำหรับ Campus Resource Booking

#### In Scope
- ผู้ใช้ค้นหาทรัพยากรและส่งคำขอจองได้
- เจ้าหน้าที่ตรวจสอบและอนุมัติ/ปฏิเสธได้
- ระบบแสดงสถานะคำขอและประวัติพื้นฐานได้

#### Out of Scope
- ระบบชำระเงินเต็มรูปแบบ
- การเชื่อมต่อทุกระบบของมหาวิทยาลัย
- รายงานวิเคราะห์เชิงบริหารอย่างละเอียด

### Step 3: ระบุ Constraints และ Assumptions

ตัวอย่างคำถาม

- มีเวลา/ทรัพยากรจำกัดอย่างไร?
- ผู้ใช้ทุกคนมีบัญชีอยู่แล้วหรือไม่?
- จำเป็นต้องใช้งานผ่านมือถือไหม?
- ข้อมูลใดไม่ควรถูกเก็บหรือเผยแพร่?

### Step 4: Ethics / Privacy / Responsible AI Check

ให้ทีมตอบอย่างน้อย

1. มีข้อมูลส่วนบุคคลใดบ้างที่เกี่ยวข้อง?
2. ถ้าใช้ AI ช่วยสรุป requirement จะหลีกเลี่ยงการป้อนข้อมูลอ่อนไหวอย่างไร?
3. ถ้ามีการตัดสินใจอัตโนมัติ เช่น แนะนำทรัพยากร จะกระทบ fairness หรือไม่?

## Worksheet

### 1) Context Actors
- Primary user:
- Supporting staff:
- External system/policy:

### 2) In Scope
- _เติมอย่างน้อย 3 ข้อ_

### 3) Out of Scope
- _เติมอย่างน้อย 3 ข้อ_

### 4) Constraints / Assumptions / Ethics
| Item | Type | Impact | Response |
|---|---|---|---|
| _เติม_ | Constraint / Assumption / Ethics | _เติม_ | _เติม_ |

## สิ่งที่ต้องส่งออกจากกิจกรรมนี้

- context diagram แบบง่าย 1 ภาพ/1 block
- in scope อย่างน้อย 3 ข้อ
- out of scope อย่างน้อย 3 ข้อ
- ตาราง constraints และ ethics/privacy เบื้องต้น
