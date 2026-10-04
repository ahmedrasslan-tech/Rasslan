# مفكرة القضايا - مشروع APK

## الطريقة 1: بدون تثبيت أي برنامج (الأسهل)
1. أنشئ حسابًا مجانيًا على github.com ثم مستودعًا جديدًا (New repository).
2. ارفع محتويات هذا المجلد كلها إلى المستودع (Add file > Upload files)، مع مجلد .github.
3. افتح تبويب Actions، اختر Build APK ثم Run workflow.
4. بعد 5-10 دقائق افتح التشغيل الناجح، ونزّل court-diary-apk من قسم Artifacts.
5. فك الضغط وانقل app-debug.apk إلى الهاتف وثبّته (اسمح بالتثبيت من مصدر غير معروف).

## الطريقة 2: على الكمبيوتر
المتطلبات: Node 22 و JDK 21 و Android Studio.
npm install
npx cap add android
(أضف الصلاحيات POST_NOTIFICATIONS و SCHEDULE_EXACT_ALARM و RECEIVE_BOOT_COMPLETED في android/app/src/main/AndroidManifest.xml)
npx cap sync android
npx cap open android   ثم Build > Build APK

## ملاحظات
- التنبيهات هنا مجدولة في نظام أندرويد نفسه، فتعمل والتطبيق مغلق.
- عند أول تشغيل اسمح بالإشعارات. وفي أندرويد 12 فما فوق فعّل "التنبيهات والتذكيرات" للتطبيق من إعدادات النظام لدقة أعلى.
- هذا APK تجريبي (debug) للاستخدام الشخصي. للنشر في Google Play يلزم توقيع Release.
- لتعديل التطبيق عدّل www/index.html فقط.
