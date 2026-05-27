# 🔌 Connect Edge Impulse to UNO Q

> สำหรับช่วง 09:30-10:00 — ครู/TA ใช้สอน setup

---

## Overview

UNO Q เป็นบอร์ดสองสมอง — เราจะใช้ **Linux side** เป็น Edge Impulse device

---

## Step 1: Boot UNO Q

1. เสียบ USB-C เข้า UNO Q + power adapter (5V/3A)
2. รอ ~30 วินาทีให้ Linux boot
3. ดู LED indicator → ติดต่อเนื่อง = พร้อมใช้

---

## Step 2: เชื่อม Wi-Fi

### Method A: ผ่าน Arduino App Lab (ง่ายสุด)

1. เปิด Arduino App Lab บน laptop
2. UNO Q จะปรากฏใน device list
3. คลิก device → Setup → Wi-Fi
4. เลือก network → ใส่ password

### Method B: ผ่าน ADB

```bash
# บน laptop
adb devices
adb shell

# ใน UNO Q shell
sudo nmcli device wifi connect "SSID" password "PASSWORD"
```

---

## Step 3: SSH เข้า UNO Q

```bash
# หา IP ของ UNO Q
adb shell ip addr show wlan0 | grep inet

# SSH (default: arduino / arduino)
ssh arduino@<IP>
```

> ⚠️ ถ้า password ผิด → reset ผ่าน `adb shell sudo passwd arduino`

---

## Step 4: ติดตั้ง Edge Impulse CLI

ใน UNO Q terminal:

```bash
sudo apt update

# Node.js 20
curl -sL https://deb.nodesource.com/setup_20.x | sudo bash -

# Dependencies
sudo apt install -y gcc g++ make build-essential nodejs sox \
  gstreamer1.0-tools gstreamer1.0-plugins-good \
  gstreamer1.0-plugins-base gstreamer1.0-plugins-base-apps

# Edge Impulse Linux client
sudo npm install edge-impulse-linux -g --unsafe-perm
```

⏱️ ใช้เวลา ~5-10 นาที (ขึ้นกับ network)

---

## Step 5: Connect Camera/Mic (ถ้าใช้)

ก่อนรัน Edge Impulse ต้องเสียบ peripherals ผ่าน USB Hub:

```bash
# เช็ค camera
ls /dev/video*

# เช็ค audio
arecord -l
```

---

## Step 6: Login + เลือก Project

```bash
edge-impulse-linux
```

จะเปิด wizard:
1. Email + password (จาก Edge Impulse account)
2. เลือก project ของทีม
3. ตั้งชื่อ device (เช่น `team-XX-unoq`)

✅ จะเห็นข้อความ "Your device is now connected to Edge Impulse"

---

## Step 7: ทดสอบ Data Acquisition

ใน Edge Impulse Studio:
1. Devices tab → จะเห็น UNO Q connected
2. Data acquisition → Start sampling
3. เลือก sensor / camera / microphone
4. กด Start → เห็น data flow มาจาก UNO Q ✓

---

## ⚠️ Troubleshooting

### "edge-impulse-linux command not found"

```bash
# เช็ค path
which edge-impulse-linux

# ถ้าไม่เจอ install ใหม่
sudo npm install edge-impulse-linux -g --unsafe-perm
```

### "Camera not detected"

```bash
# เช็ค USB
lsusb

# เช็ค driver
dmesg | tail -20

# ลอง re-plug + reboot
```

### "Permission denied" ตอน access camera/mic

```bash
sudo usermod -aG video,audio arduino
# logout แล้ว login ใหม่
```

### "32-bit OS error"

```
"You are attempting to deploy an .eim Edge Impulse model file
to a 32-bit operating system running on a 64-bit CPU."
```

→ ใช้ deployment target = **Arduino UNO Q** (ไม่ใช่ "Linux") ใน Studio

### Connection drop บ่อย

- เช็ค Wi-Fi signal
- เปลี่ยน Wi-Fi channel (5GHz ดีกว่า 2.4GHz)
- ลอง LAN cable แทน Wi-Fi

---

## ⏱️ Time Budget

ใน workshop ใช้ช่วง 09:30-10:00:
- 5 นาที: Boot + connect Wi-Fi
- 5 นาที: SSH access
- 10 นาที: Install dependencies (รอ apt)
- 5 นาที: Login Edge Impulse
- 5 นาที: Test data acquisition

ถ้าทีมไหนใช้เกิน 30 นาที → ให้ TA ช่วย / ใช้ pre-flashed UNO Q สำรอง

---

## 📚 Reference

- [Arduino UNO Q docs](https://docs.edgeimpulse.com/hardware/boards/arduino-uno-q)
- [Edge Impulse Linux SDK](https://docs.edgeimpulse.com/docs/edge-ai-targets/edge-impulse-for-linux)
