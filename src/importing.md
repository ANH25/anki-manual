# الاستيراد

<!-- toc -->

يستطيع أنكي استيراد الملفات النصية، وحزم الرزم المنشأة بميزة التصدير،
وملفات <span dir="ltr">.db</span> الخاصة بـ Mnemosyne 2.0،
وملفات <span dir="ltr">.xml</span> الخاصة بـ SuperMemo.
لاستيراد ملف، اضغط على قائمة ملف ثم «استيراد».

## الملفات النصية

يمكن استيراد أي **ملف نصي** يحتوي حقولًا مفصولة بفواصل، أو فواصل منقوطة، أو رموز tab،
إذا توفرت الشروط التالية.

- يجب أن تكون الملفات بصيغة نصية عادية (ملفي.txt). يجب تحويل الصيغ الأخرى مثل
     مثل ملفي.xls، أو ملفي.rtf، أو ملفي.doc إلى صيغة نصية أولًا.

- يجب أن تكون الملفات بصيغة UTF-8 (انظر في الأسفل).

- يحدد أنكي عدد الحقول في الملف بالنظر إلى السطر الأول (غير المذيَّل). يتم تجاهل
    أي سطور لها عدد مختلف من الحقول.

- يحدد السطر الأول أيضًا الرمز الفاصل - إذا وجد أنكي رمز «؛» في السطر الأول فسيستخدمه،
    وإذا وجد فاصلة فسيستخدمها، وهكذا دواليك.

يمكن إيزاع الحقول في الملف النصي إلى أي حقل في ملحوظاتك، بما في ذلك حقل الوسوم.
تستطيع اختيار ما يقابل كل حقل في الملف النصي من حقول الملحوظة عند الاستيراد.

عند استيراد ملف نصي، تستطيع اختيار الرزمة التي تريد وضع البطاقات فيها.
لاحظ أنه إذا كان خيار الرزمة المهيمنة مفعلًا لواحد أو أكثر من قوالبك، فستذهب البطاقات
إلى تلك الرزمة بدلًا من الرزمة التي حددتها.

هذا مثال عن ملف صالح:

    قطة لطيفة؛ كلب شرس؛ حصان قوي
    تفاح؛ موز؛ عنب

هناك طريقتان لتضمين رموز نهاية السطر في حقولك.

**أحط السطور المتعددة للحقل بأقواس اقتباس**:

    مرحبا؛ "هذا جواب
    مكون من سطرين"
    اثنان؛ هذا جواب مكون من سطر واحد

لأن علامات الاقتباس تُستخدم لتحديد بداية الحقل ونهايته، إذا أردت استخدامها داخل حقولك،
فعليك استبدال علامة الاقتباس المزودجة الواحدة باثنتين، كالتالي:

    الحقل الأول؛"الحقل الثاني "بعلامات اقتباس متجاهلة" داخله"

عند استخدام برنامج جدولة بيانات مثل Libreoffice لإنشاء ملف CSV، سيعالج البرنامج
علامات الاقتباس المزدوجة تلقائيًا.

**استخدم نهايات سطور HTML**:

    مرحبا؛ هذا<br>جواب مكون
    من سطرين؛ هذا جواب مكون من سطر

عليك تفعيل خيار «اسمح بـ HTML في الحقول» في نافذة الاستيراد لكي يعمل هذا.

لا تعمل السطور المتعددة بعلامات الاقتباس بشكل صحيح إذا كنت تستخدم عبارات ملء فراغات
تمتد عدة سطور. في هذه الحالة، استخدم نهايات سطور HTML بدلًا من ذلك.

تستطيع أيضًا تضمين الوسوم في حقل آخر وتحديده كحقل وسوم في نافذة الاستيراد:

    الحقل الأول؛ الحقل الثاني؛ الوسوم

