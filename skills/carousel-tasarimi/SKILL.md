---
name: carousel-tasarimi
description: Carousel, çok slaytlı gönderi ya da kaydırmalı görsel post hazırlanırken kullan. Kendi stil kartına göre 1080×1350 slaytlar yazar ve teslimden önce taşma, okunurluk ve font kontrolü yapar.
---

# Carousel tasarımı

Hedef: her carousel aynı elden çıkmış gibi görünsün. Bunun için stil kartını bir kez doldur, Claude her seferinde ona uysun.

## Stil kartı (doldur)
- Boyut: 1080 × 1350 (dikey)
- Zemin: [ÖRN. düz açık renk / kareli desen / kâğıt dokusu] — renk: [#……]
- Kart: [ÖRN. açık zemin, kalın koyu çerçeve, yuvarlak köşe, düz gölge]
- Ana renk: [#……]  Vurgu renkleri: [#……] [#……]
- Başlık fontu: [AD] (dilinin tüm harfleri var mı kontrol et)
- Gövde fontu: [AD]
- Tekrarlayan detaylar: [ÖRN. sağ üstte sayfa no, sağ altta hesap adı]
- Kaçındıklarım: [ÖRN. stok fotoğraf, gradyan, emoji ikon]

## Yapı (5–8 slayt)
1. **Kapak:** büyük başlık (2–3 satır), anahtar kelime vurgulu, "kaydır" ipucu.
2. **Neden önemli / sonuç:** rakam ya da tek güçlü iddia.
3–N. **Gövde:** slayt başına 1 fikir; numaralı kartlar, karşılaştırma, ya da soru–cevap baloncukları.
Son. **Kapanış:** tek eylem çağrısı (kaydet ya da gönder) + kısa özet.

## Yazı kuralları
- Gövde yazısı en az 26 px; başlık iç slaytlarda 56–72 px.
- Slayt başına en fazla ~45 kelime.
- Önemli 1–2 kelimeyi vurgula (fosforlu bant, renk), cümlenin tamamını değil.
- Başlıkları mümkünse soru gibi yaz; arama ve kaydetme için iyi çalışıyor.

## Üretim
Slaytları HTML olarak yaz (her slayt sabit 1080×1350), sonra tarayıcıda PNG'ye çevir. Fontları yerel dosya olarak yükle ki dilin özel harfleri yedek fonta düşmesin.

## Teslimden önce MUTLAKA kontrol
Her slaytı tek tek büyütüp bak:
- Kartın altından taşan ya da kesilen yazı var mı?
- Etiket/hap yazıları ikinci satıra kayıyor mu? Kayıyorsa metni kısalt.
- Süs öğeleri yazının ya da sayfa numarasının üstüne biniyor mu?
- Slaytın ortasında büyük boş alan kaldı mı? Kaldıysa kartları büyüt ya da içeriği dağıt.
- Özel harfler (ç, ğ, ı, İ, ş) başlıkta aynı fontla mı basılmış?
Her şey temiz olmadan "hazır" deme.

## Öğrenilenler
- …
