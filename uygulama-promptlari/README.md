# Claude ile kendi uygulamanı yap: 5 hazır prompt

Claude'a bir uygulama yaptırıp **Install as app** butonuyla bilgisayarına normal bir uygulama gibi kurabilirsin. Kod yazmana, paketleme yapmana ya da API anahtarı almana gerek yok.

Aşağıda kopyala-yapıştır yapabileceğin 5 prompt var. Her birinde ne yaptığı, neye ihtiyaç duyduğu ve kurduktan sonra neleri deneyebileceğin yazıyor.

> Özellik Kasım 2026'da beta olarak geldi. Ekranlar ve adlar değişebilir; bir şey farklı görünürse Claude'a "Install as app nerede?" diye sorman yeterli.

---

## Başlamadan önce

- **Claude masaüstü uygulaması** (Mac ya da Windows) gerekiyor ve güncel olmalı. Tarayıcıda (Chrome, Safari) açtığında kurma seçeneği çıkmaz.
- **Ücretsiz plan dahil** bütün planlarda açılıyor.
- **Gmail, Takvim, Notion** gibi bir uygulamayı kullanacaksan önce Claude'da o bağlantıyı (connector) aç.
- Uygulama Claude'a her iş yaptırdığında bu, **plan kullanım limitinden** düşer.
- Uygulama Claude hesabınla çalışır: **internet ve açık bir Claude oturumu** gerekir.

## 3 adımda kurulum

1. Claude masaüstü uygulamasında yeni bir sohbet aç ve aşağıdaki promptlardan birini yapıştır.
2. Claude uygulamayı yapınca dene, beğenmediğin yeri düz Türkçeyle söyle ("butonlar daha büyük olsun", "koyu tema yap").
3. Uygulamanın üstündeki **Install as app** (Uygulama olarak kur) seçeneğine bas ve onayla.

Artık Dock'ta (Windows'ta görev çubuğunda) kendi simgesi olan ayrı bir uygulaman var. Claude'a sonradan değişiklik yaptırırsan kurulu uygulama kendiliğinden güncellenir.

## İzin seviyeleri: dikkat

Kurarken uygulamaya ne kadar izin vereceğini seçersin:

| Seviye | Ne yapabilir | Ne zaman |
|---|---|---|
| **Varsayılan** | Bir web sitesinin yapabildikleri kadar | Başkasının paylaştığı her uygulama |
| **Uygulama özellikleri** | Bildirim, klavye kısayolu, menü çubuğu | Kendi yaptığın, ne yaptığını bildiğin uygulama |
| **Tam erişim** | Programları çalıştırır, dosyalarını sormadan okur, değiştirir, siler | Sadece kendi yaptığın ve kodunu anladığın uygulama |

**Başkasının yaptığı bir uygulamaya tam erişim verme.** Uygulamalar kurulmadan önce kimse tarafından incelenmiyor.

---

## 1. Günlük içerik planlayıcı

**Ne yapar:** Menü çubuğunda durur. Her sabah o gün ne paylaşacağını, saatini ve yapılacaklarını gösterir; zamanı gelince bildirim atar.
**Gerekenler:** Bağlantı gerekmez. Bildirim ve menü çubuğu için "Uygulama özellikleri" izni.

```text
Bana "Bugün ne paylaşıyorum?" adında küçük bir masaüstü uygulaması yap.

Amaç: Her sabah o gün paylaşacağım içerikleri ve yapılacaklarımı tek bakışta görmek.

Özellikler:
- Haftalık içerik planı: her gün için bir ya da birkaç içerik ekleyebileyim. Her içerikte tür (Reels, Carousel, Story, Post), saat, kısa başlık ve durum (fikir / çekildi / kurgulandı / paylaşıldı) olsun.
- Açılış ekranı "Bugün" olsun: bugünün içerikleri saat sırasıyla, altında bugünün yapılacakları.
- Yapılacaklar listesi: ekle, tamamla, sil.
- Paylaşım saatinden 30 dakika önce bildirim gönder ("19:30 Reels: <başlık>").
- Menü çubuğunda dursun; tıklayınca bugünün özetini göstersin.
- Verilerim uygulamanın içinde kayıtlı kalsın, kapatıp açınca silinmesin.

Tasarım: sade, büyük yazılı, açık ve koyu tema. Mobil gibi tek sütun.
Önce bana çalışan bir sürüm göster, sonra Install as app ile kuracağım.
```

