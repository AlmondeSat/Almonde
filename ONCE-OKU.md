# Yalnızca güncelleme — 24 Kasım 2026

GitHub AlmondeSat/Almonde main ağacı `9a3ed488e615713c66c1617f5e4f3171a1b24344` ile yerel son sürümün Git blob içerik özetleri karşılaştırıldı. 289 dosya aynı; yalnızca 7 yeni/değişen dosya bu pakette. Video ve logo dosyaları aynı olduğundan dahil edilmedi. Açılmış güncelleme 3.018.904 bayttır.

1. ZIP'i açın.
2. `GUNCELLEME` klasörünün İÇİNDEKİ dosyaları mevcut deponun köküne birleştirin. `assets` klasörü depodaki `assets` ile birleşmeli. `GUNCELLEME` adında ek üst klasör veya ZIP dosyası yüklemeyin.
3. Dört yeni `assets` dosyasını önce, `_worker.js` dosyasını en son yükleyin. `.assetsignore` ve `wrangler.jsonc` kökte olmalı. Tercihen hepsini tek commit ile gönderin; eski dosyaları silmeyin.
4. Cloudflare deploy komutu mevcut `npx wrangler deploy` olarak kalabilir. Gerçek API anahtarı dosyalarda değil Cloudflare Secret ortamında kalır.
5. Dağıtımdan sonra siteyi yenileyin. Rapor bölümü analiz sonrasında görünür; Albert sürekli açıktır. İlk ziyaret İngilizce, önceki dil tercihi korunur. Son görünüm, yumuşak köşeler, açık mod başlıkları ve son telif satırı dahildir.

Önceki 66 MB toplu paketi ve eski küçük yamaları ayrıca yüklemeyin. Bu fark paketi mevcut GitHub içeriğinin üstüne uygulanır; boş depoya tek başına kurulmaz. GitHub bu karşılaştırmadan sonra tekrar değiştiyse dosya listesi yeniden kontrol edilmelidir.

Son yerel kod: 78 test geçti. Canlıya otomatik yükleme yapılmadı. Sorunda Cloudflare'dan önceki başarılı dağıtıma dönün. `karsilastirma.json` yalnızca bilgi içindir, siteye yüklenmesi gerekmez.
