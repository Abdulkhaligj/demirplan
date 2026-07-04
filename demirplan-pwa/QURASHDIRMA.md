# DəmirPlan — Quraşdırma Təlimatı

Bir mənbədən üç platforma: **Android APK + iPhone (PWA) + Veb**

## Addım 1 — GitHub Pages-də yerləşdir (pulsuz, 5 dəqiqə)

1. github.com-da yeni repo yarat, məsələn: `demirplan`
2. Bu qovluqdakı BÜTÜN faylları repo-ya yüklə:
   - index.html
   - manifest.json
   - sw.js
   - icon-192.png, icon-512.png, icon-maskable-512.png, apple-touch-icon.png
3. Repo → **Settings → Pages** → Source: `main` branch, `/ (root)` → **Save**
4. 1-2 dəqiqə sonra ünvanın hazır olacaq:
   `https://SƏNIN-ADIN.github.io/demirplan/`

## Addım 2 — Android APK (PWABuilder ilə)

1. **pwabuilder.com** saytına gir
2. GitHub Pages ünvanını yapışdır → **Start**
3. Yoxlamadan keçəndən sonra → **Package for Stores → Android**
4. İki seçim:
   - **Google Play üçün**: imzalanmış AAB paketi (Play developer hesabı lazımdır — birdəfəlik 25 USD / ~₼42)
   - **Birbaşa quraşdırma üçün**: "Other Android" → APK endir
5. APK-nı telefona at → aç → "Naməlum mənbələrə icazə ver" → quraşdır ✓

## Addım 3 — iPhone-da quraşdırma (PWA)

APK iOS-da işləmir, amma PWA əsl tətbiq kimi davranır:

1. iPhone-da **Safari** ilə GitHub Pages ünvanını aç
2. **Paylaş düyməsi (⬆) → "Ana ekrana əlavə et" (Add to Home Screen)**
3. Ana ekranda DəmirPlan ikonu yaranır — tam ekran açılır, offline işləyir ✓

## Qeydlər

- Bütün məlumatlar cihazın öz yaddaşında saxlanılır (localStorage) — server yoxdur, heç nə heç yerə göndərilmir.
- Aİ foto analizi üçün Anthropic API açarı lazımdır (console.anthropic.com). Navy metodu isə tam offline işləyir.
- Tətbiqi yeniləmək istəsən: index.html-i dəyiş, repo-ya yüklə, sw.js-dəki `CACHE` adını `demirplan-v2` et — istifadəçilərdə avtomatik yenilənəcək.
- iOS App Store-a rəsmi yükləmək istəsən Capacitor + Mac + Xcode + Apple Developer hesabı (99 USD/il) lazımdır — amma PWA əksər hallarda kifayətdir.
