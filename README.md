# TypeScript-Lesson

# مقدمة في TypeScript





لقد اصبحت لغة TypeScript واحده من اشهر اللغات في السنوات الاخيره ، في حال كان لديك معرفة بلغة JavaScript سيكون من السهل تعلم TypeScript.
سوف نتعلم في هذا الدرس :


- لماذا نتعلم  TypeScript؟
- ماهي فوائد استخدامه ؟
- ماهي طريقة استخدامه ؟
- كيفية التعامل معه وانشاء ملف ts
- انواع البيانات الموجوده 
- كيفية انشاء مشروع TypeScript



## ماهو TypeScript؟

تقوم لغة TypeScript بكل ماتقوم به لغة JavaScript لكن مع إضافة بعض المميزات ،فلقد تم بناء لغة TypeScript فوق  JavaScript.  السبب الرئيسي لإستخدام TypeScript هو اضافة الصرامة الى الكود البرمجي فكما نلاحظ عند كتابة متغير مثلًا بالـJavaScript فنحن لا نقوم بتحديد نوع المدخل فقط نقوم بكتابة المتغير فلغة JavaScript تعتبر   dynamically typed language
هذا يعني انه يمكن تغيير قيمة نوع المدخل .
مثال :


    let name = "Mohammed"
    name = 33

كما نلاحظ هنا قمنا بتعريف المتغير واسناد قيمة من النوع string وهي اسم  Mohamed ومن ثم قمنا بتغير قيمته الى متغير من النوع Number ! لقد سمحت لنا لغة JavaScript بتغيير نوع القيمة المدخلة لكن  استخدام TypeScript يمنع هذا النوع من الإدخال . يفرض علينا TypeScript تحديد نوع المدخل المراد ادخاله 

مثال :

    let name:string = name
    name = 33 // ERROR name cannot change from string to number

وكما نلاحظ قمنا بتحديد نوع المدخل وهو من نوع string  وفي هذه الحاله لن يقبل المتغير اي نوع اخر من البيانات ، وبهذا يتم ضمان انه لن يتم تغيير القيمه المدخله من قبل المستخدم.

*ملاحظه: لايمكن قراءة TypeScript من قبل المتصفحات لذا تلجأ الى استخدام TypeScript Compiler (TSC) فيقوم إرجاع كود TypeScript الى JavaScript

ـــــــــــــــــــــــــــــــــــــــــــــــــــــــــــ


## لماذا نقوم بإستخدام TypeScript؟


- اكتشفت الآبحاث ان استخدام TypeScript يمكنه اكتشاف 15٪ من الأخطاء الشائعة.
- قابلية القراءة - من الأسهل أن ترى ما الذي يفترض أن تفعله في الكود. وعند العمل ضمن فريق ، يكون من الأسهل رؤية ما ينوي المطورون الآخرون تحقيقه.
- إنه شائع - معرفة أن TypeScript سيمكنك من التقدم إلى المزيد من الوظائف الجيدة.
- سوف يمنحك تعلم TypeScript فهماً أفضل ومنظوراً جديداً لجافا سكريبت.


## عيوب TypeScript:
- يستغرق TypeScript وقتًا أطول في الكتابة من JavaScript ، حيث يتعين عليك تحديد الأنواع ، لذلك قد لا يكون من المفيد استخدامه للمشاريع الفردية الصغيرة.
- يجب ان يتم تحويل الكود الى  JavaScript  حتى تستطيع المتصفحات قراءته

لكن الوقت الإضافي الذي يجب أن تقضيه في كتابة تعليمات برمجية أكثر دقة وتجميعها سيكون أكثر من توفيره من خلال عدد الأخطاء القليلة الموجودة في التعليمات البرمجية الخاصة بك.
بالنسبة للعديد من المشاريع - خاصة المشاريع المتوسطة إلى الكبيرة - سيوفر لك TypeScript الكثير من الوقت


## كيفية إعداد مشروع TypeScript:

 اولًا يجب التآكد من وجود بيئة العمل Node.js ولتحقق من ذالك سوف نقوم بالذهاب الى الـTerminal الخاص بنا وكتابة الآمر 

     node -v

