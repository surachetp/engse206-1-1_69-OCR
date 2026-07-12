# ENGSE206 Student Project Template

> **สำหรับนักศึกษาเท่านั้น** — ใช้เป็น repository ส่วนตัวของนักศึกษาแต่ละคนหรือแต่ละคู่ ตั้งแต่ Pre-learning จนถึง Day 6

Repository นี้ไม่มีเอกสารเฉลย ไม่มี rubric ภายในของผู้สอน ไม่มี teaching slides และไม่มี model solution ของกรณีศึกษา เพื่อให้เป็นพื้นที่ทำงานและส่งผลงานของนักศึกษาโดยตรง

## เริ่มต้นที่นี่

1. อ่าน [`START_HERE_TH.md`](START_HERE_TH.md)
2. กรอกข้อมูลทีมใน [`TEAM.md`](TEAM.md)
3. ทำ Pre-learning ใน [`docs/00_prelearning/`](docs/00_prelearning/)
4. ใช้ repository เดิมทำงานต่อเนื่อง Day 1 → Day 6
5. Commit และ push หลังแต่ละ checkpoint
6. ส่ง URL ของ repository, tag หรือ release ตามที่ผู้สอนกำหนด

## โครงสร้างหลัก

```text
engse206-student-project-template/
├── START_HERE_TH.md
├── HOW_TO_USE_THIS_REPO_TH.md
├── PROJECT_STATUS.md
├── TEAM.md
├── AI_USAGE_LOG.md
├── GIT_WORKFLOW.md
├── docs/
│   ├── 00_prelearning/
│   ├── 01_day1_problem_discovery/
│   ├── 02_day2_elicitation/
│   ├── 03_day3_requirement_analysis/
│   ├── 04_day4_srs_traceability/
│   ├── 05_day5_architecture_ux/
│   └── 06_day6_detailed_design_review/
├── evidence/
├── assets/
├── references/
└── submission/
```

## ผลงานตามลำดับ 6 วัน

| ช่วง | ผลงานหลัก |
|---|---|
| Pre-learning | P00 Case Selection Proposal + Readiness Check |
| Day 1 | P01 Problem Brief + P02 Stakeholder / Context / Scope |
| Day 2 | P03 Elicitation Plan + P04 Evidence Log / Issue List |
| Day 3 | P05 Prioritized Backlog + P06 User Stories/Use Cases + P07 Requirement Model |
| Day 4 | P08 SRS + P09 Review Report + P10 Traceability + P11 Change Analysis |
| Day 5 | P12 Design Strategy + P13 Architecture + P14 User Flow/Prototype + P15 Usability Plan |
| Day 6 | P16 Detailed Design + P17 Review + P18 Final Revision + P19 Pitch + P20 Reflection |

## กติกาความลับและข้อมูลจริงจากโรงงาน

- ใช้นามแฝงแทนชื่อโรงงาน หน่วยงาน บุคคล ระบบ หรือผลิตภัณฑ์จริง
- ห้ามอัปโหลดข้อมูลลูกค้า ข้อมูลพนักงาน ตัวเลขการผลิต รหัสภายใน เอกสารลับ หรือข้อมูลส่วนบุคคล
- เก็บเฉพาะหลักฐานที่สรุปแล้วและปลอดภัยต่อการเผยแพร่
- หากใช้ AI ต้องไม่ป้อนข้อมูลลับ และต้องบันทึกใน [`AI_USAGE_LOG.md`](AI_USAGE_LOG.md)

## Commit ที่แนะนำ

```text
D0: submit pre-learning case proposal
D1: frame problem and stakeholder scope
D2: add elicitation evidence and issues
D3: prioritize requirements and acceptance criteria
D4: baseline SRS and traceability
D5: add architecture and prototype
D6: add detailed design and review evidence
FINAL: revise requirement-to-design package
```

## คู่มือเพิ่มเติม

- [`HOW_TO_USE_THIS_REPO_TH.md`](HOW_TO_USE_THIS_REPO_TH.md) — คู่มือใช้งานแบบละเอียด
- [`GIT_WORKFLOW.md`](GIT_WORKFLOW.md) — วิธี commit, push, tag และทำงานเดี่ยว/คู่
- [`SUBMISSION_GUIDE_TH.md`](SUBMISSION_GUIDE_TH.md) — แนวทางส่งงานแต่ละวัน
- [`PROJECT_STATUS.md`](PROJECT_STATUS.md) — ตารางติดตามความคืบหน้า
