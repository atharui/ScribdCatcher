# ScribdCatcher

## العربية

يحوّل ScribdCatcher الصفحات المعروضة في قارئ مستندات Scribd إلى PDF مرتّب. استخدم نسخة ويندوز لمعالجة عدة روابط على الكمبيوتر، ونسخة أندرويد لحفظ مستند وفتحه أو مشاركته من الجوال.

| النظام | الإصدار | التنزيل |
|---|---|---|
| ويندوز 64 بت | 1.0.27 | [تنزيل ملف ZIP](https://github.com/atharui/ScribdCatcher/raw/refs/heads/main/downloads/ScribdCatcher-Windows-1.0.27.zip) |
| أندرويد | 1.0.52 | [تنزيل ملف APK](https://github.com/atharui/ScribdCatcher/raw/refs/heads/main/downloads/ScribdCatcher-Android-1.0.52.apk) |

### ويندوز

**المتطلبات** — ويندوز 64 بت مع Windows PowerShell، وGoogle Chrome، وNode.js 20 أو أحدث، وأداة uv. يجب أن يتعرّف PowerShell على الأمرين `node` و`uv`. عند أول تصدير، يجهّز uv بيئة Python 3.12 ومكتبتي PyMuPDF وPillow. يلزم اتصال بالإنترنت ومساحة للملفات المؤقتة والناتج.

1. فك ضغط المجلد كاملًا وافتح `ScribdCatcher.exe`.
2. الصق رابطًا واحدًا أو عدة روابط، كل رابط في سطر. اختر طريقة التصدير والدقة ومجلد الحفظ.
3. حدّد مستندًا واضغط **معاينة المستند المحدد** لمشاهدة أول ثلاث صفحات منه، أو جميع صفحاته إذا كان أقصر.
4. اضغط **بدء التصدير** لمعالجة القائمة بالترتيب وحفظ PDF مستقل لكل مستند. تستطيع تصغير النافذة أثناء العمل، والإيقاف المؤقت بين الصفحات ثم الاستئناف. يسجّل البرنامج التقدم والأخطاء في مجلد `Logs` داخل مجلد الحفظ.

يحفظ **الالتقاط المرئي** كل صفحة كصورة. تحاول طريقتا **الطباعة** و**SVG** الحفاظ على النص وعناصر الصفحة عندما يسمح تخطيطها بذلك. الدقة الأعلى تزيد حجم الملفات المصوّرة، خصوصًا في الكتب الطويلة.

### أندرويد

**المتطلبات** — الحد الأدنى المعلن في الحزمة Android 5.0 ‏(API 21)، مع WebView مفعّل واتصال بالإنترنت ومساحة للحفظ. لم يُختبر التطبيق ميدانيًا على كل إصدارات أندرويد المدعومة في الحزمة.

1. نزّل ملف APK وثبّته. إذا طلب أندرويد الإذن بالتثبيت من المتصفح أو مدير الملفات، امنحه للتطبيق الذي فتحت منه الملف.
2. الصق رابط المستند واختر مجلد الحفظ وطريقة التصدير ثم ابدأ الالتقاط. يمكن أيضًا لصق رابط HTTPS مباشر لملف PDF وحفظ الأصل.
3. يقرأ التطبيق عدد الصفحات تلقائيًا. عند غياب العدّاد يتابع الصفحات المرقمة التي تظهر في العارض. إذا تأخرت الصفحة التالية أكثر من نحو 11 ثانية، قد يحفظ التطبيق الصفحات التي ظهرت فقط ويعرض عددها.
4. للمستندات الطويلة، فعّل من **خيارات التصدير** حفظ كل 12 صفحة في PDF مستقل لتقليل استهلاك الذاكرة. يتضمن اسم كل جزء نطاق صفحاته. بعد الحفظ يمكنك فتح الملف أو مشاركته.

## English

ScribdCatcher exports pages displayed in the Scribd document viewer to an ordered PDF. The Windows edition processes a list of links. The Android edition saves a document on your phone and lets you open or share the result.

| Platform | Version | Download |
|---|---|---|
| Windows 64-bit | 1.0.27 | [Download ZIP](https://github.com/atharui/ScribdCatcher/raw/refs/heads/main/downloads/ScribdCatcher-Windows-1.0.27.zip) |
| Android | 1.0.52 | [Download APK](https://github.com/atharui/ScribdCatcher/raw/refs/heads/main/downloads/ScribdCatcher-Android-1.0.52.apk) |

### Windows

**Requirements** — 64-bit Windows with Windows PowerShell, Google Chrome, Node.js 20 or later, and uv. Both `node` and `uv` must be available on PATH. On the first export, uv prepares a Python 3.12 environment with PyMuPDF and Pillow. Allow internet access and enough disk space for temporary pages and the output.

1. Extract the entire ZIP and open `ScribdCatcher.exe`.
2. Paste one document link per line. Choose an export method, capture resolution, and destination folder.
3. Select a document and choose **Preview selected document** to see up to its first three pages.
4. Start the export to process the list in order and save one PDF per document. You can minimize the window, pause between pages, and resume. Progress and errors are recorded in the `Logs` subfolder of the destination.

**Visible capture** saves pages as images. **Print** and **SVG** attempt to retain text and page elements when the layout permits. Higher capture resolutions can produce much larger files for long books.

### Android

**Requirements** — The APK declares Android 5.0 (API 21) as its minimum. It needs an enabled WebView, internet access, and storage for the export. Device testing has not covered every Android version declared by the APK.

1. Download and install the APK. If Android asks, allow installation from the browser or file manager that opened the package.
2. Paste a document link, select a destination folder and export method, then start capture. You can also paste a direct HTTPS PDF link to save the original.
3. The app detects the page count automatically. When the viewer omits the total, the app follows numbered pages as they appear. If the next page takes longer than about 11 seconds, the saved PDF can be partial. The completion message reports how many pages were saved.
4. For long documents, enable **Long documents** in export options to save up to 12 pages per PDF and reduce memory use. Each part includes its page range in the filename. Open or share the saved file from the app.
