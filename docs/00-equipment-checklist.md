# 📦 Equipment Checklist (สำหรับครู/ผู้จัด)

## อุปกรณ์ที่แต่ละทีมต้องได้

### Hardware (1 ชุด/ทีม)

- [ ] Arduino UNO Q (2GB หรือ 4GB)
- [ ] USB-C cable + Power adapter (5V/3A)
- [ ] Modulino kit ครบ:
  - [ ] Modulino Movement (IMU 6-axis)
  - [ ] Modulino Distance (ToF)
  - [ ] Modulino Thermo (Temp + Humidity)
  - [ ] Modulino Light (Brightness + Color)
  - [ ] Modulino Buttons (3 buttons + LED)
  - [ ] Modulino Knob
  - [ ] Modulino Buzzer
  - [ ] Modulino Pixels (8x RGB LED)
- [ ] Qwiic cables (อย่างน้อย 4 เส้น)
- [ ] Modulino Base (โครงประกอบ)

### เสริมสำหรับ Track B (Vision) และ Track D (Audio)

- [ ] USB Webcam (Logitech HD Pro หรือเทียบเท่า) — Track B
- [ ] USB Microphone — Track D
- [ ] USB Hub (powered) — เพราะ UNO Q ต้องเสียบหลายอย่าง

## อุปกรณ์กลาง (ใช้ร่วม)

- [ ] Projector + HDMI
- [ ] Wi-Fi เร็วพอสำหรับ 20 ทีม upload data ไป Edge Impulse Studio พร้อมกัน
- [ ] Power strip (UNO Q + Laptop กินไฟพอควร)
- [ ] กล้อง DSLR/Smartphone — ถ่ายภาพกิจกรรมสำหรับ Wrap Up

## บัญชี/Software (เตรียมล่วงหน้า)

- [ ] บัญชี **GitHub** ของแต่ละทีม (สร้างก่อนถึงวัน workshop)
- [ ] บัญชี **Edge Impulse** ของแต่ละทีม (Free tier พอ)
- [ ] **Arduino App Lab** ติดตั้งบน laptop ของทีม
- [ ] **VS Code** (ทางเลือก) + Git extension

## Pre-Flight Test (1 วันก่อน)

ครู/TA ทุกคนต้องทดสอบ:
- [ ] Boot UNO Q ได้ครั้งแรก
- [ ] เชื่อม Wi-Fi ได้
- [ ] Login Edge Impulse + สร้าง project test ได้
- [ ] Train+Deploy demo model (Gesture Wand) เสร็จใน 30 นาที
- [ ] Push code ไป GitHub ได้

## TA/Mentor Ratio

- **1 TA : 3-5 ทีม** สำหรับ Day 1 (เพราะ UNO Q ยังใหม่ ปัญหาเฉพาะหน้าเยอะ)
- TA ทุกคนควรผ่าน Pre-Flight Test มาก่อน

## Backup Plan

- [ ] Backup dataset ของ Track A (Gesture) อยู่ใน `labs/track-a-motion/backup-dataset/`
- [ ] UNO Q สำรอง 2 ตัว (กันเสีย)
- [ ] Modulino สำรอง 1 ชุด
- [ ] Mobile hotspot สำรอง กันเน็ตห้องล่ม
