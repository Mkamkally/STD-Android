# متتبع التقدم الدراسي (SPT) + المستشار الأكاديمي الذكي

**متتبع التقدم الدراسي (Study Progress Tracker - SPT)** هو تطبيق أندرويد حديث يعمل دون الحاجة للاتصال بالإنترنت لتخزين بياناتك (Offline-First)، تم تطويره باستخدام **Kotlin** و **Jetpack Compose (Material 3)** وقاعدة بيانات **Room**. يساعد التطبيق الطلاب على تنظيم الفصول الدراسية والمواد والمحاضرات والمعامل والملاحظات والتنبيهات، مع دمج **مستشار أكاديمي ذكي** يدعم الإملاء الصوتي والتحكم المباشر ببيانات التطبيق وربط أي مزود ذكاء اصطناعي خارجي.

---

## 📥 تحميل التطبيق وتثبيته

- **[تحميل ملف التطبيق `SPT-v1.0.0.apk`](./SPT-v1.0.0.apk)**

> **المتطلبات:** نظام Android 8.0 (API 26) أو أحدث. قد يُطلب منك تفعيل خيار *"التثبيت من مصادر غير معروفة"* عند تثبيت ملف APK مباشرة على جهازك.

---

## ✨ أبرز المميزات

### 1. تنظيم الدراسة وتتبع التقدم الأكاديمي
- **الفصول الدراسية والمواد:** إنشاء وتعديل وإعادة ترتيب وحذف الفصول الدراسية والمواد مع حفظ محلي آمن ودائم عبر قاعدة بيانات Room.
- **توليد المحاضرات والمعامل تلقائياً:** عند إنشاء أو تعديل أي مادة، يقوم التطبيق بتوليد المحاضرات (`Lecture 1..N`) والمعامل (`Lab 1..M`) تلقائياً بالعدد المطلوب.
- **تتبع الإنجاز ومستوى الصعوبة:** متابعة حالة إنجاز كل محاضرة أو معمل، وتحديد مدة الدراسة المتوقعة ومستوى الصعوبة (سهل، متوسط، صعب) بمؤشر بصري مدمج.
- **مساحة العمل والملاحظات:** تدوين الملاحظات الدراسية لكل عنصر، وإضافة وسوم افتراضية أو مخصصة (مثل: `Exam`، `Important`، `Need Revision`، `Assignment`، `Quiz`، `Project`)، مع إمكانية ربط مجلد محلي من ذاكرة الهاتف عبر إطار `SAF`.
- **لوحة التحليلات الذكية:** حساب فوري لنسبة الإنجاز الإجمالية، وعدد العناصر المنجزة والمتبقية، وتحديد **أكثر المواد إنجازاً**، و**أضعف المواد (الأقل إنجازاً)**، و**أصعب المواد**، بالإضافة إلى سجل النشاطات الأخيرة.
- **البحث الشامل:** البحث السريع داخل جميع الفصول والمواد والمحاضرات والملاحظات والوسوم.
- **التنبيهات الذكية:** جدولة تذكيرات للمذاكرة مع خيارات التكرار (بدون تكرار، يومي، أسبوعي، شهري، سنوي).
- **النسخ الاحتياطي والاستعادة (JSON):** تصدير كامل بياناتك إلى ملف `.json` واستعادتها في أي وقت إما عبر **الدمج (Merge)** أو **الاستبدال الشامل (Full Replace)**.

### 2. المستشار الأكاديمي الذكي والتحكم بالبيانات
- **تشخيص نقاط الضعف والفجوات المهارية:** يحلل بياناتك الدراسية الحالية ليحدد بدقة المواد التي تعاني فيها أو تتأخر في إنجازها، ويكتشف المهارات الناقصة ويقترح مسارات وظيفية مناسبة لك.
- **بطاقات معاينة وتأكيد لتعديل البيانات:** يمكنك الطلب من الذكاء الاصطناعي إنشاء خرائط طريق دراسية متكاملة، أو إنشاء/تعديل/حذف الفصول والمواد، أو تحديد محاضرات ومعامل معينة كمكتملة ✅ أو غير مكتملة ⬜ — حيث تظهر لك **بطاقة معاينة وتأكيد** واضحة قبل تنفيذ التعديلات بضغطة زر.
- **الإملاء الصوتي المباشر (Speech-to-Text):** زر ميكروفون مدمج بجانب زر الإرسال للتحدث وتحويل كلامك مباشرة إلى نص جاهز للإرسال باللغتين العربية والإنجليزية.
- **دعم مرن لمزودي الذكاء الاصطناعي:**
  - يعمل التطبيق افتراضياً ومباشرة بواسطة **Groq (`openai/gpt-oss-120b`)**.
  - يتيح لك في **الإعدادات** إدخال بيانات أي مزود خارجي مخصص (**Base URL** + **Model Name** + **API Key**) لدعم خدمات مثل Groq و OpenAI و OpenRouter و DeepSeek و Google Gemini أو أي واجهة متوافقة مع OpenAI، مع زر **فحص الاتصال** واستعادة الافتراضي في أي وقت.

