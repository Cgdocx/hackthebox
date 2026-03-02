# Writeup: Makeshift (Cyber Apocalypse 2024 - Crypto)

## 📋 Challenge Summary
- **Event:** Cyber Apocalypse 2024
- **Category:** Crypto / Simple Substitution
- **Goal:** ย้อนกลับกระบวนการสลับตำแหน่งตัวอักษรเพื่อถอดรหัส Flag

## 🔍 Analysis & Solution

โจทย์ให้สคริปต์ Python ที่ใช้ในการเข้ารหัส Flag โดยมีอัลกอริทึมดังนี้:
1. วนลูปอ่านตัวอักษรทีละ 3 ตัว
2. สลับตำแหน่งตัวอักษรในแต่ละกลุ่มตามลำดับที่กำหนด (เช่น `abc` -> `bca`)

### 🛠️ Steps to Solve:
1. **Understand Logic:** สคริปต์สลับตำแหน่งตัวอักษรในทุกๆ 3 ตัว
2. **Reverse Process:** เขียนสคริปต์ย้อนกลับเพื่อสลับตำแหน่งกลับคืนที่เดิม
3. **Execution:** รันสคริปต์กับข้อความที่ถูกเข้ารหัสไว้ในไฟล์ `output.txt`

## 🏁 Flag
**HTB{n3w_7h1n65_4r3_m4d3_7h15_w4y}**
