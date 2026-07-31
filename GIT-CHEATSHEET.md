# چیت‌شیت دستورهای Git (فارسی)

این فایل شامل دستورات مهم و پرکاربرد گیت به‌همراه توضیح کوتاه و مثال است.

## پایه و پیکربندی
- git config --global user.name "نام شما"
- git config --global user.email "you@example.com"
- git config --list

## شروع کار
- git init
  - ایجاد مخزن محلی در پوشه فعلی
- git clone <repo-url>
  - کپی کردن مخزن از راه دور

## وضعیت و بررسی
- git status
  - نمایش فایل‌های تغییر کرده، آماده برای کامیت و غیره
- git diff
  - نمایش تفاوت‌ها بین نسخه‌ها (کاربرد: قبل از استیج)

## افزودن و کامیت
- git add <file>
- git add .
  - اضافه‌کردن فایل‌ها به staging area
- git commit -m "پیام کامیت"
  - ثبت تغییرات در تاریخچه
- git commit -am "پیام"  # اضافه + کامیت برای فایل‌های دنبال‌شده

## کار با شاخه‌ها (Branches)
- git branch
  - لیست شاخه‌ها
- git branch <name>
  - ایجاد شاخه جدید
- git checkout <branch>
  - رفتن به شاخه
- git switch <branch>
  - معادل مدرن برای checkout به شاخه
- git checkout -b <new-branch>
  - ایجاد و رفتن به شاخه‌ی جدید
- git merge <branch>
  - ادغام شاخه‌ی مشخص به شاخه‌ی فعلی
- git rebase <branch>
  - پایه‌گذاری مجدد شاخه (برای تاریخچه‌ی تمیزتر)

## راه دور (Remote)
- git remote -v
  - نمایش ریموت‌ها
- git remote add origin <url>
  - اضافه‌کردن ریموت جدید
- git fetch
  - گرفتن تاریخچه از ریموت بدون ادغام
- git pull
  - دریافت و ادغام از ریموت (fetch + merge)
- git push
  - ارسال شاخه‌ی محلی به ریموت
- git push -u origin <branch>
  - ست کردن upstream و اولین پوش

## تاریخچه و بررسی کامیت‌ها
- git log
  - لیست کامیت‌ها
- git log --oneline --graph --decorate --all
  - نمایش خلاصه و گراف
- git show <commit>
  - نمایش تغییرات یک کامیت
- git blame <file>
  - نشان‌دهنده‌ی هر خط و کامیتی که آن را تغییر داده

## بازگردانی و اصلاح
- git restore <file>
  - بازگرداندن فایل به نسخه‌ی HEAD (unstage و discard local changes)
- git restore --staged <file>
  - برداشتن فایل از staging
- git reset --soft <commit>
  - برگرداندن HEAD بدون تغییر staging
- git reset --hard <commit>
  - بازگردانی کامل (مخرب)
- git revert <commit>
  - ایجاد یک کامیت جدید که اثر کامیت مشخص را معکوس می‌کند (امن برای ریپوزهای مشترک)

## stash (ذخیره موقت تغییرات)
- git stash
  - ذخیره تغییرات کاری (پاک کردن از working dir)
- git stash list
- git stash apply  # اعمال آخرین stash بدون حذف
- git stash pop    # اعمال و حذف آخرین stash

## تگ‌گذاری
- git tag <name>
  - ایجاد تگ سبک
- git tag -a v1.0 -m "release 1.0"
  - ایجاد تگ annotated
- git push origin --tags
  - ارسال تگ‌ها به ریموت

## کار با فایل‌ها
- git rm <file>
  - حذف فایل و stage کردن حذف
- git mv <old> <new>
  - انتقال/تغییر نام و stage کردن

## تمیزکاری
- git clean -n  # چه فایل‌هایی حذف می‌شود؟
- git clean -f  # حذف فایل‌های untracked

## ابزارهای مفید
- git stash save "message"
- git cherry-pick <commit>
  - اعمال یک کامیت از شاخه‌ی دیگر
- git bisect start / good / bad
  - برای پیداکردن کامیتی که باگ را معرفی کرده
- git reflog
  - تاریخچه‌ی HEAD (بازیابی کامیت‌های از دست رفته)

## پیشنهادات و Alias‌ها
- git config --global alias.co checkout
- git config --global alias.br branch
- git config --global alias.ci commit
- git config --global alias.st status

---

فایل بالا شامل دستورات پایه و رایج است. اگر می‌خواهید نسخه‌ی انگلیسی یا دستورهای بیشتری (مثلاً گیت‌فلو، هوک‌ها، یا مثال‌های پیشرفته) اضافه کنم بگویید تا گسترش بدهم.