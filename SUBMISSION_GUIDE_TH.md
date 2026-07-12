# แนวทางส่งงาน Day 0–Day 6

## หลักการ

นักศึกษาใช้ repository เดิมตลอดรายวิชา และส่ง checkpoint ของแต่ละวันด้วย commit/tag ที่ชัดเจน

## ขั้นตอนก่อนส่ง

1. ตรวจไฟล์ที่กำหนดของวันนั้น
2. ตรวจว่าไม่มีข้อมูลลับหรือข้อมูลส่วนบุคคล
3. อัปเดต `AI_USAGE_LOG.md`
4. อัปเดต `PROJECT_STATUS.md`
5. commit และ push
6. สร้าง tag ตามที่ผู้สอนกำหนด

## ชื่อ tag ที่แนะนำ

```text
day0-prelearning
day1-submission
day2-submission
day3-submission
day4-submission
day5-submission
day6-submission
final-submission
```

ตัวอย่าง

```bash
git status
git add .
git commit -m "D1: complete problem brief and scope"
git push
git tag day1-submission
git push origin day1-submission
```

## สิ่งที่ส่งใน LMS / Google Classroom

- Repository URL
- Commit URL หรือ Tag URL
- ชื่อ project และรายชื่อสมาชิก
- หมายเหตุเรื่องไฟล์ภายนอก เช่น prototype link
- PDF เฉพาะเมื่อผู้สอนกำหนด

## Checklist รายวัน

### Day 0

- [ ] P00 Case Selection Proposal
- [ ] Initial Context and Ethics
- [ ] Readiness Check
- [ ] Instructor approval/pending note

### Day 1

- [ ] P01 Problem Brief
- [ ] P02 Stakeholder / Context / Scope
- [ ] Peer feedback และ revision plan

### Day 2

- [ ] P03 Elicitation Plan / Interview Guide
- [ ] P04 Evidence Log / Issue List
- [ ] Evidence ผ่านการปกปิดข้อมูลแล้ว

### Day 3

- [ ] P05 Prioritized Requirements Backlog
- [ ] P06 User Stories / Use Cases / Acceptance Criteria
- [ ] P07 Requirement Model

### Day 4

- [ ] P08 SRS v1
- [ ] P09 Requirement Review Report
- [ ] P10 Traceability Matrix
- [ ] P11 Change Request / Impact Analysis

### Day 5

- [ ] P12 Design Strategy
- [ ] P13 Conceptual Architecture
- [ ] P14 User Flow / Prototype
- [ ] P15 Usability Test Plan

### Day 6

- [ ] P16 Detailed Design
- [ ] P17 Design Review Report
- [ ] P18 Revision Log / Final Package
- [ ] P19 Design Pitch
- [ ] P20 Individual Reflection
