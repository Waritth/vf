# แผนผังโครงการ สทบ. ปี 2569-2570

Interactive Dashboard สำหรับนำเสนอแผนผังโครงการภาพรวมของสำนักงานกองทุนหมู่บ้านและชุมชนเมืองแห่งชาติ (สทบ.) ปี 2569-2570

## ภาพรวม

- **งบประมาณรวม:** 350.11 ล้านบาท
- **จำนวนโครงการ:** 8 โครงการ
- **แบ่งเป็น 2 Session:**
  - Session 1 · มีเงินแล้ว (253.11M · 5 โครงการ)
  - Session 2 · รองบ 70 ล้าน (งบใหม่ · 3 โครงการ)

## Deploy เป็น GitHub Pages

### วิธีที่ 1: ผ่าน GitHub Web UI (ง่ายที่สุด — ไม่ต้องใช้ command line)

1. เข้า https://github.com/new
2. สร้าง repo ใหม่ (เช่น ชื่อ `vf-april-dashboard` หรือ `sor-tor-bor-plan-2569`)
3. เลือก **Public** (GitHub Pages ฟรีเฉพาะ public repo)
4. กด **Create repository**
5. ในหน้า repo ที่เพิ่งสร้าง กด **uploading an existing file**
6. ลากไฟล์ทั้ง 3 ไฟล์ในโฟลเดอร์นี้เข้าไป: `index.html`, `.nojekyll`, `README.md`
7. กด **Commit changes**
8. ไปที่ **Settings → Pages** (เมนูด้านซ้าย)
9. ใต้ **Source** เลือก `Deploy from a branch`, เลือก branch `main` และ folder `/ (root)` → **Save**
10. รอประมาณ 1-2 นาที → เว็บจะ live ที่ `https://<github-username>.github.io/<repo-name>/`

### วิธีที่ 2: ผ่าน Command Line (เร็วกว่าถ้าใช้ git เป็นประจำ)

```bash
cd "github-pages-deploy"
git init
git add .
git commit -m "Initial deploy: แผนผังโครงการ สทบ. 2569-2570"
git branch -M main
git remote add origin https://github.com/<your-username>/<repo-name>.git
git push -u origin main
```

จากนั้นไปที่ **Settings → Pages** ตามขั้นตอนที่ 8-10 ข้างบน

## URL ที่จะได้

```
https://<github-username>.github.io/<repo-name>/
```

ตัวอย่าง: หาก username = `ply-warit` และ repo = `vf-april-dashboard` จะได้ `https://ply-warit.github.io/vf-april-dashboard/`

## ไฟล์ในโฟลเดอร์นี้

- `index.html` — Interactive Dashboard (ต้องชื่อ index.html เพื่อให้ GitHub Pages แสดงเป็นหน้าแรกอัตโนมัติ)
- `.nojekyll` — บอก GitHub ไม่ต้องประมวลผลด้วย Jekyll (ไฟล์ว่าง แต่สำคัญ)
- `README.md` — ไฟล์นี้เอง

## ฟีเจอร์ของเว็บ

- 🔍 **ค้นหา + กรอง** — ช่องค้นหาและปุ่มกรองตาม Session / สถานะ
- 📊 **Stats Bar** — สรุปงบประมาณรวม · จำนวนโครงการ · ผลผลิตรวม
- 🗂️ **8 การ์ดโครงการ** — คลิกเพื่อดูรายละเอียดเพิ่มเติมใน Modal
- ⌨️ **Keyboard shortcuts** — `Esc` ปิด modal · `← →` เลื่อนโครงการ
- 📱 **Responsive** — รองรับมือถือ แท็บเล็ต เดสก์ท็อป
- 🖨️ **Print-friendly** — พิมพ์ได้สวยจากเบราว์เซอร์

## License

เอกสารภายในของ สทบ. สำหรับใช้นำเสนอเท่านั้น