هذا مثال عن ملف صالح بسطر أول مُتجاهَل (\#):

    # هذا تعليق يتم تجاهله
    شيء ما؛ فلان؛ شيء
    حقل 1؛ حقل 2؛ حقل 3

### جداول البيانات و UTF-8

إذا كان هناك حروف غير لاتينية في ملفاتك (مثل الحركات، الحروف اليابانية وما إلى ذلك)،
يتوقع أنكي أن تكون الملفات محفوظة بصيغة UTF-8. أسهل طريقة لتحقيق هذا هي باستخدام
برنامج جدولة البيانات المجاني LibreOffice بدلًا من Excel لتحرير الملف،
لأنه يدعم UTF-8 بسهولة، ويصدّر المحتوى متعدد السطور بشكل صحيح، عكس Excel.
إذا كنت تريد الاستمرار باستخدام Excel،
انظر [هذا المنشور](https://docs.google.com/document/d/12YE_FS6A9ANLTESJNtPP116ti4nNmCBghyoJBRtno_k/edit?usp=sharing)
لمزيد من المعلومات.

لحفظ جدول البيانات إلى ملف يستطيع أنكي قراءته، اذهب إلى ملف&lt;حفظ كـ، ثم اختر CSV
كنوع الملف. بعد قبول الخيارات الافتراضية، سيحفظ LibreOffice الملف وستستطيع عندها
استيراده إلى أنكي.

### HTML

يمكن لأنكي أن يعالج النص المستورد من الملفات النصية كـ HTML (اللغة المستخدمة لصفحات الويب).
يعني هذا أن النص الغامق، والمائل، والتنسيقات الأخرى يمكن تصديرها إلى ملف نصي واستيرادها مجددًا.
إذا كنت تريد تضمين تنسيق HTML، تستطيع تفعيل خيار «اسمح بـ HTML في الحقول» عند الاستيراد.
قد ترغب في إلغاء تفعيل هذا الخيار إذا كنت تستورد بطاقات تحتوي
على أقواس مثلثة &lt;&gt; أو صيغ HTML أخرى.

إذا كنت تريد استخدام HTML لتنسيق ملفك وتريد تضمين أقواس مثلثة أو واو العطف اللاتينية،
فيمكنك كتابتها بشكل مختلف:

| الحرف | البديل |
|-|-|
| &lt; | `&lt;` |
| &gt; | `&gt;` |
| &amp; | `&amp;` |

### استيراد الوسائط

إذا كنت تريد تضمين ملفات صوتية وصور من ملف نصي، انسخ الملفات إلى
[مجلد collection.media](files.md). **لا تنشئ مجلدات فرعية في مجلد الوسائط،
وإلا لن تعمل بعض الميزات.**

بعد نسخ الملفات، عدل حقلًا من الحقول في الملف النصي كالتالي:

<div dir="ltr">

    <img src="myimage.jpg">
</div>

أو

<div dir="ltr">

    [sound:myaudio.mp3]
</div>

كبديل، قد ترغب في استخدام ميزة [البحث والاستبدال](browsing.md) في نافذة المتصفح
لتحديث كل الحقول في الوقت نفسه. إذا كان كل حقل يحتوي على نص مثل "myaudio"،
وتريد جعله يشغل ملفًا صوتيًا، فستبحث عن (.\*) وتستبدله بـ "\[sound:\\1.mp3\]"
مع تفعيل خيار التعابير النمطية.

عند استيراد ملف نصي يحتوي على هذه المراجع، لا تنسَ تفعيل خيار السماح بـ HTML.

قد تُجذب إلى فعل شيء كهذا في قالب:

<div dir="ltr">

    <img src="{{اسم الحقل}}">
</div>

لا يدعم أنكي هذا لسببين: إن البحث عن الوسائط المستخدمة عملية مكلفة، حيث يجب معالجة
كل بطاقة، وميزة كهذه ليست واضحة لمستخدمي الرزم المشتركة. الرجاء استخدام
ميزة البحث والاستبدال بدلًا من ذلك.

### وسائط بالجملة

خيار آخر لاستيراد عدد كبير من الوسائط هو استخدام
[إضافة استيراد الوسائط](https://ankiweb.net/shared/info/1531997860).
تنشئ هذه الإضافة ملحوظات تلقائيًا لكل الملفات في مجلد تحدده، بأسماء الملفات في الجانب الأمامي
(ما عدا لاحقة الملف، لذلك إذا كان لديك ملف باسم تفاحة.jpg، فسيحتوي الجانب الأمامي على «تفاحة»)
والصور أو الملفات الصوتية في الجانب الخلفي. إذا كنت تريد ترتيبًا مختلفًا للوسائط وأسماء الملفات،
تستطيع [تغيير نوع ملحوظة](browsing.md) البطاقات بعد إنشائها.

### إضافة الوسوم

إذا كنت تريد إضافة وسوم «وسم 1» و «وسم 2» لكل سطر تستورده، أضف التالي أعلى الملف النصي:

<div dir="ltr">

    tags:tag1 tag2
</div>

### الملحوظات المكررة والتحديث

عند استيراد الملفات النصية، يستخدم أنكي الحقل الأول للتحقق مما إذا كانت الملحوظة فريدة.
بشكل افتراضي، إذا كان للملف الذي تستورده حقل أول يطابق ملحوظة من الملحوظات الموجودة
في مجموعتك ولتلك الملحوظة النوع نفسه الذي تستورده، فسيتم تحديث حقول هذه الملحوظة
بناءً على محتوى الملف المستورد. يسمح لك صندوق منسدل في نافذة الاستيراد بتغيير هذ السلوك،
لتجاهل الملحوظات المكررة تمامًا، أو استيرادها كملحوظات جديدة بدلًا من تحديث الملحوظات الموجودة.

يُجرى فحص الملحوظات المكررة في كل مجموعتك، وليس فقط في الرزمة الحالية.
إذا أشار أنكي إلى أن البطاقات لم تتغير بينما كنت تتوقع أن يتم استيرادها، تحقق من
أن الملحوظات ليست موجودة من قبل في مجموعتك في مكان ما.

إذا كان خيار تحديث الملحوظات مفعلًا وهناك نسخ قديمة من الملحوظات التي تستوردها
في مجموعتك، فسيتم تحديثها في مكانها (في رزمها الحالية) بدلًا من نقلها إلى الرزمة
التي حددتها في نافذة الاستيراد. إذا حُدِّثت الملحوظات في مكانها، ستُحفَظ معلومات الجدولة
لكل بطاقات هذه الملحوظات.

لمعلومات حول كيفية معالجة الملحوظات المكررة في ملفات <span dir="ltr">.apkg</span>،
انظر قسم [حزم الرزم](exporting.md#حزم-الرزم).
