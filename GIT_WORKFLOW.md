# Git Workflow สำหรับ Portfolio

## กติกาง่าย ๆ

1. ทำงานในไฟล์ Markdown ตามโฟลเดอร์ของแต่ละวัน
2. Commit ทุกครั้งที่ artefact ถึง checkpoint ที่ตรวจได้
3. เขียน commit message ให้สื่อสารว่าอะไรเปลี่ยนและอยู่ในวันใด
4. เก็บรูป/ไฟล์ประกอบไว้ใน `evidence/` หรือ `assets/` และอ้างอิงจากเอกสาร
5. อย่าลบ revision log เพื่อซ่อนการแก้งาน; history คือหลักฐานของการเรียนรู้

## ตัวอย่างคำสั่งพื้นฐาน

```bash
git status
git add .
git commit -m "D1: frame problem and stakeholder scope"
git push
```

## ก่อนส่ง final

- [ ] ทุกไฟล์ P00–P20 ที่เกี่ยวข้องมีเนื้อหาครบ
- [ ] มี traceability อย่างน้อย need/evidence → requirement → design → verification idea
- [ ] AI usage log อัปเดต
- [ ] ลบ/ปกปิดข้อมูลลับหรือข้อมูลส่วนบุคคลแล้ว
- [ ] `TEAM.md` และ individual reflection ครบ
