# **Git Shoxlari (Branches) - Tushuncha va Hayotiylashtirilgan Misollar**

---

## **Shox (Branch) Nima?**
**Shox** - Loyihangizning parallel versiyasi. Bitta daraxtning turli shoxlari kabi, siz asosiy kodga ta'sir qilmasdan yangi xususiyatlar, tuzatishlar yoki eksperimentlar uchun alohida "shox" yaratishingiz mumkin. Har bir shox mustaqil ishlaydi.

### **Nega Shoxlar Kerak?**
1. **Asosiy kodni himoya qilish**: Yangi kodni sinab ko'rishda asosiy (main) branch xavfsiz qoladi.
2. **Bir vaqtning o'zida bir necha ish**: Jamoa a'zolari turli xususiyatlarni alohida shoxlarda ishlaydi.
3. **Xatolarni tuzatish**: Asosiy branchda xato topilsa, yangi shox ochib tezda tuzatish mumkin.

---

## **Hayotiy Misollar bilan Tushuntirish**

### **Misol 1: Restoran Menyusi (Asosiy Branch)**
- **Main branch** - Restoran menyusi (dishlar ro'yxati).
- **Yangi shox** - Yangi taom qo'shish uchun.
  
**Qadamlar**:
1. `git switch -c yangi-taom` - Yangi shox yaratish.
2. Menyuga yangi taom qo'shing.
3. `git commit -m "Yangi taom qo'shildi"` - O'zgarishlarni saqlash.
4. Taomni test qiling.
5. `git switch main` - Asosiy menyuga qaytish.
6. `git merge yangi-taom` - Yangi taomni asosiy menyuga qo'shish.

### **Misol 2: Veb-saytda Xato Tuzatish**
- **Main branch** - Ishlayotgan veb-sayt.
- **Bug branch** - Xatolarni tuzatish uchun.

**Qadamlar**:
1. `git switch -c footer-xato` - Xato uchun shox yaratish.
2. Saytning footer qismidagi xatoni tuzating.
3. `git commit -m "Footer xatosi tuzatildi"` - Saqlang.
4. Xatoni tekshirib ko'ring.
5. `git switch main` - Asosiy saytga qayting.
6. `git merge footer-xato` - Tuzatilgan koddan foydalaning.

---

## **Shoxlar bilan Ishlash: Komandalar**

### **1. Shox Yaratish va O'tish**
```bash
git branch yangi-shox      # Shox yaratish
git switch yangi-shox      # Shoxga o'tish
# Yoki qisqa yo'l:
git switch -c yangi-shox   # Yarash va o'tish
```

### **2. Shoxni GitHubga Yuklash**
```bash
git push -u origin yangi-shox  # Birinchi marta
git push                      # Keyingi commitlar
```

### **3. Shoxlarni Ro'yxatini Ko'rish**
```bash
git branch       # Lokal shoxlar
git branch -a    # Barcha shoxlar (lokal + remote)
```

### **4. Shoxni Birlashtirish (Merge)**
```bash
git switch main              # Asosiy shoxga o'tish
git merge yangi-shox         # Yangi-shoxni mainga qo'shish
```

### **5. Shoxni O'chirish**
```bash
git branch -d yangi-shox     # Lokal shoxni o'chirish
git push origin --delete yangi-shox  # Remote shoxni o'chirish
```

---

## **Konfliktlar (Conflict) Nima va Qanday Hal Qilish?**

### **Misol: Ikki Kishi Bir Faylni O'zgartirsa**
1. **Ali** `main` branchda `style.css` ni o'zgartiradi va GitHubga yuboradi.
2. **Vali** o'z shoxida `style.css` ni o'zgartiradi va `git merge main` qilganda **konflikt** paydo bo'ladi.
3. Git konfliktni hal qilishni so'raydi:
   ```css
   <<<<<<< HEAD
   .button { color: blue; }  # Vali kodi
   =======
   .button { color: red; }   # Ali kodi
   >>>>>>> main
   ```
4. **Yechim**: Kerakli kodni tanlang, konflikt belgilarini o'chiring va commit qiling.

---

## **Eng Yaxshi Amaliyotlar**
1. **Asosiy shoxni himoya qiling**:
   - Faqat testlardan o'tgan kodni `main` ga qo'shing.
2. **Shox nomini aniq belgilang**:
   - `feature/login`, `bugfix/footer-error` kabi.
3. **Tez-tez yangilang**:
   ```bash
   git switch main
   git pull          # O'zgarishlarni yuklab olish
   git switch sizning-shox
   git merge main    # Asosiy kod bilan yangilash
   ```

---

## **Xulosa**
**Shoxlar** - Dasturchining "xavfsiz maydonchasi". Xoh yangi xususiyat ishlang, xoh xatolarni tuzating, barcha tajribalaringizni shoxlarda amalga oshiring. Asosiy loyihangiz xavfsiz qolsin! 🛡️