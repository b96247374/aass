# Military Reports System

نظام إدارة التقارير العسكرية مبني باستخدام Flask.

## المتطلبات
- Python 3.10 أو أحدث
- Flask
- Flask-Login
- Flask-SQLAlchemy
- hijri-converter
- pytz
- gunicorn (للاستضافة)

## طريقة التشغيل محليًا
1. ثبت المتطلبات:
   ```bash
   pip install -r requirements.txt
   ```
2. شغل التطبيق:
   ```bash
   python app.py
   ```
3. افتح المتصفح على:
   ```
   http://127.0.0.1:5000
   ```

## طريقة النشر على Render أو Heroku
1. ارفع جميع ملفات المشروع (مع requirements.txt و Procfile) إلى GitHub.
2. اربط المستودع مع Render أو Heroku.
3. استخدم إعدادات التشغيل:
   - Build command:
     ```
     pip install -r requirements.txt
     ```
   - Start command:
     ```
     gunicorn app:app
     ```
     أو إذا كان ملف app.py داخل مجلد:
     ```
     gunicorn military_reports_system.app:app
     ```

## ملاحظات
- لا ترفع ملفات قاعدة البيانات أو uploads أو __pycache__ إلى GitHub.
- جميع القوالب في مجلد `views` أو `templates`.
- جميع الملفات الثابتة (CSS, صور) في مجلد `static`.

---

لأي استفسار أو مشكلة، تواصل مع مطور النظام.
