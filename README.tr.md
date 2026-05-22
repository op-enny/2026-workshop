# AI Workshop Playbook

Bu repo, katılımcıların workshop demolarını adım adım kendi başlarına takip edebilmesi için hazırlandı.

## 1. Amaç

Bu workshop'ta, gerçekçi iş dosyalarıyla daha hızlı ve kullanılabilir sonuçlara nasıl ulaşılacağını gösteriyoruz. Odakta eşleştirme, önceliklendirme, risk tespiti ve yazım desteği var.

## 2. Kimler İçin

Freelancer'lar, küçük işletmeler, ajanslar, ofis ekipleri, danışmanlık ve backoffice rolleri için.

## 3. Repo İçeriği

- [demo-kontoauszug.csv](demo-kontoauszug.csv): Banka ekstresi
- [demo-rechnungsliste.xlsx](demo-rechnungsliste.xlsx): Fatura listesi
- [demo-vertrag.pdf](demo-vertrag.pdf): Sözleşme demosu
- [demo-posteingang.txt](demo-posteingang.txt): E-posta önceliklendirme demosu
- [demo-offene-rechnungen.xlsx](demo-offene-rechnungen.xlsx): Gecikmiş ödemeler demosu
- [demo_data](demo_data): Tekil fatura PDF'leri
- [workshop-demo-guide.md](workshop-demo-guide.md): Moderatör rehberi
- [demo-answer-key.md](demo-answer-key.md): Beklenen sonuçlar
- [workshop-onepager.md](workshop-onepager.md): Kısa özet
- [workshop-onepager.pdf](workshop-onepager.pdf): Yazdırılabilir one-pager
- [demo-files-spec.json](demo-files-spec.json): Merkezi spesifikasyon

## 4. Hızlı Başlangıç

1. Repo'yu aç.
2. İlk olarak Demo 1 ile başla.
3. Sonra yedek senaryoları tek tek dene.

## 5. Workshop Akışı

### Demo 1: Kontoauszug + Rechnungsliste

Dosyalar:

- [demo-kontoauszug.csv](demo-kontoauszug.csv)
- [demo-rechnungsliste.xlsx](demo-rechnungsliste.xlsx)

Amaç:

- Ödemeleri faturalarla eşleştirmek
- açık faturaları bulmak
- kısmi ödemeleri görmek
- isim farklılıklarını ve açıklanamayan ödemeleri işaretlemek

Örnek prompt:

```text
Bu banka ekstresindeki gelen ödemeleri, ekteki fatura listesiyle eşleştir. Üç tablo döndür: (1) eşleşen ödemeler, (2) ekstrede var ama faturada yok, (3) faturada var ama ödeme gelmemiş. Belirsiz eşleşmeleri işaretle.
```

Dikkat edilmesi gerekenler:

- Müller GmbH ve K. Müller bilerek birebir aynı yazılmadı.
- Innovate GmbH sadece kısmen ödendi.
- Fiverr ve Ref. 2024-123 doğrudan fatura listesiyle eşleşmiyor.
- Adobe, Slack, Notion ve banka masrafları gider, fatura tahsilatı değil.

Beklenen ana sonuçlar:

- Açık veya tam ödenmemiş: 2025-053, 2025-055, 2025-056
- Geç ödenmiş: 2025-050
- Belirsiz veya eşleşmeyen hareketler: Ref. 2024-123, Fiverr Auszahlung

Referans:

- [demo-answer-key.md](demo-answer-key.md)

### Demo 2: Sözleşme inceleme

Dosya:

- [demo-vertrag.pdf](demo-vertrag.pdf)

Amaç:

- riskli sözleşme maddelerini bulmak
- sonuçlarını sade bir dille açıklamak

Örnek prompt:

```text
Bu sözleşmeyi bir freelancer olarak oku. Dikkat etmem gereken maddeleri sade Türkçe olarak özetle. Özellikle: ödeme şartları, fesih koşulları, sorumluluk ve fikri mülkiyet. Riskli ya da alışılmadık maddeleri işaretle.
```

Beklenen noktalar:

- 90 gün ödeme vadesi
- 3 ay fesih süresi ve otomatik uzama
- hak devrinin daha üretim anında başlaması
- sınırsız sorumluluk
- geniş rekabet yasağı

### Demo 3: E-posta önceliklendirme

Dosya:

- [demo-posteingang.txt](demo-posteingang.txt)

Amaç:

- e-postaları önceliğe göre sıralamak
- bugün, bu hafta ve sonra olarak ayırmak

Örnek prompt:

```text
Bu e-postaları önceliğe göre sınıflandır: Bugün cevaplanmalı / Bu hafta / Eylem gerekmiyor. Her e-posta için önerilen yanıt tonunu ve tahmini süreyi de belirt.
```

### Demo 4: Açık faturaları takip etme

Dosya:

- [demo-offene-rechnungen.xlsx](demo-offene-rechnungen.xlsx)

Amaç:

- gecikme süresine göre doğru tonda e-posta yazmak
- nazik, net ve resmi hatırlatmaları ayırmak

Örnek prompt:

```text
Bu listede gecikmiş ödeme olan müşteriler var. Her biri için, gecikme süresine uygun tonda bir hatırlatma e-postası yaz: 1–14 gün için nazik ve hatırlatıcı, 15–30 gün için kararlı ve net, 30+ gün için resmi ve sonuç odaklı.
```

## 6. Kendi Kendine Deneme

1. Sadece ilgili bloktaki dosyaları aç.
2. Önce kendi prompt'unu yaz.
3. Sonucu [demo-answer-key.md](demo-answer-key.md) ile karşılaştır.
4. Prompt'u daha iyi şekilde yeniden yaz.
5. Yapı ile sonuç kalitesinin nasıl değiştiğini gözlemle.

## 7. Eğitmen İçin

- Akış için [workshop-demo-guide.md](workshop-demo-guide.md) dosyasını kullan.
- Handout olarak [workshop-onepager.pdf](workshop-onepager.pdf) dosyasını kullan.
- İç referans için [demo-answer-key.md](demo-answer-key.md) dosyasını kullan.

## 8. Public Repo Notları

Bu repo içindeki tüm veriler kurgusaldır. Gerçek hesap, gerçek fatura veya gerçek kişisel veri içermez.

## 9. İsteğe Bağlı Sonraki Adım

Repo'yu public paylaşacaksan, katılımcı soruları için Issues veya Discussions bölümünü aktif etmek faydalı olur.