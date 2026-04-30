# LatestReleaseMirror
A GitHub Actions pipeline that mirrors only the latest release of multiple source repos, filters assets by file pattern, skips oversized files (>100 MB), and organizes everything in releases/owner/repo/ with version metadata.


## 📦 Latest Releases
<!-- RELEASES_START -->

<!-- RELEASES_END -->





## 🔒 بررسی صحت فایل‌ها (SHA256)


⚠️ پیش از اجرا یا نصب فایل‌های دانلود شده از این ریپو (و بصورت کلی هر جایی به جز منبع اصلی)، یک‌بار Checksum فایل دانلود شده را با مقدار اصلی (که در صفحه Release هر پروژه برای تمام ورژن‌ها قابل مشاهده‌است) مقایسه کنید. برای حاصل شدن اطمینان از اینکه فایل‌ها دستکاری نشده‌اند و دقیقا همان نسخه منتشر شده در سورس اصلی می‌باشند، باید مقدار هش‌ sha256 یک نسخه از یک فایل خاص با مقدار هشی که برای همان نسخه و فایل در سورس اصلی قابل مشاهده‌است، کاملا یکسان باشد. در صورت مغایرت، از نصب آن خود‌داری کنید.

در اینجا یک راهنمای کوتاه برای بررسی فایل‌های دانلود شده از منبعی به جز سورس اصلی، با استفاده از SHA256 در سیستم‌عامل‌های مختلف آورده شده است.



### 🍎 macOS / 🐧 Linux (ترمینال)
```bash
sha256sum FILE_NAME
```
(در macOS قدیمی‌تر ممکن است به جای آن از shasum -a 256 FILE_NAME استفاده کنید)


### 🪟 Windows (PowerShell)


```Powershell
Get-FileHash -Algorithm SHA256 FILE_NAME
```

### 📱 Android (با ترمینال یا Termux)
```Powershell
sha256sum FILE_NAME
```
(اگر دستور در دسترس نبود، ابتدا pkg install coreutils را در Termux اجرا کنید)

