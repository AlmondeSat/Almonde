# Video ve uydu haritası yaması — 23 Kasım 2026

Bu paket 23 Kasım ana güncellemesinin üzerine uygulanır. ZIP'i açın; altı dağıtım dosyasını mevcut GitHub deposunun köküne, `assets/` yapısını koruyarak birleştirin. Bu notu yüklemeniz gerekmez. ZIP'in kendisini yüklemeyin. Eski video dosyalarını silmeyin, tekrar yüklemeyin. En güvenlisi tek commit; partili yüklemede Worker'ı en son koyun.

## Değişiklik

- Orijinal 160 kaliteli kare açılışta dört eşzamanlı indirmeyle sıkıştırılmış biçimde belleğe alınır. Çözünürlük, kare dosyaları ve sıkıştırma kalitesi değiştirilmedi.
- Yakın kareler ayrıca çözülür; 160 karenin tümü çözülmüş GPU görüntüsü olarak tutulmaz. Tampon tamamlanınca oynatma ağdan bağımsız hale gelir. İlk yükleme uzayabilir. Kullanıcı hazırlığı atlarsa bu avantajın tamamı elde edilemez.
- Normal kaydırmada yararlı indirmeler sürekli iptal edilmez; büyük konum sıçramalarında eski işler bırakılır. İndirme zaman aşımı ve hazırlığı geçme seçeneği korunur.
- Uydu görüntüleri sabit Esri sunucularından aynı kökenli `/api/imagery-tiles` üzerinden alınır. HTML hata yanıtları reddedilir, ikinci sabit sunucu denenir, başarılı görüntüler önbelleklenir. Kaynak hatalarında harita sınırlı yeniden deneme yapar.
- Service worker v41.

## Kontrol

75 otomatik test ve TypeScript denetimi geçti. Yerel `/api/imagery-tiles?z=3&x=4&y=3` gerçek JPEG/HTTP200 döndürdü. Gerçek cihazda FPS veya zayıf ağ ölçümü bu paket için tamamlanmadı; sabit 60 FPS garantisi verilmez. İlk yüklemeden sonra yavaş ileri/geri kaydırma ve tüm bölgelere harita yakınlaştırma denenmelidir. Üçüncü taraf uydu hizmetinin erişilebilirliği garanti değildir.

Canlıya dağıtım yapılmadı. Yerel sürüm: http://127.0.0.1:3001/#top

Önceki başarılı dağıtımı Cloudflare'da koruyun. Sorunda önceki sürüme dönün; API anahtarını hiçbir dosyaya eklemeyin.
