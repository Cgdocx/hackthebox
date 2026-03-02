# Global CTF Writeups Archive (2023-2025)

## 📋 Overview
รวบรวมสรุปเทคนิคและแนวทางการแก้โจทย์จากรายการแข่งขัน CTF ระดับนานาชาติหลากหลายรายการ โดยเรียบเรียงใหม่เน้นความเข้าใจในระดับภาพรวม

### 1. Web Exploitation Trends
- พบการใช้ **SSTI** ในภาษาที่หลากหลายมากขึ้น (Python Jinja2, Java Velocity, Ruby ERB)
- การโจมตีระบบ **JWT** โดยใช้ช่องโหว่ใน Library รุ่นเก่า
- เทคนิคการข้ามผ่าน Proxy (HAProxy, Nginx) เพื่อเข้าถึง Endpoint ภายใน

### 2. Pwn & Binary Analysis
- เน้นการทำ **Ret2Libc** และการจัดการหน่วยความจำบนระบบ 64-bit
- โจทย์แนว **Heap Exploitation** (Tcache poisoning, Chunk overlapping) พบมากขึ้นในรายการระดับสูง
- การวิเคราะห์ช่องโหว่ในระดับ **Kernel** และระบบจำลอง (VM Jailbreak)

### 3. Forensics & Incident Response
- การวิเคราะห์ทราฟฟิกเครือข่ายที่ซับซ้อน (HTTPS Decryption, USB PCAP)
- การทำ **Memory Analysis** ด้วย Volatility 3
- กู้คืนข้อมูลจากระบบไฟล์ที่ถูกลบหรือถูกทำลาย (Ext4, NTFS recovery)

### 4. Cryptography
- การโจมตีจุดอ่อนของ **RSA** (Common Factor, Small exponent)
- การวิเคราะห์ **AES-CBC** (Padding Oracle Attack)
- โจทย์แนว **Elliptic Curve Cryptography (ECC)** ที่เริ่มแพร่หลายมากขึ้น

### 5. Hardware & Misc
- การถอดรหัสสัญญาณดิจิทัล (UART, SPI, I2C) ผ่านไฟล์ .sal
- การวิเคราะห์ลายวงจรบน PCB จากไฟล์ Gerber
- โจทย์แนว Python Sandbox และการทำ Jailbreak ในสภาพแวดล้อมที่จำกัด

---
*บันทึกนี้เป็นการสรุปความรู้ที่ได้จากการวิเคราะห์ฐานข้อมูล Writeup ของ D13David และ CTF Community*
