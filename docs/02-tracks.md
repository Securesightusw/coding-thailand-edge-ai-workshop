# 🎯 4 Tracks ให้ทีมเลือก

> **Theme กลาง:** *"AI for Daily Life — สอน AI ให้มอง/ฟัง/รู้สึก สิ่งรอบตัวคุณ"*

แต่ละทีมเลือก **1 Track** + เลือกระดับความท้าทาย (Basic / Intermediate / Advanced)

---

## 🎬 Anchor Demo (วิทยากรสาธิต)

### 🪄 Gesture Wand — Motion Classification

- **โจทย์:** จำแนกท่าทางการเคลื่อนไหวมือ
- **Sensor:** Modulino Movement
- **Classes:** วงกลม / Z-shape / สั่น / นิ่ง

นี่คือตัวอย่างที่วิทยากรจะสาธิตเปิด workshop ทีมสามารถลอกแล้วต่อยอดได้

---

## 🥇 Track A — Motion Classification

### "Smart Motion Sensor"

| ระดับ | โจทย์ตัวอย่าง | Classes |
|---|---|---|
| 🟢 **Basic** | Tilt Detector | นิ่ง / เอียงซ้าย / เอียงขวา |
| 🟡 **Intermediate** | Activity Tracker | ยืน / เดิน / วิ่ง / นั่ง |
| 🔴 **Advanced** | Fall Detector | ยืน / เดิน / นั่ง / **ล้ม** |

**Sensor หลัก:** Modulino Movement (IMU 6-axis)
**Output:** Modulino Pixels (สีตามคลาส) + Buzzer (alert)

**จุดเด่น:**
- ✅ เก็บข้อมูลเร็ว (10 วินาที/sample)
- ✅ Train เร็ว เห็นผลทันที
- ✅ ไม่ต้องใช้ Webcam
- ✅ เหมาะกับทีมมือใหม่

**โจทย์ Real World ต่อยอด Day 2:**
- Fall detector สำหรับผู้สูงอายุ
- Fitness rep counter
- Vibration anomaly detection สำหรับเครื่องจักร

---

## 🥈 Track B — Vision Classification

### "Smart Camera"

| ระดับ | โจทย์ตัวอย่าง | Classes |
|---|---|---|
| 🟢 **Basic** | Object Sort | ขวด / กระป๋อง / กระดาษ |
| 🟡 **Intermediate** | Mask Detector | ใส่หน้ากากถูก / ไม่ถูก / ไม่ใส่ |
| 🔴 **Advanced** | Fruit Ripeness | ดิบ / สุกพอดี / สุกเกิน |

**Sensor หลัก:** USB Webcam (Linux side)
**Output:** Modulino Pixels + LED Matrix + Buzzer

**จุดเด่น:**
- ✅ เห็นผลชัดเจน นักเรียนตื่นเต้น
- ✅ Real-world applications เยอะ
- ✅ เชื่อม Computer Vision concepts

**ข้อควรระวัง:**
- ⚠️ ต้อง USB Hub (camera + power)
- ⚠️ Train นานกว่า Track อื่น
- ⚠️ ต้องตั้ง model size = **nano**
- ⚠️ ระวัง bias จาก background, แสง

**โจทย์ Real World ต่อยอด Day 2:**
- Smart Recycle Bin (เปิดฝาตามประเภทขยะ)
- ตรวจโรคพืชจากใบ
- Quality control ในโรงงาน

---

## 🥉 Track C — Multi-Sensor Anomaly Detection

### "Smart Environment"

| ระดับ | โจทย์ตัวอย่าง | Classes |
|---|---|---|
| 🟢 **Basic** | Day/Night Detector | กลางวัน / กลางคืน / เปิดไฟ |
| 🟡 **Intermediate** | Fridge Door Alert | ปิด / เปิดสั้น / เปิดทิ้ง |
| 🔴 **Advanced** | Smart Zone | ห้องว่าง / มีคน / มีคนเยอะ |

**Sensor หลัก:** Combo — Modulino Thermo + Light + Distance
**Output:** Modulino Pixels + Buzzer

**จุดเด่น:**
- ✅ สอน **multi-sensor fusion** ได้
- ✅ ใช้ Modulino ล้วน ไม่ต้องเพิ่มอุปกรณ์
- ✅ Data dense → train เร็ว

**ข้อควรระวัง:**
- ⚠️ Class boundary อาจไม่ชัด → ต้องออกแบบ classes ดีๆ
- ⚠️ ต้องเก็บข้อมูลในหลายสภาพแวดล้อม

**โจทย์ Real World ต่อยอด Day 2:**
- Smart classroom monitor
- ตู้เย็นในร้านสะดวกซื้อ (alarm ถ้าเปิดทิ้ง)
- Smart parking (มีรถจอด/ว่าง)

---

## 🏅 Track D — Audio Classification

### "Smart Listener"

| ระดับ | โจทย์ตัวอย่าง | Classes |
|---|---|---|
| 🟢 **Basic** | Sound Type | ปรบมือ / ดีดนิ้ว / เงียบ |
| 🟡 **Intermediate** | Cough Detector | ไอ / จาม / พูด / เงียบ |
| 🔴 **Advanced** | Keyword Spotting | "Hey Arduino" / "Stop" / "Help" / noise |

**Sensor หลัก:** USB Microphone (Linux side)
**Output:** Modulino Pixels + Buzzer + LED Matrix

**จุดเด่น:**
- ✅ Audio Edge AI กำลังเป็นที่นิยม
- ✅ Real-world cases เยอะ
- ✅ Edge Impulse มี keyword spotting template ให้

**ข้อควรระวัง:**
- ⚠️ ต้อง USB mic (เช็คก่อนว่ามีพอ)
- ⚠️ ระวัง noise ในห้อง workshop
- ⚠️ ต้อง record ใน environment ที่ใกล้กับ deployment

**โจทย์ Real World ต่อยอด Day 2:**
- ระบบตรวจอาการป่วยจากเสียงไอ
- Smart speaker / voice command
- ตรวจเครื่องจักรผิดปกติจากเสียง

---

## 🤔 จะเลือก Track ไหนดี?

ใช้ flowchart นี้:

```
มีคน Vision/ML มาก่อนไหม?
├─ ไม่มี → Track A (Motion) ★ แนะนำ
└─ มี → ทีมอยากทำอะไร?
        ├─ สิ่งที่เห็นได้ → Track B (Vision)
        ├─ Multi-sensor → Track C (Environment)
        └─ Audio       → Track D (Audio)

แล้วระดับล่ะ?
├─ ไม่เคยทำ ML → Basic
├─ พอเข้าใจ概念 → Intermediate
└─ เคย train โมเดลแล้ว → Advanced
```

## 🎯 ทุก Track มีคะแนนเต็มเท่ากัน

**ไม่มี Track ไหนยากกว่าหรือได้คะแนนน้อยกว่า** — Rubric เดียวกัน ประเมินที่กระบวนการ ไม่ใช่ความซับซ้อนของโจทย์

- เลือก Basic ทำให้ดี → 30/30
- เลือก Advanced ทำไม่จบ → ได้น้อยกว่า Basic ที่จบ

**คำแนะนำ:** เลือก scope ที่ทำเสร็จใน 90 นาทีแรกได้ แล้วเหลือเวลาไป iterate V2