في حال وجود node.js سوف يقوم بطباعة النسخه المتوفره بالجهاز 
في حال عدم توفرها فيجب علينا تحميل Node.js من خلال https://nodejs.org/en/download/

 من ثم نقوم بتحمل TypeScript من خلال الامر 

     npm i -g typescript

حيث انها حزمة من حزم Node.js ولهذا يجب علينا التأكد من وجود بيئة العمل Node.js في الجهاز 
وفي حال اردنا التأكد من تجاح التحميل نقوم بكتابة الامر التالي :


    tsc -v

*ملاحظه : في حال حدوث مشكلة بجهاز من نوع Mack  او كنت تستخدم نظام linex نقوم بكتابة كلمة sudoقبل الامر 

    sudo npm i -g typescript

ومن ثم سيقوم بطلب ادخال الرقم سري الخاص بجهازك من ثم سوف يقوم بتحمل الحزمة

## كيفية تشغيل ملف TypeScript


- اولًا : سوف نقوم بفتح محرر الآكواد المستخدم ، في حالتنا هنا سوف نقوم بالعمل مع محرر الأكواد visual studio

 ومن ثم سوف نقوم بإنشاء ملف بصيغة TypeScript ، index.ts
 وكتابة الامر 

    let name = "Mohammed"
    let id = 5;

وحتى نقوم بتحويل الكود من TypeScript الى JavaScript نقوم بكتابة الامر التالي 


    tsc index

سوف يقوم هذا الأمر بإنشاء ملف جديد بصيغة index.js وذالك لتقوم المتصفحات بقراءة الكود البرمجي فكما وضحنا سابقًا ان المتصفحات لا تستطيع قراءة TypeScript فيجب تحويلها اولًا الى صيغة JavaScript

في حال اردت من المحرر تحويل كودك الى JavaScript بشكل تلقائي قم بإستخدام الأمر 

     tsc index.ts -w

ملاحظه* : في حال وجود مشكله وظهور cannot redeclare block-scoped variable

نقوم بكتابة export {} في نهاية الكود .

واحده من اهم المميزات لإستخدام TypeScript هو إظهارها لرسائل الخطأ .

مثال :

    let id = 5;
    id = "5"; // Error: Type 'string' is not assignable to 
    type 'number'.

لقد تم التعرف من خلال اول قيمة تم ادخالها وهي الرقم 5 ان المتغير يستقبل بيانات من النوع Number ، وعند قيامنا بمحاولة تغييره تم رفض ذالك .

لكن عند الذهاب الى ملف index.js سنجد انه تم بالفعل كتابة الكود بدون اي مشاكل ، لقد سمحت لنا لغة JavaScript بالتغيير على نوع البيانات وهذه احد المشاكل اللتي قامت لغة TypeScript بحلّها .


## كيفية إعداد ts config File

يجب ان يكون ملف الـconfig في نفس مسار المشروع 

اولًا نقوم بكتابة الأمر 

    tsc --init

 
 سوف نلاحظ ظهور ملف جديد يحمل الإسم tsconfig.json 
 وهو المسؤول عن اعدادات المشروع 
 
 سوف نلاحظ عند القيام بالدخول للملف بعض الخيارات 
 مثل:
 

       /* Modules */
        "module": "commonjs",                                /* Specify what module code is generated. */
        // "rootDir": "./",                                  /* Specify the root folder within your source files. */
        // "moduleResolution": "node",                       /* Specify how TypeScript looks up a file from a given module specifier. */
        // "baseUrl": "./",                                  /* Specify the base directory to resolve non-relative module names. */
        // "paths": {},                                      /* Specify a set of entries that re-map imports to additional lookup locations. */
        // "rootDirs": [],                                   /* Allow multiple folders to be treated as one when resolving modules. */
        // "typeRoots": [],                                  /* Specify multiple folders that act like './node_modules/@types'. */
        // "types": [],                                      /* Specify type package names to be included without being referenced in a source file. */
        // "allowUmdGlobalAccess": true,                     /* Allow accessing UMD globals from modules. */
        // "moduleSuffixes": [],                             /* List of file name suffixes to search when resolving a module. */
        // "resolveJsonModule": true,                        /* Enable importing .json files. */
        // "noResolve": true,  

