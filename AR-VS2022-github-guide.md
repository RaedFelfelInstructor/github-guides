# دليل GitHub لمستخدمي Visual Studio 2022

## مقدمة

سيساعد هذا الدليل طلاب البرمجة على استخدام GitHub بكفاءة مع Visual Studio 2022. يوفر Visual Studio تكاملاً قوياً مع GitHub، مما يتيح لك تنفيذ معظم عمليات Git مباشرة من بيئة التطوير المتكاملة دون الاعتماد على أوامر سطر الأوامر.

## جدول المحتويات

1. [إعداد GitHub في Visual Studio](#1-إعداد-github-في-visual-studio)
2. [إنشاء مستودع](#2-إنشاء-مستودع)
3. [استنساخ مستودع](#3-استنساخ-مستودع)
4. [سحب تغييرات المستودع](#4-سحب-تغييرات-المستودع)
5. [تثبيت التغييرات](#5-تثبيت-التغييرات)
6. [تجهيز التغييرات](#6-تجهيز-التغييرات)
7. [دفع التغييرات](#7-دفع-التغييرات)
8. [إنشاء طلبات السحب](#8-إنشاء-طلبات-السحب)
9. [إنشاء وإدارة الفروع](#9-إنشاء-وإدارة-الفروع)
10. [دمج الفروع](#10-دمج-الفروع)
11. [تخزين التغييرات مؤقتاً](#11-تخزين-التغييرات-مؤقتاً)
12. [حل التعارضات](#12-حل-التعارضات)

## 1. إعداد GitHub في Visual Studio

### الاتصال الأولي بحساب GitHub

1. افتح Visual Studio 2022
2. اذهب إلى **File > Account Settings**
3. في قسم "All Accounts"، انقر على **Add**
4. اختر **GitHub** من قائمة أنواع الحسابات
5. انقر على **Sign in** واتبع التعليمات للمصادقة باستخدام حساب GitHub الخاص بك

### تكوين إعدادات Git

1. اذهب إلى **Tools > Options**
2. انتقل إلى **Source Control > Git Global Settings**
3. أدخل اسمك وبريدك الإلكتروني (سيظهران في التثبيتات)
4. اضبط الإعدادات الأخرى حسب الحاجة (قوالب رسائل التثبيت، أدوات المقارنة، إلخ)

## 2. إنشاء مستودع

### إنشاء مستودع جديد على GitHub من Visual Studio

1. اذهب إلى **File > New > Repository**
2. اختر **GitHub** كنوع المستودع
3. املأ:
   - اسم المستودع
   - الوصف (اختياري)
   - المسار المحلي حيث سيتم إنشاء المستودع
   - حدد ما إذا كان المستودع عامًا أو خاصًا
4. انقر على **Create**

### تحويل مشروع موجود إلى مستودع Git

1. مع فتح مشروعك، اذهب إلى **Git > Create Git Repository**
2. اختر موقع المستودع
3. تحقق من **Add to GitHub** إذا كنت تريد نشره على الفور
4. املأ تفاصيل المستودع وانقر على **Create and Push**

## 3. استنساخ مستودع

### الاستنساخ من GitHub

1. اذهب إلى **Git > Clone Repository**
2. في قسم "Browse a Repository"، اختر **GitHub**
3. قم بتسجيل الدخول إذا طُلب منك ذلك
4. اختر المستودع الذي تريد استنساخه من قائمة المستودعات الخاصة بك
   - استخدم شريط البحث للعثور على مستودعات محددة
   - قم بالتصفية حسب المالك (حسابك أو المؤسسات التي تنتمي إليها)
5. اختر المسار المحلي حيث تريد استنساخ المستودع
6. انقر على **Clone**

## 4. سحب تغييرات المستودع

### سحب التغييرات من GitHub

1. افتح مشروعك
2. في شريط الحالة أسفل Visual Studio، سترى معلومات Git
3. ابحث عن مؤشرات للتغييرات الواردة (عادة ما تظهر كـ ↓ مع رقم)
4. انقر على مؤشر Git في شريط الحالة واختر **Pull**

بديلاً:
1. اذهب إلى **Git > Pull**
2. ستعرض نافذة تغييرات Git التغييرات الواردة بعد السحب

## 5. تثبيت التغييرات

### عرض وتثبيت التغييرات

1. قم بإجراء تغييرات على الكود الخاص بك
2. افتح نافذة **Git Changes** بالنقر على أيقونة Git في شريط الحالة في الأسفل أو بالذهاب إلى **View > Git Changes**
3. في نافذة Git Changes، سترى الملفات المعدلة
4. أدخل رسالة التثبيت في مربع النص في الأعلى
5. انقر على **Commit All** لتثبيت جميع التغييرات، أو حدد ملفات معينة وانقر على **Commit Staged**

## 6. تجهيز التغييرات

### تجهيز ملفات أو تغييرات محددة

1. في نافذة **Git Changes**، سترى جميع الملفات المعدلة
2. لتجهيز ملفات محددة:
   - انقر على أيقونة **+** بجانب الملفات الفردية التي تريد تجهيزها
   - أو انقر بزر الماوس الأيمن على الملفات واختر **Stage**
3. لتجهيز أجزاء محددة من ملف:
   - انقر نقرًا مزدوجًا على الملف لفتح عرض المقارنة
   - حدد التغييرات التي تريد تجهيزها
   - انقر بزر الماوس الأيمن واختر **Stage Selected Lines**
4. ستنتقل الملفات المجهزة إلى قسم "Staged Changes"
5. أدخل رسالة التثبيت وانقر على **Commit Staged**

## 7. دفع التغييرات

### دفع التثبيتات إلى GitHub

1. بعد تثبيت التغييرات، سترى إشعارًا يوضح أن لديك تثبيتات صادرة
2. انقر على **Push** في نافذة Git Changes

بديلاً:
1. انظر إلى شريط الحالة الذي يعرض التثبيتات الصادرة (عادة كـ ↑ مع رقم)
2. انقر على مؤشر Git واختر **Push**
3. أو اذهب إلى **Git > Push**

## 8. إنشاء طلبات السحب

### إنشاء طلب سحب من Visual Studio

1. بعد دفع التغييرات إلى فرع، اذهب إلى **Git > Create Pull Request**
2. سيؤدي هذا إلى فتح صفحة طلب السحب على GitHub في متصفح الويب الخاص بك
3. املأ:
   - عنوان طلب السحب
   - وصف التغييرات
   - الفرع الأساسي (حيث تريد الدمج)
   - فرع المقارنة (الفرع الذي يحتوي على تغييراتك)
4. انقر على **Create Pull Request**

### عرض وإدارة طلبات السحب

1. اذهب إلى **Git > GitHub > Pull Requests**
2. ستفتح نافذة GitHub Pull Requests التي تعرض جميع طلبات السحب للمستودع
3. يمكنك التصفية حسب الحالة (مفتوح، مغلق، الكل) أو حسب طلبات السحب المعينة
4. حدد طلب سحب لـ:
   - عرض التفاصيل
   - إضافة تعليقات
   - الموافقة أو طلب التغييرات
   - إكمال طلب السحب (الدمج)

## 9. إنشاء وإدارة الفروع

### إنشاء فرع جديد

1. في الزاوية اليمنى السفلية من Visual Studio، سترى اسم الفرع الحالي
2. انقر على اسم الفرع لفتح قائمة الفروع
3. اختر **New Branch**
4. أدخل اسمًا للفرع الجديد
5. تحقق من **Checkout branch** للانتقال إليه فورًا
6. انقر على **Create**

### التبديل بين الفروع

1. انقر على اسم الفرع في شريط الحالة
2. اختر الفرع الذي تريد الانتقال إليه من القائمة المنسدلة
3. سيقوم Visual Studio تلقائيًا بفحص الفرع المحدد

### عرض جميع الفروع

1. اذهب إلى **View > Git Repository Window**
2. في نافذة المستودع، قم بتوسيع قسم **Branches**
3. سترى الفروع المحلية والبعيدة
4. انقر بزر الماوس الأيمن على أي فرع للحصول على خيارات إضافية

## 10. دمج الفروع

### دمج الفروع في Visual Studio

1. انتقل إلى الفرع الوجهة (الفرع الذي تريد الدمج فيه)
2. اذهب إلى **Git > Manage Branches**
3. انقر بزر الماوس الأيمن على الفرع المصدر (الفرع الذي تريد الدمج منه)
4. اختر **Merge '[source branch]' into '[destination branch]'**
5. إذا لم تكن هناك تعارضات، سيكتمل الدمج تلقائيًا
6. إذا كانت هناك تعارضات، انظر قسم [حل التعارضات](#12-حل-التعارضات)

## 11. تخزين التغييرات مؤقتاً

### تخزين التغييرات غير المثبتة مؤقتاً

1. مع وجود تغييرات غير مثبتة في دليل العمل الخاص بك، اذهب إلى **Git > Stashes > Stash All**
2. أدخل وصفًا للتخزين المؤقت (اختياري ولكن موصى به)
3. انقر على **Stash**

### تطبيق التغييرات المخزنة مؤقتاً

1. اذهب إلى **Git > Stashes > Manage Stashes**
2. في نافذة Stashes، سترى جميع التخزينات المؤقتة المحفوظة
3. انقر بزر الماوس الأيمن على تخزين مؤقت واختر:
   - **Apply** (يطبق التخزين المؤقت ولكن يحتفظ به في قائمة التخزين)
   - **Apply and Drop** (يطبق التخزين المؤقت ويزيله من القائمة)
   - **Drop** (يزيل التخزين المؤقت دون تطبيقه)

## 12. حل التعارضات

### التعامل مع تعارضات الدمج

1. عندما يحدث تعارض في الدمج، سيعرض Visual Studio إشعارًا
2. افتح نافذة **Git Changes**
3. سترى الملفات ذات التعارضات مدرجة تحت "Merge Changes"
4. انقر نقرًا مزدوجًا على ملف متعارض لفتح محرر الدمج
5. يعرض محرر الدمج:
   - **Source** (التغييرات من الفرع المصدر)
   - **Target** (التغييرات من الفرع الهدف)
   - **Result** (حيث تنشئ النسخة النهائية)
6. لكل تعارض:
   - انقر على **Take Left** لاستخدام تغيير المصدر
   - انقر على **Take Right** لاستخدام تغيير الهدف
   - انقر على **Take Both** لتضمين كلا التغييرين
   - أو قم بتحرير لوحة النتيجة يدويًا لإنشاء حل مخصص
7. بمجرد حل جميع التعارضات في ملف، انقر على **Accept Merge**
8. بعد حل جميع الملفات المتعارضة، قم بتثبيت الدمج

## نظرة عامة على ميزات GitHub في Visual Studio

### نافذة مستودع Git

توفر نافذة مستودع Git عرضًا شاملاً للمستودع الخاص بك:

1. اذهب إلى **View > Git Repository Window**
2. تعرض هذه النافذة:
   - الفروع (المحلية والبعيدة)
   - المستودعات البعيدة
   - العلامات
   - التخزينات المؤقتة
   - سجل التثبيتات
   - سجل الملفات للملفات المحددة

### نافذة تغييرات Git

نافذة تغييرات Git هي واجهتك الرئيسية للعمل مع Git:

1. اذهب إلى **View > Git Changes**
2. تعرض هذه النافذة:
   - التغييرات غير المثبتة
   - التغييرات المجهزة
   - إدخال رسالة التثبيت
   - حالة الدفع/السحب
   - معلومات الفرع

### ميزات تكامل GitHub

يوفر Visual Studio 2022 ميزات إضافية لـ GitHub:

1. **تكامل مشكلات GitHub**:
   - اذهب إلى **Git > GitHub > Issues**
   - إنشاء وعرض وإدارة مشكلات GitHub
   - ربط التثبيتات بالمشكلات

2. **سير عمل إجراءات GitHub**:
   - اذهب إلى **Git > GitHub > Actions**
   - عرض وإدارة سير عمل GitHub
   - مشاهدة حالة تشغيل الإجراء

3. **GitHub Codespaces**:
   - إنشاء والاتصال بـ GitHub Codespaces
   - تحرير الكود في بيئات قائمة على السحابة

## استكشاف الأخطاء الشائعة وإصلاحها

### مشكلات المصادقة

1. إذا كنت تواجه مشكلة في المصادقة مع GitHub:
   - اذهب إلى **Tools > Options > Source Control > GitHub**
   - انقر على **Clear All Credentials**
   - قم بتسجيل الدخول مرة أخرى

### فشل عمليات Git

1. لفشل عمليات Git العامة:
   - تحقق من نافذة الإخراج (**View > Output**) واختر "Git" من القائمة المنسدلة
   - ابحث عن رسائل خطأ محددة
   - تحقق من اتصالك بالإنترنت

### مشكلات أداء Git في Visual Studio

1. إذا كانت عمليات Git بطيئة:
   - اذهب إلى **Tools > Options > Source Control > Git > Performance**
   - اضبط الإعدادات مثل تكرار الجلب وفترة تحديث حالة المستودع
   - فكر في تمكين خيار "Disable source control for large repositories"

## أفضل الممارسات لـ Visual Studio وGitHub

1. **احتفظ بـ Visual Studio محدثًا**: غالبًا ما تتضمن الإصدارات الأحدث تكاملًا محسنًا مع Git
2. **استخدم مخطط Git المدمج**: قم بتصور سجل المستودع الخاص بك باستخدام نافذة مستودع Git
3. **استفد من تصور الفروع**: استخدم القائمة المنسدلة لاختيار الفرع لرؤية هيكل التفريع الخاص بك
4. **خصص نافذة تغييرات Git**: رتبها لسير عملك من خلال إرسائها حيث تفضل
5. **استخدم اختصارات لوحة المفاتيح**:
   - التثبيت: Ctrl+Enter من نافذة تغييرات Git
   - الدفع/السحب: Alt+P+P أو Alt+P+L من نافذة تغييرات Git
   - عرض التغييرات: Alt+G, C

## موارد إضافية

- [توثيق Visual Studio Git](https://learn.microsoft.com/en-us/visualstudio/version-control/git-with-visual-studio)
- [توثيق GitHub](https://docs.github.com/en)
- [امتداد Visual Studio GitHub](https://marketplace.visualstudio.com/items?itemName=GitHub.GitHubExtensionforVisualStudio)

---

يغطي هذا الدليل عمليات GitHub الأساسية باستخدام واجهة Visual Studio 2022 الرسومية. مع اكتسابك مزيدًا من الراحة مع هذه الأدوات، ستجد أن تكامل Git في Visual Studio يحسن سير عمل التطوير الخاص بك ويجعل التعاون من خلال GitHub أكثر كفاءة.