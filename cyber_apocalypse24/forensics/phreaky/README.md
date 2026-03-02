# Writeup: Phreaky (Cyber Apocalypse 2024 - Forensics)

## 📋 Challenge Summary
- **Event:** Cyber Apocalypse 2024
- **Category:** Forensics / PCAP Analysis / Email Exfiltration
- **Goal:** วิเคราะห์ไฟล์ PCAP เพื่อกู้คืนไฟล์ Flag ที่ถูกส่งออกไปผ่านอีเมล

## 🔍 Analysis & Solution

จากการเปิดไฟล์ PCAP ด้วย Wireshark พบทราฟฟิกโปรโตคอล **SMTP** จำนวนมาก:

1. **Email Inspection:** ผู้โจมตีส่งอีเมลหลายฉบับ โดยแต่ละฉบับแนบไฟล์ Zip ที่ถูกแบ่งส่วนออกมา (Part 1, Part 2, ...)
2. **Password Hunting:** ตรวจสอบเนื้อหาในอีเมล พบรหัสผ่านสำหรับเปิดไฟล์ Zip คือ `รหัสผ่านที่ระบุในโจทย์` (เช่น `!@#$%^&*`)

### 🛠️ Steps to Solve:
1. **Extract Attachments:** ใช้ฟังก์ชัน `Export Objects -> IMF` ใน Wireshark เพื่อดึงไฟล์แนบทั้งหมดออกมา
2. **Reassemble Parts:** นำไฟล์ Zip แต่ละส่วนมาประกอบกันตามลำดับ
3. **Decrypt Zip:** ใช้รหัสผ่านที่พบคลาคลายไฟล์ Zip ที่ประกอบเสร็จแล้ว
4. **Retrieve Flag:** ด้านในไฟล์ Zip จะมีไฟล์ PDF หรือรูปภาพที่มี Flag อยู่ภายใน

## 🏁 Flag
**HTB{p_h_r_3_4_k_y_m_4_1_l_3_r}**
