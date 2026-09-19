# ORSY-OMAR-

دعوة زفاف عمر وكريمته — 06.10.2026

الموقع: https://omar-wedding-2026.omaralblack.workers.dev/

## ملفات المشروع

- `dist/index.html`: الصفحة كاملة، بما فيها التصميم والحركة والعد التنازلي وروابط التقويم والموقع وواتساب.
- `dist/*.webp`: صور الدعوة والخريطة.
- `dist/wedding-song.mp3`: أغنية الدعوة.
- `wrangler.jsonc`: إعداد نشر الموقع على Cloudflare Workers، باسم `omar-wedding-2026`.

تم نقل المصدر المحلي المحفوظ بعد استعادة نسخة 15 سبتمبر 2026، من commit `f0153b9`. لم يتضمن النقل تعديل التصميم أو الخطوط. تعذر التحقق المباشر من النسخة الحية عبر اتصال Cloudflare خلال النقل.

## ربط النشر التلقائي

الملفات موجودة في GitHub. الربط التلقائي مع Cloudflare يحتاج تفعيله من لوحة Cloudflare مرة واحدة:

1. افتح Workers & Pages واختر العامل الموجود `omar-wedding-2026`.
2. اختر Settings ثم Builds ثم Connect.
3. اربط حساب GitHub واختر `omaralblack-pixel/ORSY-OMAR-`.
4. استخدم الإعدادات التالية:

| الإعداد | القيمة |
| --- | --- |
| Production branch | `main` |
| Root directory | `/` |
| Build command | اتركه فارغًا؛ الملفات جاهزة في dist |
| Deploy command | `npx wrangler@4 deploy` |

بعد تفعيل الربط، التغييرات على فرع `main` تنشر تلقائيًا إلى العامل نفسه. تعديل إعدادات النشر يتم في `wrangler.jsonc`، وتعديل الدعوة داخل `dist/index.html`.

لا تحفظ رموز API أو مفاتيح الوصول داخل ملفات المستودع.

الدليل الرسمي: https://developers.cloudflare.com/workers/ci-cd/builds/#connect-an-existing-worker
