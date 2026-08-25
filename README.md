# Kuzatuv Cam - Telegram Bot E-commerce System

Bu loyiha to'liq e-commerce tizimini Telegram Mini App (Web App) ko'rinishida o'z ichiga oladi. U mahsulotlar katalogi, savat, SMS orqali tasdiqlash, admin paneli va Firebase real-time sinxronizatsiyasiga ega.

## 📂 Loyiha tuzilishi

- \`app.js\`: Asosiy mantiq (JavaScript), holatni boshqarish (state), Firebase bilan ishlash, Telegram Mini App integratsiyasi va UI yangilash.
- \`index.html\`: Yagona sahifali (SPA) tuzilma, onboarding, OTP, bosh sahifa, savat, profil va admin qismlarini o'z ichiga oladi.
- \`style.css\`: O'ziga xos dizayn, mobil qurilmalar uchun moslashtirilgan interfeys, va turli elementlarning uslublari (CSS).
- \`products-data.js\`: Boshlang'ich mahsulotlar va kategoriyalar ro'yxati (katalog).
- \`README.md\`: Loyiha haqida ma'lumot va o'rnatish qo'llanmasi.

## 🚀 Texnologiyalar va Xususiyatlar

*   **Frontend:** HTML, CSS, JavaScript (Vanilla - frameworklarsiz)
*   **Backend/Ma'lumotlar bazasi:** Firebase Realtime Database (mahsulotlar, akkauntlar, izohlar sinxronizatsiyasi uchun)
*   **Integratsiyalar:**
    *   Telegram Mini App (Web App API)
    *   Telegram Bot API (Buyurtmalarni kanal/guruhga yuborish uchun)
    *   iSMS.uz API (SMS OTP tasdiqlash uchun)
*   **Xususiyatlar:**
    *   Foydalanuvchi va Admin rollari.
    *   SMS orqali xavfsiz avtorizatsiya.
    *   Mahsulotlarni kategoriyalar bo'yicha filtrlash, qidirish.
    *   Savat va kabel hisoblagichi.
    *   Joylashuvni aniqlash orqali buyurtma berish.
    *   Admin tomonidan mahsulot/kategoriya qo'shish, o'chirish, tahrirlash.
    *   Real-time izohlar.

## 🛠️ O'rnatish va Sozlash

### 1. Telegram Bot va Kanal sozlamalari
1. @BotFather orqali yangi bot yarating va uning Tokenini oling.
2. Botni buyurtmalar tushadigan guruh yoki kanalga **Admin** sifatida qo'shing.
3. \`app.js\` faylini oching va \`CONFIG\` qismida quyidagilarni o'zgartiring:
   - \`BOT_TOKEN\`: Botfather'dan olingan token.
   - \`CHAT_ID\`: Bot qo'shilgan guruh/kanal ID si yoki username si.

### 2. Firebase Sozlamalari (Ixtiyoriy, lekin umumiy ishlashi uchun zarur)
Agar Firebase ulanmasa, tizim faqat shu qurilma xotirasida (localStorage) ishlaydi (demo rejim).
1. [Firebase Console](https://console.firebase.google.com/) da yangi loyiha yarating.
2. Realtime Database bo'limini yoqing va qoidalarni \`true\` qilib o'rnating (test uchun).
3. Loyiha sozlamalaridan Web App qo'shing va u yerdagi konfiguratsiyani \`app.js\` dagi \`CONFIG.FIREBASE\` qismiga yozing.

### 3. SMS Tasdiqlash (iSMS.uz)
1. iSMS.uz saytida ro'yxatdan o'ting va API kalit oling.
2. \`app.js\` dagi \`CONFIG.SMS.API_KEY\` va qurilma nomini (\`DEVICE_ID\`) kiritib qo'ying.
   *Eslatma: Tizimga admin sifatida kirish uchun ismga "Sirius", telefonga "sIRIUS746" kiritish orqali SMS ni chetlab o'tish mumkin (app.js da ko'rsatilganidek).*

### 4. Ishga tushirish
Fayllarni oddiy veb-serverga (masalan, Vercel, Netlify yoki GitHub Pages) yuklang va manzilni Telegram Botga Web App sifatida ulang.
