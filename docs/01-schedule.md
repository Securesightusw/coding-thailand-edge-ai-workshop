# 📅 Day 1 Schedule — Edge AI Workshop (6 ชั่วโมง)

> **เป้าหมาย:** ทุกทีมจบวันด้วย Model V2 + Prediction Log + Idea Canvas พร้อมไป Prototype Day

---

## ภาพรวม Timeline

```
09:00 ─┬─ 09:30  นำเข้า + Anchor Demo (30 นาที)
       │
09:30 ─┼─ 10:00  UNO Q Setup + Modulino Tour + Git 101 (30 นาที)
       │
10:00 ─┼─ 10:30  Track Selection + Class Design Workshop (30 นาที)
       │
10:30 ─┼─ 12:00  Data Collection Hands-on (90 นาที) ★
       │
12:00 ─┼─ 13:00  พักเที่ยง
       │
13:00 ─┼─ 14:00  Train V1 + Deploy to UNO Q (60 นาที)
       │
14:00 ─┼─ 15:30  10-Case Testing + Iterate to V2 (90 นาที) ★
       │
15:30 ─┼─ 16:00  Cross-Track Demo (2 นาที/ทีม)
       │
16:00 ─┼─ 16:30  Wrap Up + Idea Canvas (30 นาที)
       │
16:30 ─┴─ 17:00  Maker Space + Token Strategy (30 นาที)
```

★ = ช่วงสำคัญที่สุด สำหรับเก็บคะแนน

---

## 📍 รายละเอียดแต่ละช่วง

### ⏰ 09:00–09:30 | นำเข้าสู่บทเรียน + Anchor Demo

**ผู้สอน:** วิทยากรหลัก

**เนื้อหา:**
1. **Edge AI คืออะไร** (5 นาที)
   - ทำไม inference ที่ edge ดีกว่า cloud
   - ตัวอย่าง real-world: ถังขยะอัจฉริยะ, smart camera, fall detector
2. **Anchor Demo: Gesture Wand** (15 นาที)
   - สาธิตจบทั้ง pipeline ต่อหน้านักเรียน
   - เก็บข้อมูล 3 ท่า (วงกลม / Z / นิ่ง) → train → deploy → demo
   - ใช้ Modulino Movement + Pixels
3. **Skill Assessment 30 คะแนน** (5 นาที)
   - ย้ำว่าประเมินตลอดวัน
   - หลักฐานคือ commit ใน GitHub repo ของทีม
4. **กฎ Day 1** (5 นาที)
   - ห้ามใช้โค้ดสำเร็จรูปจากอินเทอร์เน็ตโดยไม่อ้างอิง
   - ทุก decision ต้องอธิบายได้ (Debug & Explain)

**สื่อ:** Slide 1-8 + Live Demo

---

### ⏰ 09:30–10:00 | UNO Q Setup + Modulino Tour + Git 101

**ผู้สอน:** วิทยากร + TA

**Part A — UNO Q + Modulino (15 นาที):**
- เชื่อม USB-C, รอ boot
- ต่อ Modulino ผ่าน Qwiic — เน้น polarized connector (ผิดด้านเสียบไม่ได้)
- เปิด Arduino App Lab, login
- ลอง read sensor ดิบจาก Modulino Movement (sample sketch มีให้)

**Part B — Git 101 (15 นาที):**
- ดู [`04-git-basics.md`](04-git-basics.md)
- ทุกทีม:
       1. สร้าง repo ทีมใหม่จาก [team-repo-template](../templates/team-repo-template/)
       2. Clone repo ทีมลง laptop
  3. แก้ README ใส่ชื่อทีม + commit แรก

---

### ⏰ 10:00–10:30 | Track Selection + Class Design

**Part A — เลือก Track (10 นาที):**
- ดู [`02-tracks.md`](02-tracks.md)
- แต่ละทีมเลือก 1 track + ตัดสินใจระดับความท้าทาย (Basic/Intermediate/Advanced)
- เขียนเหตุผลในไฟล์ `docs/track-selection.md` ของ repo ทีม
- Commit + Push

**Part B — Class Design Workshop (20 นาที):**
- ใช้ Worksheet W1 [`worksheets/W1-class-design.md`](../worksheets/W1-class-design.md)
- แต่ละทีม define classes ของตัวเอง พร้อมตอบ:
  - แต่ละ class แยกกันด้วย feature อะไร?
  - มี edge case อะไรที่อาจทำให้สับสน?
  - เก็บกี่ตัวอย่าง/class? ทำไม?
- ครู/TA review ก่อนเริ่มเก็บข้อมูล

⚠️ **ห้ามเก็บข้อมูลก่อนได้รับการ approve จาก TA** — กันการเสียเวลา

---

### ⏰ 10:30–12:00 | Data Collection Hands-on ★

**ผู้สอน:** TA per 3-5 ทีม

**เนื้อหา:**
- เริ่ม Edge Impulse Studio → New Project → ตั้งชื่อ
- เชื่อม UNO Q กับ Edge Impulse (มี script ใน [`labs/setup/connect-edge-impulse.md`](../labs/setup/connect-edge-impulse.md))
- เก็บข้อมูลตามเป้าหมาย:
  - **Track A (Motion):** 50 samples × class, แต่ละ sample 2 วินาที
  - **Track B (Vision):** 100 images × class
  - **Track C (Environment):** 200 samples × class
  - **Track D (Audio):** 50 samples × class, แต่ละ sample 1 วินาที

