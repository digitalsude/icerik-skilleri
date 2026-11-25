---
name: pano-okuyucu
description: Kullanıcı hesap istatistiklerinin (insights, analytics, pano) ekran görüntüsünü ya da rakamlarını paylaştığında kullan. Rakamları okur, neyin işe yaradığını çıkarır ve sonraki 2 hafta için somut öneri verir.
---

# Pano okuyucu

## Adım 1: rakamları oku
Ekran görüntüsünden şunları tabloya dök (görünmeyeni uydurma, "görünmüyor" yaz):
- Tarih aralığı
- Görüntüleme, erişilen hesap
- Takipçi / takipçi olmayan görüntüleme oranı
- Takipçi: başlangıç, son, net değişim (başlangıç = son − net değişim)
- İçerik türüne göre görüntüleme (video, gönderi, hikâye)
- Grafikte sıçrama olan günler
- Kitle: cinsiyet, yaş, şehir (varsa)

## Adım 2: yorumla
- **Sıçrama günleri:** o günlerde ne paylaşıldı? Kullanıcıya sor ya da içerik listesinden bul. Sıçramanın ardından düşüş varsa, sıçratan içeriğin benzeri tekrar denendi mi?
- **Takipçi olmayan oranı:** yüksekse öneri sistemi içeriği dağıtıyor demektir; düşükse hook ve konu yeni kişilere hitap etmiyor olabilir.
- **İçerik türü dağılımı:** hangi tür emeğe göre en çok getiriyor?
- **İzlenme → takipçi dönüşümü:** net takipçi ÷ erişilen hesap. Düşükse profil (isim, bio, sabit gönderiler) gelenlere "neden takip edeyim" sorusunu cevaplamıyor olabilir.
- **Kitle:** içerikteki örnekler ve dil bu kitleye uyuyor mu?

## Adım 3: öneri
Kısa ve uygulanabilir:
1. **Tekrar et:** (en iyi giden 1–2 içerik ve ortak noktası)
2. **Bırak ya da değiştir:** (1 şey)
3. **Dene:** (1 yeni şey; `format-testi` skill'i varsa onunla)
4. **Profil:** (gerekiyorsa 1 düzeltme)

## Kurallar
- Rakamları yuvarlarken yönü değiştirme ("1.002.315" → "1 milyon" olur, "900 bin" → "1 milyon" olmaz).
- 30 günlük bir rakamı daha kısa bir döneme yazarken grafikle kontrol et; önceki günler sıfıra yakın değilse söyle.
- Tek bir viral videodan genel kural çıkarma.
- Neden–sonuç iddiasını kesin yazma ("bu yüzden oldu" yerine "büyük ihtimalle").

## Öğrenilenler
- …
