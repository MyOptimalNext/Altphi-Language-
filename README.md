# **Altphi Language Documentation**  

Altphi هي لغة برمجة مصممة خصيصًا للأبحاث الفيزيائية والحسابات العلمية. توفر بيئة مرنة للباحثين للعمل مع الثوابت الفيزيائية والمعادلات والمحاكاة، مع الحفاظ على فصل واضح بين **منطق الكود** و**البيانات الفيزيائية**.  

---

## **Table of Contents**  
1. [**Overview**](#overview)  
2. [**Key Features**](#key-features)  
3. [**Standard Libraries**](#standard-libraries)  
4. [**Data Files**](#data-files)  
5. [**Basic Syntax**](#basic-syntax)  
6. [**Importing Libraries and Data**](#importing-libraries-and-data)  
7. [**How to Contribute**](#how-to-contribute)  
8. [**License**](#license)  

---

## **Overview**  

Altphi هي لغة برمجة تهدف إلى تبسيط وتسريع تطوير المحاكاة الفيزيائية والحسابات العلمية. تدعم مجالات متعددة من الفيزياء مثل:  

- **الميكانيكا** (كلاسيكية، نسبية، كمية)  
- **الكهرومغناطيسية** (الكهرباء، الضوء)  
- **الظواهر الموجية** (الصوت، الضوء)  
- **التطبيقات العلمية** (الكيمياء، الفلك، البلازما، الفيزياء النووية)  
- **أدوات الرسوميات والمحاكاة** (2D/3D)  

Altphi تفصل بين **مكتبات الكود** و**ملفات البيانات الفيزيائية** لضمان دقة الحسابات وسهولة تحديث الثوابت الفيزيائية دون الحاجة إلى تعديل الكود البرمجي نفسه.  

---

## **Key Features**  
✅ لغة مفسرة مصممة خصيصًا للفيزياء والعلوم.  
✅ فصل صارم بين الكود والثوابت الفيزيائية.  
✅ مكتبات قياسية متخصصة لكل فرع من فروع الفيزياء.  
✅ دعم للوحدات الفيزيائية مباشرة في الكود.  
✅ إمكانية تخصيص البيانات الفيزيائية دون تغيير الكود.  

---

## **Standard Libraries**  

تشمل Altphi مجموعة من المكتبات القياسية التي تغطي مختلف المجالات الفيزيائية. هذه المكتبات تحتوي على دوال وثوابت معرفة مسبقًا:  

### **.alt Libraries (Libraries for Computation)**  

| Library               | Description                    |  
|----------------------|--------------------------------|  
| **chemis.alt**       | Chemistry library             |  
| **electric.alt**     | Electric phenomena library    |  
| **light.alt**        | Light and optics library      |  
| **sound.alt**        | Sound and acoustics library   |  
| **astro.alt**        | Astronomy library             |  
| **plasma.alt**       | Plasma physics library        |  
| **nuclear.alt**      | Nuclear physics library       |  
| **mechanic_classic.alt**  | Classical mechanics library  |  
| **mechanic_relativ.alt**  | Relativity mechanics library  |  
| **mechanic_quantum.alt**  | Quantum mechanics library  |  
| **3dgraph.alt**      | 3D graphing library           |  
| **2dgraph.alt**      | 2D graphing library           |  
| **3dsimulated.alt**  | 3D simulation library        |  

---

## **Data Files**  

في Altphi، يتم فصل البيانات الفيزيائية عن الكود في **ملفات بيانات مستقلة** لضمان دقة الحسابات.  

### **.apd Data Files (Physical Constants & Units)**  

| Data File              | Description                        |  
|----------------------|--------------------------------|  
| **chemis.apd**       | Chemistry constants            |  
| **electric.apd**     | Electric constants            |  
| **light.apd**        | Light-related constants       |  
| **sound.apd**        | Sound-related constants       |  
| **astro.apd**        | Astronomical constants       |  
| **plasma.apd**       | Plasma constants              |  
| **nuclear.apd**      | Nuclear constants             |  
| **mechanic_classic.apd** | Classical mechanics constants  |  
| **mechanic_relativ.apd** | Relativity constants         |  
| **mechanic_quantum.apd** | Quantum constants            |  
| **units.apd**        | Physical units data           |  

---

## **Basic Syntax**  

تتميز Altphi ببنية واضحة وبسيطة، مناسبة للباحثين في المجالات العلمية.  

### **تعريف دالة:**
```altphi
function Energy_calc => E {
  mass = 12 Kg;
  return mass * c^2;  # استخدم ثابت سرعة الضوء مباشرة
}
```
c هو ثابت سرعة الضوء، يتم تعريفه تلقائيًا في **light.apd** ولا يمكن تغييره أو إعادة تعريفه داخل الكود.  

في Altphi، **الثوابت الفيزيائية والوحدات المعرفة مسبقًا لا يمكن استخدامها كمتغيرات**، مما يضمن الدقة ويحمي البيانات الفيزيائية من التعديل غير المقصود.  

---

## **Importing Libraries and Data**  

لاستخدام مكتبات الفيزياء والبيانات الفيزيائية في البرنامج، يجب استيرادها كما يلي:  

```altphi
import phy_relativ.alt
import units.apd
import phy_relativ.apd
```
- **phy_relativ.alt** → مكتبة الفيزياء النسبية، تحتوي على وظائف متخصصة لحسابات النسبية الخاصة والعامة، مثل تحويلات لورنتز وحساب تمدد الزمن.  
- **units.apd** → ملف بيانات الوحدات الفيزيائية، يشمل تعريفات دقيقة للوحدات مثل المتر، الثانية، الكيلوجرام، وغيرها، مما يضمن الدقة في الحسابات.  
- **phy_relativ.apd** → ملف الثوابت الفيزيائية المتعلقة بالنسبية، يتضمن القيم المعرفة عالميًا مثل سرعة الضوء وثابت بلانك وثابت الجاذبية.  

---

## **How to Contribute**  

نرحب بجميع المساهمات في تطوير Altphi! سواء كنت ترغب في **إضافة مكتبات جديدة، تحسين التوثيق، أو تحسين الأداء**، يمكنك المساهمة عبر الخطوات التالية:  

1. **قم بعمل فورك للمستودع** (Fork the repository).  
2. **أنشئ فرعًا جديدًا** (`git checkout -b feature-name`).  
3. **قم بإجراء التعديلات واحفظها** (`git commit -am 'Add new feature'`).  
4. **ادفع الفرع إلى المستودع** (`git push origin feature-name`).  
5. **افتح طلب سحب (Pull Request)** ليتم مراجعته من قبل الفريق والموافقة عليه.  

> **ملاحظة:** كل تعديل يجب أن يمر عبر **طلب سحب (Pull Request)** ويتم **مراجعته بدقة** قبل الدمج لضمان جودة الكود.  

---

## **License**  

Altphi Language مرخصة بموجب **نفس رخصة Python**.  
لمزيد من التفاصيل، راجع **رخصة مؤسسة Python Software Foundation**.  

---

## **Developed by OPTINEX**  

**Lead Developer:** Loukmane Hadj Said  
For inquiries and contributions, contact us via GitHub.