**ระหว่างทาง — สอน Bias Awareness:**
- ครูเดินเช็คว่าทีมเก็บข้อมูลครบทุก variation หรือเปล่า
- ถามนำ: "ถ้าใช้ในห้องอื่น/คนอื่นใช้ จะยังทำงานได้ไหม?"

**Submission:**
- Commit Worksheet W2 [`worksheets/W2-data-collection-log.md`](../worksheets/W2-data-collection-log.md)
- Link Edge Impulse project ใน README ของทีม

---

### ⏰ 12:00–13:00 | พักเที่ยง

ครู/TA review repo ของแต่ละทีมระหว่างทาน เห็นทีมไหนติด → mark ไว้

---

### ⏰ 13:00–14:00 | Train V1 + Deploy

**ผู้สอน:** วิทยากร + TA

**Step-by-Step:**
1. ใน Edge Impulse → **Create Impulse**
   - เลือก processing block ตาม sensor
   - เลือก learning block (Classification)
2. **Train**
   - ตั้ง model size = **nano (2.4M)** เพื่อให้ลง UNO Q ได้
   - Training processor = **GPU**
   - กด Save & Train
3. **อ่าน Confusion Matrix** (สอนรวมห้อง 10 นาที)
   - True Positive / False Positive
   - Accuracy ที่ดูได้ vs ที่ใช้ได้จริง
4. **Deploy**
   - Build → Arduino UNO Q (C++ Library หรือ via App Lab)
   - Test inference บนบอร์ดจริง

⚠️ ถ้า train ผิด memory → ลด model size หรือลด class count

---

### ⏰ 14:00–15:30 | 10-Case Testing + Iterate to V2 ★

**นี่คือช่วงเก็บคะแนน Data & Testing + Debug & Explain มากที่สุด**

**Part A — 10-Case Test (40 นาที):**
- ใช้ Worksheet W3 [`worksheets/W3-prediction-log.md`](../worksheets/W3-prediction-log.md)
- ทดสอบขั้นต่ำ **10 cases** แยก:
  - 5 cases ที่คาดว่าโมเดลจะทำได้
  - 5 cases ที่ท้าทาย (edge case)
- บันทึก: timestamp, input description, predicted class, confidence, actual class, ถูก/ผิด

**Part B — Iterate V2 (50 นาที):**
- วิเคราะห์ Prediction Log
- ระบุ pattern ที่ผิด → เก็บข้อมูลเพิ่ม / แก้ class
- Train V2
- ทดสอบ 10 cases เดิม + 5 cases ใหม่
- เปรียบเทียบ V1 vs V2 ใน `docs/v1-vs-v2.md`

**Commit ทุก 30 นาที** เพื่อมี history

---

### ⏰ 15:30–16:00 | Cross-Track Show & Tell

แต่ละทีม **2 นาที**:
- โจทย์คืออะไร
- Classes อะไรบ้าง
- Accuracy V1 → V2 เปลี่ยนเท่าไหร่
- 1 thing learned

ครูประเมิน Participation & Collaboration จากช่วงนี้

---

### ⏰ 16:00–16:30 | Wrap Up + Idea Canvas

- ครูสรุป Real World Cases 3 ตัวอย่าง:
  - **เกษตร:** ตรวจโรคพืชจากใบ (Vision)
  - **สุขภาพ:** Fall detector สำหรับผู้สูงอายุ (Motion)
  - **อุตสาหกรรม:** ตรวจเครื่องจักรเสียจากเสียง (Audio)
- แนะนำ LEAN / IDEA CANVAS
- ทุกทีมร่าง Idea Canvas สำหรับ Day 2 → commit Worksheet W4

---

### ⏰ 16:30–17:00 | Maker Space + Token Strategy

- พาทัวร์ Maker Space
- อธิบาย Token Management (5 คะแนน)
- แต่ละทีมร่างรายการอุปกรณ์ที่จะใช้ + token ที่จะเบิก

---

## ✅ End of Day 1 — Checklist สำหรับทุกทีม

- [ ] Repo ทีมมี commit อย่างน้อย 10 ครั้ง
- [ ] README ของทีม update ครบ (โจทย์, classes, ผลลัพธ์)
- [ ] Dataset link Edge Impulse ใส่ใน README
- [ ] `worksheets/W1-class-design.md` ✓
- [ ] `worksheets/W2-data-collection-log.md` ✓
- [ ] `worksheets/W3-prediction-log.md` ≥10 cases ✓
- [ ] `worksheets/W4-idea-canvas.md` ✓
- [ ] Compare `docs/v1-vs-v2.md` ✓
- [ ] Model V2 deploy ลง UNO Q ได้

---

## 🎯 Tips สำหรับครู

1. **อย่าตอบทันทีเวลานักเรียนถาม** — ใช้คำถามนำเสมอ ("ลองอะไรมาแล้ว?", "คิดว่าเพราะอะไร?")
2. **เดินดู Git commit** — บอกได้ว่าทีมไหน active ทีมไหนติด
3. **ดึง Hipster ขึ้นมาพูด** — มักเป็นบทบาทที่เงียบสุด แต่มีไอเดียดี
4. **เน้น Prediction Log มากกว่า Accuracy** — เพราะคะแนนวัดที่กระบวนการ
