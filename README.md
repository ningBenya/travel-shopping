# รายการฝากซื้อ Nat

หน้ารายการของฝากซื้อจากญี่ปุ่น ติ๊ก "ซื้อแล้ว" กรอกราคาที่จ่ายจริง (เยน) แล้วแปลงเป็นบาทพร้อมยอดรวม
ถ้าตั้งค่า Firebase ไว้ ทุกคนที่เปิดลิงก์จะเห็นข้อมูลเดียวกันแบบเรียลไทม์

## ไฟล์
- `index.html` หน้าเว็บ (รายการสินค้าอยู่ที่ `const items = [ ... ]`)
- `images/` รูปสินค้า
- `firebase-config.js` ค่าตั้งค่า Firebase
- `database.rules.json` กฎของฐานข้อมูล (คัดลอกไปวางใน Firebase Console)

## ตั้งค่า Firebase (ทำครั้งเดียว)
1. ไปที่ https://console.firebase.google.com → Add project
2. เมนู Build → Realtime Database → Create Database → เลือก Singapore (asia-southeast1) → Start in locked mode
3. แท็บ Rules → วางเนื้อหาจาก `database.rules.json` → Publish
4. Project settings (รูปเฟือง) → Your apps → กดไอคอน `</>` เพิ่ม Web app → คัดลอก firebaseConfig มาวางใน `firebase-config.js`
5. commit + push แล้วเปิดหน้าเว็บ จะเห็นจุดเขียว "ซิงก์อยู่"

## หมายเหตุ
ใครก็ตามที่มีลิงก์จะแก้สถานะ "ซื้อแล้ว" และราคาได้ ส่งลิงก์ให้เฉพาะคนที่เกี่ยวข้อง