فمثلًا نلاحظ ان مسار المشروع ليس بداخل ملف لكن بإمكاننا انشاء ملف جديد بإسم src ووضع ملفات مشروعنا بداخله وسوف نقوم بتغيير المسار الى :

    "rootDir": "./src", // Where to compile from

لمتابعة التغيرات التي تحدث في المشروع 

    tsc -w


## المتغيرات في الـTypeScript

١- الأنواع البدائية **Primitive types**
-في الـJavaScript لدينا 7 انواع 

- string
- number
- bigint
- boolean
- undefined
- null
- symbol

 
 في هذه الانواع عند استخدام قيمة اوليه معها فإنه لايمكن تغيير قيمتها ،من المهم عدم الخلط بين البدائية نفسها مع المتغير المعين له قيمة أولية.
 يمكن إعادة تعيين قيمة جديدة للمتغير ، ولكن لا يمكن تغيير القيمة الحالية بالطرق التي يمكن بها تغيير الكائنات والمصفوفات والوظائف.
 

##  مثال:


    let name = 'Mohammed';
    name.toLowerCase();
    console.log(name); // Mohammed - the string method didn't mutate the string
    
    let arr = [1, 3, 5, 7];
    arr.pop();
    console.log(arr); // [1, 3, 5] - the array method mutated the array
    
    name = 'Ali' // Assignment gives the primitive a new (not a mutated) value