**Sonra şunu dene:**
- "Haftalık görünüm ekle, günleri yan yana göster."
- "Paylaşıldı olarak işaretlediğim içerikleri ay sonunda say ve göster."

---

## 2. Bütçe takipçisi

**Ne yapar:** Harcamalarını hızlıca girersin. Kategoriye göre aylık grafik çıkarır, bütçeyi aşmaya yaklaşınca ve ay sonunda bildirim atar.
**Gerekenler:** Bağlantı gerekmez. Bildirim için "Uygulama özellikleri" izni.

```text
Bana "Cüzdanım" adında bir bütçe takip uygulaması yap.

Özellikler:
- Harcama ekleme: tutar, kategori (Market, Yemek, Ulaşım, Fatura, Eğlence, Diğer), tarih (varsayılan bugün), kısa not. En fazla 3 dokunuşta eklenebilsin.
- Aylık bütçe: her kategori için limit belirleyebileyim.
- Ana ekran: bu ayın toplamı, kalan bütçe ve kategorilere göre çubuk grafik.
- Bir kategoride limitin yüzde 80'ine gelince bildirim gönder.
- Ayın son günü "Bu ay X TL harcadın, en çok Y kategorisine" diye özet bildirimi gönder.
- Geçmiş aylara geçiş ve CSV olarak dışa aktarma.
- Para birimi TL, tarih biçimi gün.ay.yıl.
- Veriler uygulamanın içinde kayıtlı kalsın.

Tasarım: sade, rakamlar büyük. Önce çalışan sürümü göster.
```

**Sonra şunu dene:**
- "Tekrarlayan harcama ekle: kira ve abonelikler her ay kendiliğinden girilsin."
- "Bu ayı geçen ayla karşılaştıran bir ekran ekle."

---

## 3. Odak zamanlayıcı

**Ne yapar:** 25 dakika odak, 5 dakika mola sayar; bitince bildirim atar. Günde kaç tur yaptığını ve neye çalıştığını kaydeder.
**Gerekenler:** Bağlantı gerekmez. Bildirim, menü çubuğu ve kısayol için "Uygulama özellikleri" izni.

```text
Bana "Odak" adında bir zamanlayıcı uygulaması yap.

Özellikler:
- 25 dakika odak, 5 dakika kısa mola, her 4 turda bir 15 dakika uzun mola. Süreler ayarlanabilsin.
- Başlamadan önce "neye çalışıyorum?" diye tek satırlık bir not girebileyim.
- Her tur bitince bildirim gönder ("Odak bitti, 5 dakika mola").
- Menü çubuğunda kalan süreyi göstersin.
- Başlat / duraklat için bir klavye kısayolu olsun.
- Bugün kaç tur yaptığımı ve hangi işe toplam ne kadar zaman ayırdığımı göstersin; son 7 günü küçük bir grafikle.
- Veriler uygulamanın içinde kayıtlı kalsın.

Tasarım: ortada büyük bir sayaç, koyu tema, dikkat dağıtmayan sade bir ekran.
```

**Sonra şunu dene:**
- "Haftalık hedef koyayım (ör. 20 tur), ilerlemeyi göster."
- "Tur bitince kısa bir 'ne yaptım' notu sorsun, günün sonunda listele."

---

## 4. Gmail özeti → yapılacaklar

**Ne yapar:** Son 24 saatin önemli maillerini özetler ve her birinden yapılacak bir iş çıkarır.
**Gerekenler:** Claude'da **Gmail bağlantısı** açık olmalı. Uygulama okur; senin onayın olmadan mail göndermemeli.

