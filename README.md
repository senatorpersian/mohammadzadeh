# سید محمدزاده — پورتفولیو تلگرامی

سایت شخصی به شکل **تلگرام دسکتاپ** با آواتار، نوتیفیکیشن و چت تعاملی.

## فایل‌ها

```
portfolio/
├── index.html          ← صفحه اصلی
├── assets/
│   ├── avatar.png      ← آواتار
│   └── notify.wav      ← صدای پیام
├── .nojekyll
└── README.md
```

## پیش‌نمایش محلی

```bash
cd portfolio
python -m http.server 8090
```

باز کنید: http://localhost:8090

---

## انتشار روی GitHub Pages (مرحله‌به‌مرحله)

### مرحله ۰ — ثبت‌نام
اگر اکانت نداری: https://github.com/signup

### مرحله ۱ — انتخاب آدرس سایت

دو مدل رایج:

| مدل | اسم ریپو | آدرس نهایی |
|-----|---------|------------|
| **الف) سایت اصلی یوزر** | `USERNAME.github.io` | `https://USERNAME.github.io` |
| **ب) پروژه جدا** | مثلاً `portfolio` | `https://USERNAME.github.io/portfolio/` |

پیشنهاد برای رزومه: **مدل الف** با یوزرنیم ثابت و حرفه‌ای  
مثال: اگر یوزرنیم‌ت `mohammadzadeh` باشد → ریپو = `mohammadzadeh.github.io`  
لینک = `https://mohammadzadeh.github.io`

> یوزرنیم GitHub را بعداً هم می‌شود عوض کرد، ولی لینک‌ها می‌شکنند — از اول خوب انتخاب کن.

### مرحله ۲ — ساخت ریپازیتوری
1. برو https://github.com/new  
2. **Repository name** را طبق جدول بالا بگذار  
3. Public را بزن  
4. تیک README نزن (خالی بساز)  
5. Create repository

### مرحله ۳ — آپلود فایل‌ها

**روش آسان (بدون Git):**
1. داخل ریپوی خالی روی **uploading an existing file** بزن  
2. کل محتویات پوشه `portfolio` را بکش داخل صفحه:
   - `index.html`
   - پوشه `assets` (با avatar و notify)
   - `.nojekyll`
   - `README.md` (اختیاری)
3. Commit changes

**روش با Git (ترمینال):**
```bash
cd portfolio
git init
git add .
git commit -m "Telegram-style portfolio"
git branch -M main
git remote add origin https://github.com/USERNAME/REPO.git
git push -u origin main
```
`USERNAME` و `REPO` را عوض کن.

### مرحله ۴ — روشن کردن Pages
1. ریپو → **Settings**  
2. از منوی چپ **Pages**  
3. Build and deployment → Source: **Deploy from a branch**  
4. Branch: `main` — Folder: `/ (root)`  
5. Save  

۱ تا ۳ دقیقه صبر کن. لینک سبز بالای همان صفحه ظاهر می‌شود.

### مرحله ۵ — بررسی لینک
- مدل الف: `https://USERNAME.github.io`  
- مدل ب: `https://USERNAME.github.io/REPO/`  

اگر مدل ب است و عکس/صدا لود نشد، معمولاً مسیر نسبی `assets/...` درست است؛ فقط مطمئن شو فایل‌ها در root ریپو هستند نه داخل زیرپوشه اضافه.

### مرحله ۶ — دامنه اختصاصی (اختیاری)
اگر دامنه داری (مثلاً `mohammadzadeh.ir`):
1. Pages → Custom domain → دامنه‌ات را وارد کن  
2. در DNS یک رکورد `CNAME` به `USERNAME.github.io` بساز  
3. تیک Enforce HTTPS را بعد از فعال‌شدن بزن  

---

## نکات اسم و برندینگ لینک

- یوزرنیم کوتاه و انگلیسی: `mohammadzadeh` / `seyedads` / `mohammadzadehads`
- از عدد و خط‌زیر زیاد پرهیز کن
- لینک را توی بیو تلگرام و اینستا بگذار:  
  `🌐 https://USERNAME.github.io`

## آپدیت بعدی سایت
فقط فایل را دوباره آپلود/پوش کن؛ Pages خودکار عوض می‌شود.
