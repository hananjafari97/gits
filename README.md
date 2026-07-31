# گیت — چیت‌شیت زیبا و تصویری

<p align="center">
  <img src="https://picsum.photos/seed/git/1200/300" alt="Git banner" style="max-width:100%; height:auto; border-radius:8px;" />
</p>

<p align="center">
  <a href="https://github.com/hananjafari97/gits"><img src="https://img.shields.io/badge/repo-gits-blue" alt="repo"/></a>
  <a href="https://github.com/hananjafari97/gits/stargazers"><img src="https://img.shields.io/github/stars/hananjafari97/gits?style=social" alt="stars"/></a>
  <a href="https://github.com/hananjafari97/gits/network/members"><img src="https://img.shields.io/github/forks/hananjafari97/gits?style=social" alt="forks"/></a>
</p>

یک چیت‌شیت گیت به زبان فارسی با توضیحات کوتاه، مثال و طراحی ساده که برای مبتدی‌ها و افراد حرفه‌ای مفید است.

## فهرست مطالب
- [معرفی](#معرفی)
- [دستورات پایه](#دستورات-پایه)
- [شاخه‌ها و ادغام](#شاخه‌ها-و-ادغام)
- [کار با راه‌دور (remote)](#کار-با-راه-دور-remote)
- [بازگردانی، استش، و تمیزکاری](#بازگردانی-استش-و-تمیزکاری)
- [منابع و فایل کامل](#منابع-و-فایل-کامل)

---

## معرفی
این ریپازیتوری شامل یک چیت‌شیت کامل گیت است. می‌توانید فایل کامل و نسخهٔ مرجع را در فایل [GIT-CHEATSHEET.md](./GIT-CHEATSHEET.md) ببینید.

## دستورات پایه
<div style="background:#f6f8fa;padding:12px;border-radius:8px;">

- تنظیم نام و ایمیل:

```bash
git config --global user.name "نام شما"
git config --global user.email "you@example.com"
```

- شروع یک مخزن جدید یا کلون کردن:

```bash
git init
git clone <repo-url>
```

- وضعیت و آماده‌سازی برای کامیت:

```bash
git status
git add <file>
git add .
git commit -m "پیام کامیت"
```

</div>

## شاخه‌ها و ادغام
![Branching illustration](https://picsum.photos/seed/branches/800/200)

- ایجاد و تعویض شاخه‌ها:

```bash
git branch new-feature
git checkout new-feature
# یا از نسخهٔ مدرن:
git switch new-feature
```

- ایجاد و رفتن به شاخهٔ جدید در یک خط:

```bash
git checkout -b fix/typo
```

- ادغام (merge) و بازپایه‌گذاری (rebase):

```bash
git checkout main
git merge new-feature
# یا برای تاریخچه تمیزتر:
git rebase main
```


## کار با راه‌دور (remote)
- افزودن ریموت:

```bash
git remote add origin <url>
```

- دریافت و ادغام تغییرات:

```bash
git fetch
git pull
```

- ارسال تغییرات:

```bash
git push -u origin <branch>
```

## بازگردانی، استش، و تمیزکاری
- بازگردانی فایل به HEAD:

```bash
git restore <file>
```

- ذخیرهٔ موقت تغییرات:

```bash
git stash
# مشاهده
git stash list
# اعمال و حذف
git stash pop
```

- حذف فایل‌های untracked (ابتدا پیش‌نمایش):

```bash
git clean -n
git clean -f
```

## منابع و فایل کامل
- فایل کامل چیت‌شیت: [GIT-CHEATSHEET.md](./GIT-CHEATSHEET.md)
- برای اضافه‌کردن تصاویر دلخواه یا اسکرین‌شات‌ها، می‌توانید آن‌ها را در پوشهٔ `assets/` آپلود کنید و در این README با مسیر `assets/<file>` ارجاع دهید.

---

اگر می‌خواهید من برایتان:
- تصاویر سفارشی (مثلاً نمودار شاخه‌ها و مراحل merge) اضافه کنم، تصویرسازی بسازم و داخل `assets/` آپلود کنم.
- قالب‌بندی را حرفه‌ای‌تر کنم (جعبه‌های رنگی، جدول محتوا لینک‌شونده، مثال‌های تعاملی).
- نسخهٔ انگلیسی کنار فارسی بسازم.

بگویید کدام‌یک را انجام دهم تا ادامه دهم.