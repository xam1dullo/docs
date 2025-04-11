# **Terminal & Git Bash Cheat Sheet (Boshlang'ichlar uchun)**  
**🖥️ Terminal - Dasturchining "Super Kuchlari"!**

---

## **1. Asosiy Terminal Komandalari**

### **Papkalar bilan Ishlash**
```bash
pwd              # 📂 Hozir turgan papkangizni ko'rsatadi (Masalan: /c/projects)
cd my-project    # 📂 "my-project" papkasiga kirish
cd ..           # 📂 Bir papka ortga qaytish (masalan: /c/projects dan /c ga)
ls               # 📜 Papkadagi fayl va papkalar ro'yxati
ls -a           # 📜 Yashirin fayllarni ham ko'rsatish (.git kabi)
```

**Misol**:  
```bash
cd Desktop    # Desktop papkasiga o'tish
ls            # Desktopdagi fayllarni ko'rish
```

---

### **Fayl & Papka Yaratish/O'chirish**
```bash
touch index.html    # 🆕 Yangi fayl yaratish (index.html)
mkdir my-folder     # 📂 Yangi papka yaratish (my-folder)
rm file.txt         # ❌ Faylni o'chirish
rm -r my-folder     # ❌ Papkani rekursiv o'chirish (ichidagi hamma narsa bilan)
```

**Eslatma**: `rm -rf` dan ehtiyot bo'ling! Qayta tiklab bo'lmasdan o'chirib yuboradi.

---

## **2. Git bilan Ishlash**

### **Loyihani Boshlash**
```bash
git init                    # 🌀 Yangi Git repozitoriyasi yaratish
git add .                   # ➕ Barcha o'zgarishlarni saqlashga tayyorlash
git add index.html          # ➕ Faqat 1 faylni qo'shish
git commit -m "Xabar"       # 💾 O'zgarishlarni saqlash (commit)
git status                  # 🔍 Holatni ko'rish (qaysi fayllar o'zgartirilgan?)
```

**Misol**:  
```bash
git add style.css
git commit -m "Sayt dizaynini yangilash"
```

---

### **Tarixni Ko'rish**
```bash
git log             # 📜 Barcha commitlar tarixi
git log --oneline   # 📜 Qisqacha commitlar ro'yxati
```

---

## **3. Shoxlar (Branches) - "Parallel Universum"**

### **Shoxlar bilan Ishlash**
```bash
git branch                  # 🌿 Barcha shoxlarni ko'rish
git branch new-feature      # 🌿 Yangi shox yaratish
git checkout new-feature    # 🔀 Shoxga o'tish
git checkout -b login-form  # 🌟 Yangi shox yaratib, unga o'tish
git merge login-form        # 🧩 Shoxni asosiy kodga qo'shish
```

**Hayotiy Misol**:  
```bash
git checkout -b footer-design   # Footer dizayni uchun yangi shox
# ... dizayn o'zgartirishlar ...
git commit -m "Footer yangilandi"
git checkout main               # Asosiy shoxga qaytish
git merge footer-design         # Yangi dizaynni asosiy kodga qo'shish
```

---

## **4. GitHub bilan Bog'lanish**

### **Remote Repo bilan Ishlash**
```bash
git remote add origin https://github.com/user/repo.git  # 🌐 Lokal reponi GitHubga ulash
git push -u origin main         # 🚀 Kodni GitHubga birinchi marta yuborish
git push                        # 🔄 Keyingi yangilanishlarni yuborish
git pull                        # 🔄 GitHubdan yangilanishlarni yuklab olish
```

**Eslatma**: Agar `git push` ishlamasa, `git push origin main` deb yozing.

---

## **5. Tez-tez Keladigan Muammolar**

### **"Permission Denied" Xatosi**
```bash
# ❌ Faylni o'chirishda xato:
rm file.txt -> rm -f file.txt    # 🔒 -f (force) parametri bilan urinib ko'ring
```

### **Commit Xabarini O'zgartirish**
```bash
git commit --amend -m "Yangi xabar"  # 🖊️ Oxirgi commit xabarini tahrirlash
```

---

## **6. Foydali Maslahatlar**

### **Terminalda Tezkor Harakatlar**
```bash
ctrl + c          # 🔴 Joriy jarayonni to'xtatish (masalan, serverni o'chirish)
ctrl + l          # 🧹 Terminalni tozalash (yoki `clear` komandasi)
↑ (yuqori tugma)  # ⏫ Oldingi komandalarni qayta chaqirish
```

### **Git Aliaslar (Qisqartmalar)**
```bash
git config --global alias.st "status"  # ✅ `git st` = `git status`
git config --global alias.co "checkout" # ✅ `git co main` = `git checkout main`
```

---

## **7. Amaliy Misol: Loyiha Yarating!**

```bash
mkdir my-site && cd my-site     # Yangi papka
touch index.html               # HTML fayl yaratish
git init                       # Gitni boshlash
git add . && git commit -m "Birinchi commit"
git checkout -b new-design     # Yangi dizayn shoxi
# ... index.html ni tahrirlash ...
git add . && git commit -m "Dizayn yangilandi"
git checkout main              # Asosiy shoxga qaytish
```

---

**🚀 Diqqat!** Terminal qo'rqinchli ko'rinishi mumkin, lekin unga o'rgangan sari **"super kuchlaringiz"** oshadi. Har kuni 10 daqiqa mashq qiling!