# Writeup: Timed Transmission (Cyber Apocalypse 2023 - Hardware)

## 📋 Challenge Summary
- **Scenario:** ทีมกู้ภัยพบเสาอากาศที่กำลังส่งพิกัดของวัตถุโบราณ แต่สัญญาณถูกรบกวน เราต้องวิเคราะห์สัญญาณที่บันทึกไว้เพื่อหาความลับ
- **Category:** Hardware / SPI Analysis
- **Tools:** Saleae Logic / PulseView / Python

## 🔍 Analysis & Solution

จากการตรวจสอบไฟล์ที่ได้รับ (`transmission.sal`) พบว่าเป็นสัญญาณแบบ **SPI** ซึ่งประกอบด้วย 4 ช่องสัญญาณหลัก:
1. **MOSI (Master Out Slave In):** ข้อมูลที่ส่งออก
2. **MISO (Master In Slave Out):** ข้อมูลที่รับเข้า
3. **SCK (Serial Clock):** สัญญาณนาฬิกา
4. **CS (Chip Select):** เลือกอุปกรณ์

### 🛠️ Steps to Solve:
1. **Decode SPI:** ใช้ SPI Analyzer ใน Saleae หรือ PulseView โดยตั้งค่าให้ตรงกับสัญญาณ (CPOL=0, CPHA=0)
2. **Identify Data:** เมื่อถอดรหัสออกมา จะพบข้อมูลในรูปแบบ Hex หรือ ASCII ที่ถูกส่งผ่านช่อง MOSI/MISO
3. **Flag Detection:** มองหาข้อมูลที่เรียงตัวกันเป็นโครงสร้าง `HTB{...}` หรือข้อมูลที่ต้องนำมาแปลงจาก Hex อีกที

## 🏁 Flag
**HTB{71m3d_724n5m15510n_3xp053d}**

---
### 📚 References
- Based on research from [D13David's CTF Writeups](https://github.com/D13David/ctf-writeups)