### 3. الواجهة واللغات والتخصيص
- **دعم العربية والإنجليزية:** اللغة العربية (RTL) هي اللغة الأساسية في التطبيق مع إمكانية التبديل الفوري إلى اللغة الإنجليزية (LTR) من شاشة الإعدادات.
- **تصميم Material 3 ثنائي الألوان ومُنتقي ألوان مخصص:** دعم الوضع الفاتح والداكن وتلقائي النظام، مع ألوان جاهزة (الأخضر الزمردي والأزرق) بالإضافة إلى نافذة **اختيار لون مخصص (HSV + Hex)** لتحديد أي درجة لونية تفضلها بحرية.


# Study Progress Tracker (SPT) + AI Academic Advisor

**Study Progress Tracker (SPT)** is a modern, offline-first Android application built with **Kotlin**, **Jetpack Compose (Material 3)**, and **Room Database**. It helps students organize their academic semesters, courses, lectures, labs, study notes, and reminders while featuring an intelligent **AI Academic Advisor & Data Controller** with voice dictation and multi-provider API support.

---

## 📥 Download & Install

- **[Download `SPT-v1.0.0.apk`](./SPT-v1.0.0.apk)**

> **Requirements:** Android 8.0 (API 26) or higher. Enable *"Install from unknown sources"* if prompted when installing the APK directly.

---

## ✨ Key Features

### 1. Academic Hierarchy & Study Progress Tracking
- **Semesters & Courses:** Create, rename, edit descriptions, reorder, and delete semesters and courses with persistent local Room storage.
- **Auto-Generated Lectures & Labs:** Automatically generate numbered lectures and practical labs (`Lecture 1..N`, `Lab 1..M`) when creating or updating a course.
- **Compact Difficulty & Completion Tracking:** Track completion status, estimated study duration, and difficulty levels (`Easy`, `Medium`, `Hard`).
- **Study Workspace:** Write notes per study item, organize with default and custom tags (`Exam`, `Important`, `Need Revision`, `Assignment`, `Quiz`, `Project`), and attach local device folders via Android's Storage Access Framework (`SAF`).
- **Analytics Dashboard:** Real-time calculation of overall progress percentage, completed vs. pending items, **Most Completed**, **Weakest / Least Completed**, and **Hardest** courses, plus a recent activity log.
- **Global Search:** Quickly search across semesters, courses, study items, notes, and tags.
- **Smart Reminders:** Schedule study notifications with repeat options (`Never`, `Daily`, `Weekly`, `Monthly`, `Yearly`).
- **JSON Backup & Restore:** Export your entire database to a `.json` file and restore anytime using either **Merge** or **Full Replace**.

### 2. AI Academic Advisor & Interactive Data Control
- **Weakness & Skill-Gap Diagnosis:** Analyzes your live local academic data to pinpoint weak courses, identify missing skills, and suggest tailored career paths.
- **Interactive Preview & Confirmation Cards:** Ask the AI to generate multi-semester learning roadmaps, create/rename/delete semesters or courses, or mark specific lectures and labs as completed/uncompleted—review everything in a clear preview card before applying with one tap.
- **Voice Input (Speech-to-Text):** Dedicated microphone button next to the send button for hands-free Arabic or English voice dictation directly into the chat box.
- **Flexible AI Provider Support (Built-in + BYOK):**
  - Powered out of the box by **Groq (`openai/gpt-oss-120b`)**.
  - Full **Bring Your Own Provider** support in **Settings**: enter any custom **Base URL**, **Model Name**, and **API Key** (supports Groq, OpenAI, OpenRouter, DeepSeek, Google Gemini, or any OpenAI-compatible endpoint) with a built-in **Test Connection** button.

### 3. Bilingual Interface & Custom Theming
- **Arabic & English Support:** Arabic (RTL) by default with an instant in-app toggle to switch between **العربية** and **English** in Settings.
- **Two-Tone Material 3 Design & Custom Color Picker:** Clean light/dark/system themes with **Emerald**, **Blue**, and an interactive **HSV + Hex Custom Color Picker** so you can choose any accent shade.
