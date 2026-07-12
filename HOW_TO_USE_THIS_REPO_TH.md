# คู่มือการใช้ Student Project Repository

## 1. Repository นี้ใช้ทำอะไร

ใช้เป็นพื้นที่ทำงานและ portfolio ของนักศึกษาแต่ละคนหรือแต่ละคู่ ตั้งแต่ก่อนเรียนจนจบ Day 6 โดยงานทุกวันจะเชื่อมโยงกันจาก

```text
Problem → Evidence → Requirements → SRS → Architecture/UX → Detailed Design
```

## 2. วิธีทำงานในแต่ละวัน

1. เปิด `README.md` ภายในโฟลเดอร์ของวันนั้น
2. ทำกิจกรรมตามลำดับที่กำหนด
3. เติมข้อมูลในไฟล์ Pxx ที่เกี่ยวข้อง
4. เก็บภาพ แผนภาพ หรือบันทึกสนับสนุนใน `evidence/` หรือ `assets/`
5. ตรวจ checklist
6. commit และ push
7. อัปเดต `PROJECT_STATUS.md`

## 3. งานเดี่ยวและงานคู่

### งานเดี่ยว

- ทำงานบน `main` ได้โดยตรง
- commit เป็นระยะ ไม่รอรวมทุกอย่างตอนท้าย
- ใช้ reflection อธิบายการตัดสินใจของตนเอง

### งานคู่

- สมาชิกทั้งสองต้องมี commit หรือหลักฐานการมีส่วนร่วม
- ห้ามแบ่งงานแบบคนหนึ่งทำ requirement อีกคนทำ design โดยไม่เข้าใจภาพรวมร่วมกัน
- การตัดสินใจสำคัญต้องบันทึกในเอกสารหรือ revision log
- ใช้ branch สั้น ๆ ได้ เช่น

```bash
git checkout -b day3-backlog
# แก้ไขไฟล์
git add .
git commit -m "D3: draft prioritized backlog"
git push -u origin day3-backlog
```

จากนั้นสร้าง Pull Request เพื่อ review ร่วมกัน

## 4. การเก็บหลักฐาน

ใช้โฟลเดอร์เหล่านี้

```text
evidence/interviews/     บันทึกการสัมภาษณ์ที่สรุปและปกปิดข้อมูลแล้ว
evidence/observations/   บันทึกการสังเกต workflow
evidence/reviews/        feedback, peer review, review checklist
evidence/prototype/      ภาพ prototype และผลทดสอบ
assets/                  diagram, image, exported artifact
references/              แหล่งข้อมูลอ้างอิงที่เผยแพร่ได้
```

ตั้งชื่อไฟล์ให้สื่อความหมาย เช่น

```text
evidence/interviews/interview-summary-role-operator-01.md
assets/day5/conceptual-architecture-v1.png
```

## 5. การอ้างอิงภาพใน Markdown

```markdown
![Stakeholder Map](../../assets/day1/stakeholder-map-v1.png)
```

ใช้ relative path เพื่อให้ภาพเปิดได้ทั้งบนเครื่องและ GitHub

## 6. การใช้ AI อย่างรับผิดชอบ

AI ใช้ช่วยได้ เช่น

- ช่วยจัดรูปแบบตาราง
- ช่วยตรวจความกำกวมของข้อความ
- ช่วยเสนอคำถามเพิ่มเติม
- ช่วยวิจารณ์ requirement หรือ design

แต่ต้อง

- ไม่ป้อนข้อมูลลับหรือข้อมูลส่วนบุคคล
- ตรวจคำตอบกับบริบทจริง
- ไม่คัดลอกคำตอบโดยไม่เข้าใจ
- บันทึก prompt, ผลที่นำมาใช้ และการตรวจแก้ใน `AI_USAGE_LOG.md`

## 7. สิ่งที่ไม่ควรทำ

- ไม่ upload teaching slides หรือเฉลยของผู้สอนเข้า repo
- ไม่ upload rubric ภายในของผู้สอน
- ไม่คัดลอก Campus Resource Booking แบบเต็มมาเป็น case ของตนเอง
- ไม่ลบ Git history เพื่อปกปิดว่าเริ่มทำเมื่อไร
- ไม่เก็บไฟล์ขนาดใหญ่หรือข้อมูลลับโดยไม่จำเป็น

## 8. Definition of Done รายวัน

งานของวันหนึ่งถือว่าเสร็จเมื่อ

- artifact ที่กำหนดมีเนื้อหาครบ
- มีเหตุผลรองรับ ไม่ใช่เพียงข้อความสั้น ๆ
- เชื่อมโยงกับงานวันก่อนหน้า
- มี evidence หรือ reference ตามสมควร
- ผ่าน checklist
- commit, push และส่งลิงก์เรียบร้อย
