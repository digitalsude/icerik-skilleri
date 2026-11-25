# İçerik Skill'leri

Kısa video ve carousel üreten herkes için 7 temel Claude skill'i. Türkçe, ücretsiz, istediğin gibi değiştir.

Skill, Claude'a **bir kez** yazdığın tariftir: kuralların, örneklerin, kaçındığın şeyler. Her istekte aynı uzun promptu yapıştırmak yerine "reels yaz" dersin, Claude skill'i açıp gerisini bilir.

| # | Skill | Ne işe yarar |
|---|-------|--------------|
| 1 | [`hook-yazici`](skills/hook-yazici/SKILL.md) | İlk 2 saniye için 10 hook çıkarır, en iyi 3'ünü nedeniyle seçer |
| 2 | [`reels-senaryosu`](skills/reels-senaryosu/SKILL.md) | Hook → tek fikir → kapanış; süreye göre kelime sayısı ve ekran yazısı |
| 3 | [`format-testi`](skills/format-testi/SKILL.md) | 4 format × 4 video test planı ve hangisinin kazandığını bulma |
| 4 | [`aranir-aciklama`](skills/aranir-aciklama/SKILL.md) | Arama motorlarının ve yapay zekâ aramalarının okuyabildiği açıklama |
| 5 | [`hashtag-rotasyonu`](skills/hashtag-rotasyonu/SKILL.md) | Her paylaşımda 5 etiket, son paylaşımlarla aynı set çıkmaz |
| 6 | [`carousel-tasarimi`](skills/carousel-tasarimi/SKILL.md) | Tek bir görsel stil; her carousel aynı elden çıkmış gibi |
| 7 | [`pano-okuyucu`](skills/pano-okuyucu/SKILL.md) | İstatistik ekran görüntüsünü okuyup "neyi tekrar et, neyi bırak" der |

**Yeni:** [Claude ile kendi uygulamanı yap: 5 hazır prompt](uygulama-promptlari/README.md). Install as app ile masaüstüne kurulan uygulamalar için kopyala-yapıştır promptlar.

## Kurulum

**Claude uygulaması (web / masaüstü):**
1. `dist/` klasöründen istediğin skill'in `.zip` dosyasını indir.
2. Ayarlar → Yetenekler (Capabilities) → Skills → **Skill yükle**.
3. Yeni bir sohbette normal konuş: "şu konu için reels senaryosu yaz". Claude uygun skill'i kendisi açar.

**Claude Code:**
```bash
git clone https://github.com/digitalsude/icerik-skilleri.git
cp -r icerik-skilleri/skills/* ~/.claude/skills/
```

## İlk iş: kendine göre doldur

Her skill'de `[KÖŞELİ PARANTEZ]` içinde boş alanlar var: hesabının konusu, kitlen, sesin, renklerin, etiket havuzun. Bunları doldurmadan da çalışır ama doldurunca çıktı sana benzemeye başlar.

En hızlı yol: Claude'a şunu yaz:

> "`reels-senaryosu` skill'ini benim hesabıma göre doldur. Hesabım şu konuda: … Kitlem: … Bana sor, eksik ne varsa."

## Asıl numara: her düzeltme skill'e yazılır

Her skill'in sonunda **Öğrenilenler** bölümü var. Bir çıktıyı düzelttiğinde ("bu çok uzun", "bu kelimeyi kullanma", "hook'lar hep soru olmasın") Claude'a şunu de:

> "Bunu skill'e ekle."

Aynı hatayı ikinci kez yapmaz. Bir ay sonra skill'in senin yazdığın gibi yazar.

## Sınırlar

- Bunlar başlangıç sürümleri. Rakam, algoritma ya da platform kuralı içeren satırları kendi verinle kontrol et; platformlar kurallarını sık değiştiriyor.
- Hiçbir skill sonuç garantisi vermez. İzlenmeyi içerik getirir; skill'ler sadece her içeriği aynı özenle çıkarmana yardım eder.

## Lisans

MIT. Kopyala, değiştir, paylaş.
