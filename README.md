# Git



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
