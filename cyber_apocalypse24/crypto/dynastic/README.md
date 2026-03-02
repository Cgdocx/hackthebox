# Writeup: Dynastic (Cyber Apocalypse 2024 - Crypto)

## 📋 Challenge Summary
- **Event:** Cyber Apocalypse 2024
- **Category:** Crypto / Vigenere & Caesar Variant
- **Goal:** ถอดรหัสข้อความที่ถูกเข้ารหัสด้วยการเลื่อนตำแหน่งตัวอักษรแบบไดนามิก (Dynamic Shift)

## 🔍 Analysis & Solution

โจทย์ใช้วิธีการคล้าย Caesar Cipher แต่ค่าการเลื่อน (Shift) จะเปลี่ยนไปตามตำแหน่งของตัวอักษร (Index):

1. **Encryption Logic:** `ciphertext[i] = (plaintext[i] + i) % 26`
2. **Analysis:** ค่าที่นำมาบวกคือ Index ของตัวอักษรนั้นๆ ในสตริง

### 🛠️ Steps to Solve:
1. **Reverse Math:** เปลี่ยนจากการบวกเป็นลบ `plaintext[i] = (ciphertext[i] - i) % 26`
2. **Implementation:** เขียนสคริปต์ Python เพื่อวนลูปถอดรหัสข้อความทีละตัวอักษรโดยใช้ Index เป็นตัวกำหนดค่าการเลื่อนกลับ
3. **Decryption:** นำข้อความจาก `output.txt` มาผ่านสคริปต์ที่เขียนขึ้น

## 🏁 Flag
**HTB{d_y_n_4_5_t_y_c_i_p_h_3_r}**
