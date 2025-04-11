# **Terminal & Git Bash Cheat Sheet (Boshlangʻichlar uchun)**  
**🖥️ Terminal - Dasturchining "Kuchli Qoʻli"!**

---

## **1. Terminalga Kirish: "Qanday Ishlamaydi?" ➡️ "Qanday Ishlasa Boʻladi!"**

### **Nima uchun Terminal?**
- **Fayllar bilan tezroq ishlash** (yuzta faylni bir zumda oʻzgartirish).  
- **Dasturlarni boshqarish** (server ishga tushirish, paketlar oʻrnatish).  
- **Git bilan ishlash** (kod versiyalarini boshqarish).  

**Hayotiy Misol**:  
- **GUI (Grafik Interfeys)**: Faylni oʻchirish uchun sichqoncha bilan 10 marta bosish.  
- **Terminal**: `rm file.txt` ➜ 1 sekund!  

---

## **2. Asosiy Terminal Buyruqlari**

### **Papkalar bilan Ishlash**
```bash
pwd                # 📂 "Men qayerdaman?" (Joriy papkangizni koʻrsatadi)  
cd ~/Desktop       # 📂 Desktop papkasiga oʻtish ("~" - User papkasi)  
cd ..              # 📂 Bir qadam ortga (masalan: "Documents" dan "User" papkasiga)  
ls                 # 📜 Papkadagi hamma narsani koʻrish (fayllar, papkalar)  
ls -a              # 📜 Yashirin fayllarni ham koʻrish (.config, .git)  
```

**Misol**:  
```bash
cd Projects       # Projects papkasiga kirish  
ls                # Papkadagi loyihalarni koʻrish (my-website, blog, app)
```

---

### **Fayl va Papka Yaratish/Oʻchirish**
```bash
touch index.html    # 🆕 Yangi fayl yaratish (index.html)  
mkdir my-project    # 📂 Yangi papka yaratish (my-project)  
rm file.txt         # ❌ Faylni oʻchirish  
rm -r old-project   # 💥 Papkani OʻCHIRISH (Ichidagi HAMMA NARSA bilan!)  
```

**Eslatma**:  
- `rm -rf *` ➜ **Juda Xavfli!** Hammasini tiklanmasdan oʻchirib yuboradi.  
- Avval `ls` bilan tekshiring, keyin oʻchiring!

---

## **3. Git Buyruqlari: "Vaqt Mashinasi" bilan Ishlash**

### **Loyihani Boshlash**
```bash
git init                    # 🌀 Yangi Git repozitoriyasi yaratish  
git add .                   # ➕ Barcha oʻzgarishlarni saqlashga tayyorlash  
git commit -m "Xabar"       # 💾 Versiya yaratish (commit)  
git status                  # 🔍 Oʻzgarishlarni koʻrish  
```

**Hayotiy Misol**:  
```bash
git add style.css           # CSS faylini saqlashga tayyorlash  
git commit -m "Dizayn yangilandi"  # "Dizayn yangilandi" deb versiya yaratish  
```

---

### **Tarixni Koʻrish va Qaytish**
```bash
git log             # 📜 Barcha commitlar roʻyxati  
git checkout a1b2c  # ⏮️ Belgilangan commitga qaytish (a1b2c - commit ID)  
```

---

## **4. Git Shoxlari (Branches): "Parallel Haqiqatlar"**

### **Nega Shoxlar Kerak?**  
- **Xavfsizlik**: Yangi kodni sinab koʻrish (asosiy kod buzilmasin).  
- **Jamoa Ishi**: Har bir dasturchi alohida shoxda ishlaydi.  

### **Asosiy Buyruqlar**
```bash
git branch                  # 🌿 Barcha shoxlarni koʻrish  
git checkout -b login-form  # 🆕 Yangi shox yaratish va unga oʻtish  
git checkout main           # 🔙 Asosiy shoxga qaytish  
git merge login-form        # 🧩 Shoxni asosiy kodga qoʻshish  
```

**Hayotiy Misol**:  
1. `git checkout -b yangi-dizayn` ➜ Yangi dizayn ustida ishlash.  
2. Dizaynni test qilish ➜ Ishlasa, `git merge yangi-dizayn`.  
3. Ishlamasa ➜ Shoxni oʻchirib (`git branch -d yangi-dizayn`), yangi urinish!

---

## **5. GitHub: Kodni Bulutga Saqlash**

### **Birinchi Marotaba Kod Yuklash**
```bash
git remote add origin https://github.com/user/repo.git  # 🌐 GitHubga ulanish  
git push -u origin main         # 🚀 Kodni birinchi marta yuborish  
git push                        # 🔄 Keyingi yangilanishlarni yuborish  
```

### **Jamoadoshdan Kodni Yuklab Olish**
```bash
git pull               # 🔄 Jamoadoshning kodini o'z kompyuteringizga yuklash  
```

---

## **6. Tez-tez Keladigan Muammolar**

### **"Permission Denied" (Ruxsat Yoʻq)**
```bash
# Faylni oʻchirishda xato:  
rm file.txt -> sudo rm file.txt    # 🔑 Administrator huquqlari bilan oʻchirish (Linux/macOS)  
```

### **Commit Xabarini Tahrirlash**
```bash
git commit --amend -m "Yangi xabar"  # ✏️ Oxirgi commit xabarini oʻzgartirish  
```

---

## **7. Pro Maslahatlar**

### **Terminalda Tezkorlik**
```bash
ctrl + C          # 🔴 Jarayonni toʻxtatish (masalan, server ishini)  
ctrl + L          # 🧹 Ekranni tozalash  
tab               # 🔄 Fayl nomini avto-toʻldirish (masalan, "ind" ➜ "index.html")  
```

### **Git Aliaslar (Qisqartmalar)**
```bash
git config --global alias.st "status"     # ✅ `git st` = `git status`  
git config --global alias.cm "commit -m"  # ✅ `git cm "Xabar"` = `git commit -m "Xabar"`  
```

---

## **8. Amaliy Mashq: Loyiha Yaratamiz!**

```bash
mkdir my-app && cd my-app    # Yangi loyiha papkasi  
touch index.html            # HTML fayl yaratish  
git init                    # Gitni boshlash  
git add . && git commit -m "Birinchi versiya"  
git checkout -b contact-form  # Yangi shox  
# ... contact form qo'shish ...  
git add . && git commit -m "Kontakt formasi qo'shildi"  
git checkout main           # Asosiy shoxga qaytish  
git push -u origin main     # GitHubga yuborish  
```

---

**🎯 Diqqat!**  
- **Xato qilishdan qoʻrqmang** ➜ Barcha buyruqlarni qaytarish mumkin.  
- **Har kuni 5 daqiqa Terminalda mashq qiling** ➜ 1 oyda "pro" boʻlasiz!  

**🚀 Omad! Terminal sizning eng ishonchli yordamchingiz boʻladi!**