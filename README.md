# ماركو للأثاث الراقي - موبايل أبليكيشن

## التثبيت والبناء

### 1. تثبيت المتطلبات
- Node.js 18+ من nodejs.org
- Android Studio من developer.android.com
- Java JDK 17

### 2. إنشاء المشروع
mkdir MARCO-MOBILE-APP
cd MARCO-MOBILE-APP
# انسخ ملفات package.json و capacitor.config.json هنا
# انسخ مجلد www اللي فيه index.html و manifest.json و icon.png

npm install

### 3. إضافة أندرويد
npx cap add android

### 4. نسخ ملفات الويب للأندرويد
npx cap copy
npx cap sync

### 5. فتح في Android Studio وبناء APK
npx cap open android

# داخل Android Studio:
# Build > Build Bundle(s) / APK(s) > Build APK(s)
# أو Build > Generate Signed Bundle / APK للنسخة النهائية للمتجر

APK هيكون في:
android/app/build/outputs/apk/debug/app-debug.apk

### 6. لتحديث التطبيق بعد تعديل www/index.html
npx cap copy
npx cap sync
# ثم Build تاني من Android Studio
