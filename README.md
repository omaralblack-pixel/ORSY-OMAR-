# ORSY-OMAR-

دعوة زفاف عمر وكريمته — 06.10.2026

الموقع: https://omar-wedding-2026.omaralblack.workers.dev/

## ملفات المشروع

- `dist/index.html`: الصفحة كاملة، بما فيها التصميم والحركة والعد التنازلي وروابط التقويم والموقع وواتساب.
- `dist/*.webp`: صور الدعوة والخريطة.
- `dist/wedding-song.mp3`: أغنية الدعوة.
- `wrangler.jsonc`: إعداد نشر الموقع على Cloudflare Workers، باسم `omar-wedding-2026`.

تم نقل المصدر المحلي المحفوظ بعد استعادة نسخة 15 سبتمبر 2026، من commit `f0153b9`. لم يتضمن النقل تعديل التصميم أو الخطوط. تعذر التحقق المباشر من النسخة الحية عبر اتصال Cloudflare خلال النقل.

## حالة ربط Cloudflare

المستودع مرتبط بعامل Cloudflare الموجود `omar-wedding-2026`. بعد رفع ملفات الموقع إلى فرع `main`، شغّل تطبيق `cloudflare-workers-and-pages` عملية البناء تلقائيًا وأعاد نتيجة نجاح.

- Commit نقل الملفات: `55fff6b5d4ddb6c5e6f6117eefa238016cbb46d6`
- فحص GitHub: `Workers Builds: omar-wedding-2026` — `success`
- Cloudflare Version ID: `592cdd0a-0023-4a98-8876-c195d8d6cf0a`
- [تفاصيل البناء الناجح](https://dash.cloudflare.com/676d7985e74569dc7b03dd0575fb07dd/workers/services/view/omar-wedding-2026/production/builds/259da0d7-ea6e-48fd-b22b-5a30b2998fe1)

يمكن مراجعة إعدادات الربط من Workers & Pages → omar-wedding-2026 → Settings → Builds. إعدادات المشروع المناسبة:

| الإعداد | القيمة |
| --- | --- |
| Production branch | `main` |
| Root directory | `/` |
| Build command | اتركه فارغًا؛ الملفات جاهزة في dist |
| Deploy command | `npx wrangler@4 deploy` |

الربط يتابع تغييرات فرع `main` لبناء الموقع على العامل نفسه. حالة البناء والتحقق من الإصدار الحي متاحان في لوحة Cloudflare. تعديل إعدادات النشر يتم في `wrangler.jsonc`، وتعديل الدعوة داخل `dist/index.html`.

لا تحفظ رموز API أو مفاتيح الوصول داخل ملفات المستودع.

الدليل الرسمي: https://developers.cloudflare.com/workers/ci-cd/builds/#connect-an-existing-worker