```text
Bana "Mail Özeti" adında bir uygulama yap. Gmail bağlantımı kullansın.

Özellikler:
- "Özetle" butonuna basınca son 24 saatin gelen kutusunu okusun.
- Bülten, reklam ve otomatik bildirimleri ayırsın; kalan mailleri önem sırasına koysun.
- Her önemli mail için: gönderen, tek cümlelik özet ve varsa yapılacak iş ("Cuma'ya kadar teklif gönder").
- Yapılacak işleri ayrı bir listede toplasın; tamamladıklarımı işaretleyebileyim.
- Bir maile cevap taslağı yazmasını isteyebileyim ama ASLA kendiliğinden mail göndermesin; taslağı sadece bana göstersin.
- Sabah ilk açılışta "X önemli mail, Y yapılacak iş" diye bildirim göstersin.

Tasarım: sol tarafta özetler, sağda yapılacaklar. Sade ve okunaklı.
```

**Sonra şunu dene:**
- "Belirli kişilerden gelen mailleri her zaman en üste koy: <isimler>."
- "Yapılacakları Takvim'e etkinlik olarak eklemeyi öner, eklemeden önce bana sor."

---

## 5. Yarının toplantıları + hazırlık notu

**Ne yapar:** Takvimindeki yarınki toplantıları listeler ve her biri için 3 maddelik hazırlık notu çıkarır.
**Gerekenler:** Claude'da **Takvim bağlantısı** açık olmalı. İstersen Gmail bağlantısı da (toplantıyla ilgili son mailleri bulmak için).

```text
Bana "Yarın" adında bir uygulama yap. Takvim bağlantımı kullansın, varsa Gmail bağlantımı da.

Özellikler:
- Yarınki toplantıları saat sırasıyla listelesin: saat, başlık, katılımcılar, toplantı linki.
- Her toplantı için 3 maddelik hazırlık notu: amaç ne, bana düşen ne, sormam gereken ne. Açıklamadan ve varsa ilgili son maillerden çıkarsın.
- Üst üste binen ya da arada 10 dakikadan az boşluk olan toplantıları uyarı rengiyle göstersin.
- Her akşam 20:00'de "Yarın X toplantın var, ilki saat Y'de" diye bildirim göndersin.
- Takvimde hiçbir şeyi kendiliğinden değiştirmesin.

Tasarım: zaman çizelgesi gibi dikey liste, notlar kartın içinde açılıp kapansın.
```

**Sonra şunu dene:**
- "Toplantıdan sonra kısa not alayım, uygulama bunları toplantıya bağlı saklasın."
- "Haftanın toplantı yükünü (saat olarak) gösteren bir ekran ekle."

---

## Kendi fikrini prompta çevir

Bu şablonu kendi ihtiyacınla doldur:

```text
Bana "<uygulamanın adı>" adında bir uygulama yap.

Amaç: <hangi sorunu çözüyor, tek cümle>.

Özellikler:
- <en önemli şey>
- <ikinci şey>
- <bildirim lazımsa: ne zaman, ne yazsın>
- Veriler uygulamanın içinde kayıtlı kalsın.

Kullanacağı bağlantılar: <yoksa "yok">. Hiçbir şeyi bana sormadan göndermesin, silmesin, değiştirmesin.
Tasarım: <sade / koyu tema / büyük yazı>.
Önce çalışan bir sürüm göster.
```

İpucu: İlk seferde her şeyi isteme. Önce en basit hâlini yaptır, sonra tek tek ekle.

## Sorun giderme

- **"Install as app" görünmüyor:** Claude'u tarayıcıda açmış olabilirsin; masaüstü uygulamasında aç. Uygulamayı güncelle. Beta herkese aynı anda gelmeyebilir, birkaç gün bekle.
- **Kurdum ama açılmıyor:** Claude masaüstü uygulaması açık ve hesabın giriş yapmış olmalı, internet bağlantısı olmalı.
- **Veriler gelmiyor (Gmail/Takvim):** Claude'da o bağlantının açık olduğunu ve uygulamanın ilk açılışta istediği izni verdiğini kontrol et.
- **Bildirim gelmiyor:** Uygulamaya "Uygulama özellikleri" iznini verdiğinden ve bilgisayarının bildirim ayarlarında uygulamanın açık olduğundan emin ol.

---

Hazırlayan: [@sude.ai](https://instagram.com/sude.ai) · MIT lisansı, kopyala, değiştir, paylaş.
