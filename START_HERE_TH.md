# START HERE — เริ่มใช้งาน Repository นี้

เอกสารนี้เป็นขั้นตอนเริ่มต้นสำหรับนักศึกษา ใช้เวลาประมาณ 20–30 นาที

## Step 1: สร้าง Repository ของตนเอง

ผู้สอนจะให้ลิงก์ GitHub Template Repository จากนั้น

1. กด **Use this template**
2. เลือก **Create a new repository**
3. ตั้งชื่อ repository ตามรูปแบบที่ผู้สอนกำหนด เช่น

```text
engse206-2569-team01-maintenance-request
engse206-2569-solo05-room-booking
```

4. ตั้งค่า visibility ตามคำสั่งผู้สอน
5. กด **Create repository**

> ห้ามทำงานลง repository template ต้นฉบับโดยตรง

## Step 2: กรอกข้อมูลโครงการ

เปิดและแก้ไขไฟล์ต่อไปนี้

- [`TEAM.md`](TEAM.md)
- [`PROJECT_STATUS.md`](PROJECT_STATUS.md)
- [`AI_USAGE_LOG.md`](AI_USAGE_LOG.md)

จากนั้น commit ครั้งแรก เช่น

```bash
git add .
git commit -m "INIT: add team and project information"
git push
```

## Step 3: ทำ Pre-learning ก่อน Day 1

เข้าโฟลเดอร์ [`docs/00_prelearning/`](docs/00_prelearning/) และทำไฟล์

- `P00_case_selection_proposal.md`
- `P00_initial_context_and_ethics.md`
- `P00_readiness_check.md`
- `P00_submission_checklist.md`

เมื่อเสร็จแล้ว commit

```bash
git add .
git commit -m "D0: submit pre-learning case proposal"
git push
```

## Step 4: ใช้ Repository เดิมตลอด 6 วัน

อย่าสร้าง repository ใหม่ทุกวัน ให้ทำงานต่อเนื่องใน repo เดิม

```text
Day 1 → docs/01_day1_problem_discovery/
Day 2 → docs/02_day2_elicitation/
Day 3 → docs/03_day3_requirement_analysis/
Day 4 → docs/04_day4_srs_traceability/
Day 5 → docs/05_day5_architecture_ux/
Day 6 → docs/06_day6_detailed_design_review/
```

## Step 5: ส่งงานแต่ละวัน

หลังตรวจ checklist แล้ว ให้สร้าง tag ตัวอย่าง

```bash
git tag day1-submission
git push origin day1-submission
```

จากนั้นส่งอย่างน้อย

- URL ของ repository
- URL ของ tag หรือ commit ล่าสุด
- ไฟล์ PDF เฉพาะกรณีที่ผู้สอนกำหนด

อ่านรายละเอียดที่ [`SUBMISSION_GUIDE_TH.md`](SUBMISSION_GUIDE_TH.md)