بالعودة إلى TypeScript ، يمكننا تعيين النوع الذي نريد أن يقوم المتغير بإضافته: type (يسمى "type annotation" أو "type signature" (توقيع النوع) بعد التصريح عن متغير.


    let id: number = 5;
    let firstname: string = "Mohammed";
    let hasCat: boolean = true;
    let unit: number; // Declare variable without assigning a value
    unit = 5;
    

لكن من الأفضل عادةً عدم ذكر النوع صراحةً ، لأن TypeScript يستنتج تلقائيًا نوع المتغير (نوع الاستدلال) :


    let id = 5; // TS knows it's a number
    let firstname = 'Mohammed'; // TS knows it's a string
    let hasCat = true; // TS knows it's a boolean
    
    hasCat = 'yes'; // ERROR

يمكننا أيضًا تعيين متغير ليكون نوعًا موحدًا ( **A union type**). نوع الاتحاد هو متغير يمكن تعيين أكثر من نوع واحد له :


    let age: string | number;
    age = 27;
    age = '27';


## أنواع المراجع  Reference Types

في الـJavaScript  تقريبًا كل شي عبارة عن كائن ونستطيع القول ايضًا ان آنواع البيانات مثل : string و number و boolean تستطيع ان تكون  كائنات إذا تم تعريفها باستخدام الكلمة الأساسية الجديدة:


    let firstname = new String('Mohammed');
    console.log(firstname); // String {'Mohammed'}

ولكن عندما نتحدث عن أنواع المراجع في JavaScript ، فإننا نشير إلى المصفوفات والكائنات والوظائف.


## الأنواع المرجعية VS الأنواع البدائية :

لنناقش الإختلاف  الأساسي بين هذين النوعين :
إذا تم تخصيص نوع بدائي لمتغير ، فيمكننا التفكير في هذا المتغير على أنه يحتوي على القيمة الأولية. يتم تخزين كل قيمة بدائية في مكان فريد في الذاكرة.
إذا كان لدينا متغيرين ، x و y ، وكلاهما يحتوي على بيانات أولية ، فسيكونان مستقلين تمامًا عن بعضهما البعض
 

    let x = 2;
    let y = 1;
    
    x = y;
    y = 100;
    console.log(x); // 1 (even though y changed to 100, x is still 1)

هذا ليس هو الحال مع أنواع المراجع. تشير أنواع المراجع إلى موقع الذاكرة حيث تم تخزين الكائن.


    let point1 = { x: 1, y: 1 };
    let point2 = point1;
    
    point1.y = 100;
    console.log(point2.y); // 100 (point1 and point2 refer to the same memory address where the point object is stored)



## المصفوفات في TypeScript

في المصفوفات مع استخدام TypeScript بإمكاننا تحديد نوع البيانات التي يمكن ان تحتويها المصفوفه .


    let ids: number[] = [1, 2, 3, 4, 5]; // can only contain numbers
    let names: string[] = ['Mohammed', 'Ali', 'Noura']; // can only contain strings
    let options: boolean[] = [true, false, false]; can only contain true or false
    let books: object[] = [
      { name: 'Fooled by randomness', author: 'Nassim Taleb' },
      { name: 'Sapiens', author: 'Yuval Noah Harari' },
    ]; // can only contain objects
    let arr: any[] = ['hello', 1, true]; // any basically reverts TypeScript back into JavaScript
    
    ids.push(6);
    ids.push('7'); // ERROR: Argument of type 'string' is not assignable to parameter of type 'number'.

يمكنك استخدام أنواع الاتحاد (union types) لتعريف المصفوفات التي تحتوي على أنواع متعددة:


    let person: (string | number | boolean)[] = ['Mohammed', 1, true];
    person[0] = 100;
    person[1] = {name: 'Mohammed'} // Error - person array can't contain objects
    


اذا قمنا بإنشاء ملف يحمل صيغة ts فليس من الضروري تحديد نوع المدخل لأنه سوف يقوم بالتعرف عليه 


## مثال : 
    let person = ['Mohammed', 1, true]; // This is identical to above example
    person[0] = 100;
    person[1] = { name: 'Mohammed' }; // Error - person array can't contain objects

يوجد نوع خاص من المصفوفات التي يمكن تحديدها في TypeScript: Tuples.  هو مصفوفة ذات حجم ثابت وأنواع بيانات معروفة. هم أكثر صرامة من المصفوفات العادية.


    let person: [string, number, boolean] = ['Mohammed', 1, true];
    person[0] = 100; // Error - Value at index 0 can only be a string


## الـكائنات في TypeScript

يجب أن تحتوي الكائنات في TypeScript على جميع الخصائص وأنواع القيم الصحيحة:


    // Declare a variable called person with a specific object type annotation
    let person: {
      name: string;
      location: string;
      isProgrammer: boolean;
    };
    
    // Assign person to an object with all the necessary properties and value types
    person = {
      name: 'Mohammed',
      location: 'KSA',
      isProgrammer: true,
    };
    
    person.isProgrammer = 'Yes'; // ERROR: should be a boolean
    
    
    person = {
      name: 'Ali',
      location: 'KSA',
    }; 
    // ERROR: missing the isProgrammer property

عند تحديد توقيع كائن ما ، ستستخدم عادةً واجهة (**interface**). هذا مفيد إذا احتجنا إلى التحقق من أن كائنات متعددة لها نفس الخصائص وأنواع القيم المحددة:


    interface Person {
      name: string;
      location: string;
      isProgrammer: boolean;
    }
    
    let person1: Person = {
      name: 'Mohammed',
      location: 'KSA',
      isProgrammer: true,
    };
    
    let person2: Person = {
      name: 'Ali',
      location: 'KSA',
      isProgrammer: false,
    };



## الوظائف (Functions) في TypeScript

يمكننا تحديد ماهي الانواع اللتي سوف تُمرر للدالة ومن ثم إعادة نوع الدالة نفسها.


    // Define a function called circle that takes a diam variable of type number, and returns a string
    function circle(diam: number): string {
      return 'The circumference is ' + Math.PI * diam;
    }
    
    console.log(circle(10)); // The circumference is 31.41592653589793

فكما نلاحظ اننا مررنا  المدخل diam (قُطر) وحددنا انهُ من النوع number ومن ثم قمنا بتحديد نوع الدالة نفسها وهو عبارة عن string .

ونستطيع كتابة الدالة على طريقة ES6 او ماتسمى arrow function:


    const circle = (diam: number): string => {
      return 'The circumference is ' + Math.PI * diam;
    };
    
    console.log(circle(10)); // The circumference is 31.41592653589793

لكن ماذا لو لم يتم تحديد نوع للدالة نفسها ؟ يقوم TypeScript بالتعرف مباشرة على ان الدالة تقوم بإرجاع قيمة تحمل النوع string  ، نستطيع ايضًا كتابة circle دون الحاجه للتصريح مباشرة بأنها دالة .


## مثال :
    // Using explicit typing 
    const circle: Function = (diam: number): string => {
      return 'The circumference is ' + Math.PI * diam;
    };
    
    // Inferred typing - TypeScript sees that circle is a function that always returns a string, so no need to explicitly state it
    const circle = (diam: number) => {
      return 'The circumference is ' + Math.PI * diam;
    };

احيانًا نقوم بتمرير اكثر من مُدخل للدالة لكن لا نقوم بإستخدامه ، عند استخدامنا TypeScript فإنه يفرض استخدام جميع البيانات الممرره للداله في هذه الحالة نستطيع كتابة علامة استفهام لجعلها اختياريه .


## مثال :
    const add = (a: number, b: number, c?: number | string) => {
      console.log(c);
    
      return a + b;
    };
    
    console.log(add(5, 4, 'I could pass a number, string, or nothing here!'));
    // I could pass a number, string, or nothing here!
    // 9

كما نلاحظ اننا قمنا بتمرير ثلاث معاملات للدالة وهي ( a , b , c ) ووضعنا علامة استفهام بعد المعامل c لجعله اختياري ففي حال ازلنا الجملة 'I could pass a number, string, or nothing here!' فسيقوم TypeScript بإظهار رسالة تحمل Error تُفيد بأنه يجب علينا تمرير مدخل ثالث لكن مع علامة الإستفهام استطعنا حل هذه المشكلة.

هناك ايضًا دوال لا تُعيد لنا اي مخرج في هذه الحالة فإن الدالة سوف تحمل النوع void .

مثال :


    const logMessage = (msg: string): void => {
      console.log('This is the message: ' + msg);
    };
    
    logMessage('TypeScript is superb'); // This is the message: TypeScript is superb



## النوع any :

يُستخدم النوع any لإستقبال جميع انواع المدخلات من المتغير وبهذا نعيده الى الحالة الاصليه وهي JavaScript

كما ذكرنا سابقًا ان JavaScript تستقبل جميع الانواع للمتغير دون تحديد وحين استخدامنا للنوع any في TypeScript فإننا نساويه بالجافا سكريبت .


## مثال : 
    let age: any = '100';
    age = 100;
    age = {
      years: 100,
      months: 2,
    };

فكما نلاحظ قمنا في المرة الأولى بإدخال قيمة من النوع string ومن ثم قمنا بتغيير نوعها الى number  وفي الحالة الثالثه قمنا بتغييرها الى object لقد سمح لنا النوع any بتغيير نوع المتغير age دون اي مشاكل كما يحدث عند استخدامنا JavaScript .

*ملاحظه : يوصى بتجنب استخدام النوع any  بقدر ما تستطيع ، لأنه يمنع TypeScript من أداء وظيفته - ويمكن أن يؤدي إلى أخطاء.


## النوع Aliases :

يمكن أن يقلل النوع Aliases من تكرار الكود ، مما يحافظ على نظافة الكود الخاص واختصاره .


## مثال :


    type StringOrNumber = string | number;
    
    type PersonObject = {
      name: string;
      id: StringOrNumber;
    };
    
    const person1: PersonObject = {
      name: 'John',
      id: 1,
    };
    
    const person2: PersonObject = {
      name: 'Delia',
      id: 2,
    };
    
    const sayHello = (person: PersonObject) => {
      return 'Hi ' + person.name;
    };
    
    const sayGoodbye = (person: PersonObject) => {
      return 'Seeya ' + person.name;
    };

كما نرى انه تم حفظ الانواع بمكان واحد بداخل PersonObject ومن ثم استخدامها لاحقًا بداخل الكائن وبهذه الطريقه استطعنا اختصار الكود الخاص بنا وتقليل الكتابة .


## الـDOM and type casting

لا يمتلك TypeScript حق الوصول إلى DOM مثل JavaScript. هذا يعني أنه عندما نحاول الوصول إلى عناصر DOM ، لا يكون TypeScript متأكدًا أبدًا من وجودها بالفعل.


## مثال :
    const link = document.querySelector('a');
    
    console.log(link.href); // ERROR: Object is possibly 'null'. TypeScript can't be sure the anchor tag exists, as it can't access the DOM

ومع المتغير الذي لا يساوي قيمته null (!) يمكننا إخبار المترجم صراحة أن التعبير له قيمة أخرى غير القيمة الفارغة أو غير المحددة.  (`null` or `undefined`) .
يمكن أن يكون هذا مفيدًا عندما لا يتمكن المترجم من استنتاج النوع على وجه اليقين .


    // Here we are telling TypeScript that we are certain that this anchor tag exists
    const link = document.querySelector('a')!;
    
    console.log(link.href); 

نلاحظ كيف لم يكن علينا تحديد نوع المتغير . هذا لأن TypeScript يمكنه أن يرى بوضوح (عبر  Type Inference) أنه من النوع HTMLAnchorElement.

ولكن ماذا لو احتجنا إلى تحديد عنصر DOM من خلال صنفه ؟ لا يمكن لـ TypeScript الاستدلال على النوع ، حيث يمكن أن يكون أي شيء.


## مثال :


    const form = document.getElementById('signup-form');
    
    console.log(form.method);
    // ERROR: Object is possibly 'null'.
    // ERROR: Property 'method' does not exist on type 'HTMLElement'.

نلاحظ انه لدينا نوعين من الخطأ لذا يجب اخبار TypeScript بأننا نقوم ببناء شكل  واننا نعلم انه من النوع HTMLFormElement


    const form = document.getElementById('signup-form') as HTMLFormElement;
    
    console.log(form.method); // post

نستطيع ايضًا استخدام خصائص DOM مثل addEventListener

## مثال :
    const form = document.getElementById('signup-form') as HTMLFormElement;
    
    form.addEventListener('submit', (e: Event) => {
      e.preventDefault(); // prevents the page from refreshing
    
      console.log(e.tarrget); // ERROR: Property 'tarrget' does not exist on type 'Event'. Did you mean 'target'?
    });


## الواجهه Interfaces in TypeScript

تحدد الواجهات كيف يجب أن يبدو الـ object  : 

## مثال:


    interface Person {
      name: string;
      age: number;
    }
    
    function sayHi(person: Person) {
      console.log(`Hi ${person.name}`);
    }
    
    sayHi({
      name: 'Mohammed',
      age: 22,
    }); // Hi Mohammed


كما نلاحظ لقد اخبرنا المدخل person ان قيمته تساوي ماتحتويه قيمة interface وبهذه الطريقه يمكننا استخدامه اكثر من مره وفي اكثر من مكان .

تشابه interface النوع aliases بشكل كبير .


## النوع aliases مقارنة بالنوع interface :

يمكن استخدام كلاهما للإعلان عن شكل الـobject. نظرًا لأن TypeScript هو نظام كتابة هيكلي .


    type BirdType = {
      wings: 2
    }
    
    interface BirdInterface {
      wings: 2
    }
    
    const bird1: BirdType = {wings: 2}
    const bird2: BirdInterface = {wings: 2}
    const bird3: BirdInterface = bird1


## Declaration merging (interface only)

يتمثل أحد الاختلافات الرئيسية بين الأسماء المستعارة للنوع مقابل الواجهات في أن الواجهات مفتوحة وأن الأسماء المستعارة للكتابة مغلقة. هذا يعني أنه يمكنك توسيع الواجهة بالتصريح عنها عدة مرات ، وسيتم التعامل معها كواجهة واحدة (مع دمج أعضاء جميع التعريفات).


## مثال :
    interface Point {
      x: number
    }
    interface Point {
      y: number
    }
    const point: Point = {x: 1, y: 2}

نلاحظ اننا استطعنا استخدام interface اكثر من مرة مع نفس الإسم دون ظهور اي مشاكل،اما بالنسبة لـtype لايمكننا استخدام نفس الاسم اكثر من مرة 


## مثال :


    type Puppy = {
      color: string
    }
    
    type Puppy = {
      toys: number
    }
    
    // Error: duplicate identifier Puppy



## الأنواع الحرفية  TypeScript ( **Literal types**)


    // Union type with a literal type in each position
    let favouriteColor: 'red' | 'blue' | 'green' | 'yellow';
    
    favouriteColor = 'blue';
    favouriteColor = 'crimson'; // ERROR: Type '"crimson"' is not assignable to type '"red" | "blue" | "green" | "yellow"'.


مصدر : https://www.typescriptlang.org/docs/handbook/typescript-in-5-minutes.html

