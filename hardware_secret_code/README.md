# Writeup: Secret Code (Cyber Apocalypse 2023 - Hardware)

## 📋 Challenge Summary
- **Platform:** Hack The Box (Cyber Apocalypse 2023)
- **Scenario:** ตรวจสอบพิกัดของวัตถุโบราณที่ถูกส่งผ่านอุปกรณ์สื่อสาร แต่พิกัดถูกเข้ารหัสไว้ด้วยรหัสลับ (Secret Code)
- **Category:** Hardware / I2C Analysis
- **Tools:** Saleae Logic / PulseView

## 🔍 Analysis & Solution

จากการวิเคราะห์ไฟล์บันทึกสัญญาณ (`secret_code.sal`) พบว่าเป็นโปรโตคอล **I2C**:
1. **SDA (Serial Data):** ข้อมูลที่ส่งผ่านบัส
2. **SCL (Serial Clock):** สัญญาณนาฬิกาควบคุมจังหวะ

### 🛠️ Steps to Solve:
1. **Decode I2C:** ใช้ I2C Analyzer ในโปรแกรมถอดรหัส โดยระบุขา SDA และ SCL ให้ถูกต้อง
2. **Read Data:** ข้อมูลถูกส่งไปยังอุปกรณ์ปลายทางในรูปแบบ Hex
3. **Hex to ASCII:** นำข้อมูล Hex ที่ดึงออกมาจาก Analyzer มาทำการแปลงเป็นตัวอักษร ASCII
4. **Flag Formation:** รวบรวมตัวอักษรที่ได้มาประกอบกันเป็น Flag

## 🏁 Flag
**HTB{12C_53c237_c0d3_un10ck3d}**
