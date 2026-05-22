# Demo 1: Kontoauszug + fatura listesi oluşturma

[Genel bakış](README.tr.md) | [Sonraki demo](demo-2.tr.md)

## Amaç

- PDF faturalardan önce basit bir fatura listesi oluşturmak
- ödemeleri faturalarla eşleştirmek
- açık faturaları bulmak
- kısmi ödemeleri görmek
- isim farklılıklarını ve açıklanamayan ödemeleri işaretlemek

## Dosyalar

- [artifacts/demo-kontoauszug.csv](artifacts/demo-kontoauszug.csv)
- [artifacts/demo_data](artifacts/demo_data)

## Claude Web ile adımlar

1. [artifacts/demo_data](artifacts/demo_data) altındaki örnek PDF faturaları aç.
2. PDF dosyalarını Claude chat ekranına tek tek yükle ya da her PDF için ayrı doğrudan dosya linki ver.
3. Bu PDF'lerden fatura numarası, müşteri, tarih, tutar, vade tarihi ve ödeme durumu sütunlarını içeren bir CSV dosyası oluşturmasını iste.
4. Sonra oluşturulan bu CSV'yi [artifacts/demo-kontoauszug.csv](artifacts/demo-kontoauszug.csv) ile birlikte ödeme eşleştirme adımında kullan.

## Örnek prompt

```text
Sana şimdi birden fazla faturayı PDF olarak yükleyeceğim. Alternatif olarak her PDF için doğrudan GitHub dosya linki de paylaşabilirim. Bu faturaların hepsini okuyup fatura numarası, müşteri, tarih, tutar, vade tarihi ve ödeme durumu sütunlarını içeren bir CSV fatura listesi oluştur. Sonra bu banka ekstresindeki gelen ödemeleri bu CSV ile eşleştir. Üç tablo döndür: (1) eşleşen ödemeler, (2) ekstrede var ama faturada yok, (3) faturada var ama ödeme gelmemiş. Belirsiz eşleşmeleri işaretle.
```

## Dikkat edilmesi gerekenler

- Claude Web tarafında klasör yolu vermek tek başına yeterli olmayabilir.
- En güvenilir yöntem PDF'leri yüklemek, ikinci seçenek ise her PDF için ayrı dosya linki vermektir.
- Müller GmbH ve K. Müller bilerek birebir aynı yazılmadı.
- Innovate GmbH sadece kısmen ödendi.
- Fiverr ve Ref. 2024-123 doğrudan fatura listesiyle eşleşmiyor.
- Adobe, Slack, Notion ve banka masrafları gider, fatura tahsilatı değil.

## Beklenen ana sonuçlar

- Açık veya tam ödenmemiş: 2025-053, 2025-055, 2025-056
- Geç ödenmiş: 2025-050
- Belirsiz veya eşleşmeyen hareketler: Ref. 2024-123, Fiverr Auszahlung

## Referans

- [artifacts/demo-answer-key.md](artifacts/demo-answer-key.md)

[Genel bakış](README.tr.md) | [Sonraki demo](demo-2.tr.md)