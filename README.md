# خطوة 0: تصحيح صياغة فقط (بدون تغيير سلوك)
هذه النسخة تصلّح أخطاء صياغة من ملفك الأخير (backticks, قوسين, قوالب template literals) بحيث تعمل الصفحة كما هي،
بدون تعديل أي وظيفة.

## الخطة المرحلية
1) **خطوة 0 (هذه):** تصحيح صياغة فقط في ملف واحد.
2) **خطوة 1:** فصل الـCSS إلى ملفات `styles.css` و`mobile.css` مع إبقاء الجافاسكربت كما هو.
3) **خطوة 2:** فصل الجافاسكربت إلى وحدات صغيرة (storage/utils/render/events/charts/archive) بدون تغيير منطق.
4) **خطوة 3:** تحسينات شكلية فقط (ألوان/هوامش/جداول) بدون لمس الحسابات.
5) **خطوة 4:** تغطية حماية من التكرار/الضغط، واختبارات سريعة على زر (إضافة بند).

> كل خطوة سأرسلها كملف مضغوط منفصل لضمان عدم كسر أي شيء.


## Step 1 — CSS extraction (no functional change)
- Moved all inline CSS into `styles.css`.
- Moved the mobile-specific CSS (`<style id="mobile-v29">`) into `mobile.css`.
- Injected two `<link>` tags in `<head>`:
  ```html
  <link rel="stylesheet" href="styles.css" />
  <link rel="stylesheet" href="mobile.css" />
  ```
- JavaScript and HTML structure left untouched.
- This step is purely refactor for clarity and easier future edits.


## Step 2 — JavaScript extraction (no functional change)
- Moved all inline `<script>` blocks into a single `app.js`.
- Kept the external Chart.js CDN tag as-is for charts.
- Injected at the end of `<body>`:
  ```html
  <script src="app.js"></script>
  ```
- No logic was modified. Pure refactor for clarity.
