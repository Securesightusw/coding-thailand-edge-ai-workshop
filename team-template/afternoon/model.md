<!-- workshop-header -->
<img width="1347" height="127" alt="Coding Thailand 2026 header" src="https://github.com/user-attachments/assets/ba5cf267-f460-4fb0-b69b-c461ae061a3b" />

# Afternoon — Model

- **Input ที่ใช้:** กล้อง webcam
- **Classes:** 2
- **จำนวนตัวอย่าง/class:** อย่างละ30
- **วิธีเชื่อมเข้า Edge Impulse:** [ /] กล้อง/ไมค์ (`edge-impulse-linux`)  [ ] Modulino (`data-forwarder`)

## V1
- Accuracy (ใน Studio): ____
- F1 score ราย class (class : F1): _______________
- class ที่ F1 ต่ำสุด: _______________
- รูป Confusion Matrix: ![cm-v1](../assets/cm-v1.png)
- อ่านแล้วเห็นอะไร (class ไหนสับสนกับ class ไหน): ระบบอ่านไม่ค่อยออกเนื่องจากมีพื้นหลังมากไป

## V2 (ถ้าทัน)
- แก้อะไรจาก V1: เพิ่มฐานข้อมูล
- Accuracy V2: ดีเทคเพิ่ม  | ดีขึ้น/แย่ลงตรงไหน: ดีขึ้นเปอร์เซนการแยกเพิ่มขึ้น

## รันบนบอร์ด
- [ /] วิธีรัน: [ /] กล้อง/ไมค์ → `edge-impulse-linux-runner` (Web UI :4912)  [ ] Modulino → Arduino library ในสเก็ตช์
- [/ ] ป้อน input จริงแล้ว prediction เปลี่ยนตาม (inferencing time: 0.05 ms)
- คลิป/รูปตอนรัน: ![run](../assets/run.jpg)

## (ต่อยอด) Output logic
- threshold ที่ใช้: confidence ≥ ____
- map class → output: _______________ (เช่น "เตือน" → Buzzer + Pixels แดง)
