# 🚀 GitHub Setup Guide สำหรับผู้จัด Workshop

> วิธีนำ repo นี้ขึ้น GitHub และเตรียมให้ทีมนักเรียน fork

---

## Step 1: สร้าง Repo บน GitHub

### Option A: สร้างใหม่จาก scratch

1. ไป https://github.com/new
2. **Repository name:** `coding-thailand-edge-ai-workshop`
3. **Description:** "Day 1 materials — Coding Thailand 2026 Edge AI Workshop"
4. **Public** ✓
5. **Initialize:** ☐ ไม่ต้องติ๊ก (เราจะ push เอง)
6. กด **Create repository**

### Option B: Fork จาก template (ถ้ามีต้นแบบ)

ถ้าคุณได้รับ URL repo template → กด Fork ที่มุมขวาบน

---

## Step 2: Push Repo จากเครื่องคุณ

```bash
# เข้า folder
cd coding-thailand-edge-ai-workshop

# Init git
git init
git add .
git commit -m "init: Edge AI Workshop Day 1 materials"

# เชื่อม remote
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/coding-thailand-edge-ai-workshop.git

# Push
git push -u origin main
```

---

## Step 3: ตั้งเป็น Template Repository

ให้ทีมนักเรียน **"Use this template"** ได้ง่ายๆ:

1. ใน GitHub → repo ของคุณ → **Settings**
2. หน้า General → ติ๊ก ☑ **Template repository**
3. Save

ทำให้นักเรียนกดปุ่ม **"Use this template"** เห็นได้ทันที (ดีกว่า fork สำหรับ workshop)

---

## Step 4: ตั้ง Branch Protection (Optional)

ป้องกัน main branch ถูกแก้ตรงๆ:

1. Settings → Branches → Add rule
2. Branch name: `main`
3. ☑ Require pull request before merging
4. ☑ Require approvals: 1
5. Save

> ⚠️ สำหรับ workshop ไม่บังคับ — แต่ดีถ้าอยากสอน PR workflow เต็มรูปแบบ

---

## Step 5: เปิด GitHub Discussions (แนะนำ)

ให้นักเรียนถาม-ตอบกันได้:

1. Settings → General → Features
2. ☑ Discussions
3. Save

---

## Step 6: เตรียม URL ให้ทีม

ก่อนวัน workshop ส่งให้นักเรียนรู้ล่วงหน้า:

```
🔗 Workshop Repo:
https://github.com/YOUR_USERNAME/coding-thailand-edge-ai-workshop

📋 Team Repo Template:
ใน workshop ทีมจะ Use this template เพื่อสร้าง repo ของตัวเอง
ตั้งชื่อตามรูปแบบ: edge-ai-team-XX (เช่น edge-ai-team-01)
```

---

## Step 7: Sample Team Repo (Optional แต่แนะนำ)

สร้าง demo team repo เป็นตัวอย่าง:

```bash
# ใช้ template
gh repo create demo-team --template YOUR_USERNAME/coding-thailand-edge-ai-workshop \
  --public --clone

# หรือผ่าน UI:
# กด "Use this template" → ตั้งชื่อ demo-team
```

แล้วทำ:
- Commit ตัวอย่าง 3-5 ครั้ง (แสดง commit message format ที่ดี)
- กรอก Worksheet W1-W4 ตัวอย่าง
- ใส่ผลลัพธ์สมมุติ V1 vs V2

→ นักเรียนเห็นเป็น reference ได้ทันที

---

## Step 8: Pre-Workshop Checklist

ก่อนถึงวัน Workshop:

- [ ] Repo ขึ้น GitHub แล้ว
- [ ] ตั้งเป็น Template ☑
- [ ] Discussions เปิด ☑
- [ ] URL ส่งให้ทีมแล้ว
- [ ] Demo team repo มีตัวอย่าง
- [ ] ทุก TA fork repo + clone ลงเครื่อง
- [ ] ทดสอบ flow: ทีม template → ทีมสร้าง repo ใหม่ → push commit แรกได้

---

## ⚙️ Optional: GitHub Classroom

ถ้าคุณสะดวกใช้ GitHub Classroom (เหมาะกับ workshop ใหญ่ >20 ทีม):

1. ไป https://classroom.github.com
2. Create organization → Create classroom
3. Create assignment → ใช้ repo template
4. ได้ลิงก์ assignment สำหรับนักเรียน
5. นักเรียนกดลิงก์ → ระบบสร้าง repo ของแต่ละทีมอัตโนมัติ

**ข้อดี:** จัดการได้ดี + เห็น progress ของทุกทีมในที่เดียว
**ข้อเสีย:** ต้องตั้ง org ก่อน + นักเรียนต้องอยู่ใน account ที่ join classroom

---

## 📋 Workshop Day Flow (GitHub-focused)

### 09:30-09:45 — Setup ทีม
```
ครูพูด: "ทุกทีมไปที่ URL workshop repo"
ครูพูด: "กดปุ่ม 'Use this template' มุมขวาบน"
ครูพูด: "ตั้งชื่อ edge-ai-team-XX, public, กด Create"
ครูพูด: "Clone ลง laptop ตามคำสั่งใน docs/04-git-basics.md"
```

### ตลอดวัน — Cadence ของ Commit

แนะนำให้ครูตั้ง "Commit Time" ทุก ~30 นาที:
- 11:00 — Commit Worksheet W1
- 11:30 — Commit Data Collection log
- 13:30 — Commit V1 results
- 14:30 — Commit Prediction Log
- 15:30 — Commit V2 + comparison

### 16:30 — Final push
ทุกทีมต้อง final push ก่อนเลิก พร้อม tag `day1-final`:
```bash
git tag day1-final
git push origin day1-final
```

---

## 🎯 Tips จาก Workshop ก่อนๆ

1. **Username convention:** บอกนักเรียนตั้งชื่อ team-repo ให้ match กับ team number เพื่อง่ายต่อการ grade
2. **TA Watch List:** ให้ TA แต่ละคน Watch repo ของทีมที่ดูแล จะได้รู้เมื่อมี commit ใหม่
3. **Grading Day:** ใช้ `git log` + `gh pr list` + เปิด repo ดู → ใช้ Rubric ที่อยู่ใน `docs/03-rubric.md`
4. **Public vs Private:** Public ดีกว่า เพราะทีมเห็นของกันและกัน → เป็นแรงผลักดัน

---

## 🆘 ปัญหาที่อาจเจอ

### นักเรียนไม่มี GitHub account
→ เตรียม instruction sign up ล่วงหน้า + เผื่อ 15 นาทีใน schedule

### Push ไม่ขึ้น (HTTPS)
→ GitHub ตอนนี้ต้องใช้ Personal Access Token แทน password
→ แนะนำให้ใช้ GitHub CLI: `gh auth login`

### นักเรียนเผลอ commit dataset ใหญ่
→ มี .gitignore ใน template แล้ว แต่ย้ำตอน Git 101

### ทีม merge conflict
→ มีใน troubleshooting guide แล้ว

---

## 📚 References

- [GitHub Docs - Template Repos](https://docs.github.com/en/repositories/creating-and-managing-repositories/creating-a-template-repository)
- [GitHub Classroom](https://classroom.github.com)
- [GitHub CLI](https://cli.github.com/)
