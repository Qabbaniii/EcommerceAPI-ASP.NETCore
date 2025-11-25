# eCommerce API

هذا المشروع عبارة عن **eCommerce API** مبني باستخدام ** Onion Architecture** .

---

## بنية المشروع (Clean / Onion Architecture)

```
ECommerceApiSolution/
├── Core/
│ ├── ECommerce.Abstraction/ # الواجهات والعقود Contracts
│ ├── ECommerce.Domain/ # الكيانات Entities والمنطق الأساسي
│ └── ECommerce.Service/ # الخدمات والخدمات المشتركة
│
├── Infrastructure/
│ ├── ECommerce.Persistence/ # الاتصال بقاعدة البيانات + EF Core
│ └── ECommerce.Presentation/ # الطبقة التي تربط الـ API مع الـ Core
│
├── ECommerce.Shared/ # الأكواد المشتركة بين الطبقات
├── ECommerce.Web/ # طبقة الـ API (Controllers, Endpoints)
└── Solution Items/ # ملفات الحل العام
```

---

## تشغيل المشروع على أي جهاز

### 1 المتطلبات الأساسية

* .NET 9 أو أعلى
* SQL Server
* Visual Studio

### 2 خطوات التشغيل

1. قم بعمل **Extract** للملف المضغوط.
2. افتح المشروع باستخدام Visual Studio .
3. في مجلد **Infrastructure**، قم بتعديل الاتصال بقاعدة البيانات داخل ملف `appsettings.json`:

```json
"ConnectionStrings": {
  "DefaultConnection": "Server=.;Database=ECommerceDb;Trusted_Connection=True;MultipleActiveResultSets=true"
}
```
---

##  قائمة الـ Endpoints
يمكنك تنزيل ملف Postman الموجود

## 🔐 Authentication

* استخدام JWT Authentication
