# راهنمای استاندارد استفاده از Git

## ۱. قوانین مربوط به Branchها

- از **Push مستقیم به شاخه‌های اصلی** مانند `main` یا `develop` خودداری کنید.  
- برای هر تسک یا قابلیت جدید، یک **Branch جدید** ایجاد کنید.

### ساختار نام‌گذاری Branch‌ها:
- فیچر جدید: `feature/feature-name`  
- رفع باگ: `bugfix/issue-description`  
- هات‌فیکس: `hotfix/critical-issue`  
- تست: `test/test-description`

**مثال‌ها:**
- `feature/user-authentication`  
- `bugfix/fix-login-issue`

### افزودن شماره تسک (اختیاری):
شماره تسک جیرا را به ابتدای نام برنچ اضافه کنید:

**مثال‌ها:**
- `feature/123-user-authentication`  
- `bugfix/456-login-error`

---

## ۲. قوانین مربوط به پیام Commit

- پیام کامیت باید **کوتاه، دقیق و با فعل حال** نوشته شود.  
- هر کامیت باید تنها **یک تغییر منطقی (Atomic Commit)** را پوشش دهد.  
- استفاده از ساختار **Conventional Commits** توصیه می‌شود.

### ساختار پیشنهادی پیام کامیت:
```
<type>(scope): short message
```

**مثال‌ها:**
- `feat(auth): add OTP login via SMS`  
- `fix(cart): correct total price calculation`  
- `refactor(db): optimize user query performance`  
- `docs(api): update response schema docs`

### نوع تغییرات پیشنهادی:
- `feat`: اضافه کردن قابلیت جدید  
- `fix`: رفع باگ  
- `refactor`: بهبود ساختار کد بدون تغییر عملکرد  
- `docs`: تغییر در مستندات  
- `style`: تغییرات ظاهری (بدون منطق جدید)  
- `test`: اضافه یا تغییر تست‌ها

---

## ۳. قوانین مربوط به Merge Request  

- بعد از پایان هر تسک، برای برنچ مربوطه **Merge Request** باز کنید.  
- **بررسی و رفع کانفلیکت‌ها (conflicts)** پیش از ارسال Merge Request بر عهده‌ی برنامه‌نویس است.  
- **بررسی کد (Code Review)** توسط **Tech Lead تیم** انجام می‌شود.  
- Tech Lead موظف است **نکات فنی، ایرادات یا پیشنهادها را به صورت کامنت داخل GitLab** ثبت کند تا قابل پیگیری و شفاف باشد.

---
