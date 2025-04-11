=# Git & GitHub: Boshlang'ich Dasturchilar uchun Qo'llanma.

---

## **Kirish**
- **Git** - Bu fayllaringizdagi o'zgarishlarni kuzatib boradigan "vaqt mashinasi". Misol uchun, loyihangizni 1-hafta oldingi holatiga qaytarish imkoniyati.
- **GitHub** - Git repozitoriyalarini saqlash va jamoa bilan ishlash uchun bulut platforma.
- **Repozitoriy (Repo)** - Loyihangizning barcha fayllari va ularning versiya tarixi saqlanadigan papka.
- **Commit** - Loyihadagi o'zgarishlarning "surati" (snapshot) va izoh xabari.

---

## **Git O'rnatish**

### **Windows**
1. [git-scm.com](https://git-scm.com/download/win) saytidan Gitni yuklab oling.
2. O'rnatuvchini ishga tushiring va standartz sozlamalarni tanlang.

### **macOS**
1. **Homebrew** orqali:
   ```bash
   brew install git
   ```
2. Yoki [git-scm.com](https://git-scm.com/download/mac) saytidan yuklab oling.

### **Linux (Debian/Ubuntu)**
```bash
sudo apt update && sudo apt install git
```

---

## **Git ga Ismingizni Tanishtirish**
Har bir commitda kimligingiz ko'rinishi uchun:
```bash
git config --global user.name "Ismingiz"
git config --global user.email "email@manzilingiz.com"
```

---

## **Asosiy Git Buyruqlari**

### **1. Repozitoriy Yaratish (init)**
Loyiha papkasida Git repozitoriyasini yaratish:
```bash
git init
```

### **2. Fayllarni Saqlashga Tayyorlash (add)**
Barcha fayllarni "staging" zonasiga qo'shish:
```bash
git add .  # Joriy papkadagi hamma fayllar
```
- Faqat bitta faylni qo'shish: `git add index.html`.

### **3. Holatni Ko'rish (status)**
Qaysi fayllar o'zgartirilgan yoki tayyor ekanligini ko'rsatadi:
```bash
git status
```

### **4. Commit Qilish (commit)**
O'zgarishlarni saqlash va xabar qoldirish:
```bash
git commit -m "Login formasini qo'shish"
```

### **5. Shoxlar (Branches)**
- **Barcha shoxlarni ko'rish**:
  ```bash
  git branch
  ```
- **Yangi shox yaratish**:
  ```bash
  git branch yangi-shox        # Shox yaratish
  git switch yangi-shox        # Shoxga o'tish
  ```
  Yoki bir qatorda:
  ```bash
  git switch -c yangi-shox
  ```
- **Boshqa shoxga o'tish**:
  ```bash
  git switch asosiy-shox
  ```
- **Shox nomini o'zgartirish**:
  ```bash
  git branch -m eski-nom yangi-nom
  ```
- **Shoxni o'chirish**:
  ```bash
  git branch -d shox-nomi
  ```

---

## **GitHub bilan Ishlash**

### **1. GitHubda Repozitoriy Yaratish**
1. GitHub.com ga kiring.
2. **+** tugmasini bosing va **New Repository** tanlang.
3. Repo nomini yozing (masalan, `my-project`) va **Create** tugmasini bosing.

### **2. Loyihani GitHubga Ulash**
Lokal repozitoriyani GitHubga bog'lash:
```bash
git remote add origin https://github.com/foydalanuvchi-nomi/repo-nomi.git
```

### **3. O'zgarishlarni GitHubga Yuklash (push)**
Commitlarni GitHubga jo'natish:
```bash
git push -u origin main  # Birinchi marta
git push                # Keyingi safarlar
```

---

## **HAYOTIY MISOLLAR**

### **Misol 1: Yangi Loyiha Boshlash**
1. Yangi papka yaratish:
   ```bash
   mkdir my-website && cd my-website
   ```
2. Git repozitoriyasini ishga tushirish:
   ```bash
   git init
   ```
3. `index.html` faylini yaratish va kod yozish.
4. Barcha o'zgarishlarni commit qilish:
   ```bash
   git add .
   git commit -m "Birinchi veb-sahifa yaratildi"
   ```

### **Misol 2: Yangi Xususiyat Qo'shish (Branch)**
1. Yangi branch yaratish:
   ```bash
   git switch -c contact-form
   ```
2. `contact.html` faylini yaratish.
3. O'zgarishlarni commit qilish:
   ```bash
   git add contact.html
   git commit -m "Kontakt formasini qo'shish"
   ```
4. GitHubga yangi branchni yuklash:
   ```bash
   git push -u origin contact-form
   ```

### **Misol 3: Xatoni Tuzatish**
1. `index.html` da xato borligini aniqlang.
2. Xatoni tuzating va saqlang.
3. Commit qiling:
   ```bash
   git add index.html
   git commit -m "Xato tuzatildi"
   ```
4. GitHubga yuboring:
   ```bash
   git push
   ```

---

## **Tez-tez Sodir Bo'ladigan Muammolar**
- **Commit qila olmayapman!**  
  `user.name` va `user.email` sozlanmagan. Sozlang:
  ```bash
  git config --global user.name "Ismingiz"
  ```
- **GitHub parol sorayapti!**  
  GitHubga SSH kalit bilan ulaning yoki token ishlating.

---

## **Maslahatlar**
- Har doim `git status` ni tekshiring.
- Kichik o'zgarishlarni tez-tez commit qiling.
- Yangi xususiyatlar uchun alohida branch oching.

--- 

**Muvaffaqiyat!** Git va GitHub sizning loyihalaringizni xavfsiz saqlash, jamoadoshlar bilan hamkorlik qilish va code tarixini kuzatishda eng ishonchli yordamchingiz bo'ladi. 🚀