# Bisiklet Kiralama Veri Analizi Projesi

Bu proje, Konya, Türkiye'de Ekim, Kasım ve Aralık aylarına ait bisiklet kiralama verilerini analiz ediyor. Veri kümesi, kiralama başlangıç ve bitiş tarihleri, konumlar, mesafeler ve ücretler hakkında bilgiler içerir.

## İçindekiler

- [Giriş](#giriş)
- [Veri Hazırlığı](#veri-hazırlığı)
- [Veri Analizi](#veri-analizi)
- [Görselleştirme](#görselleştirme)
- [Başlangıç](#başlangıç)
- [Katkıda Bulunma](#katkıda-bulunma)
- [Lisans](#lisans)

## Giriş

Bu proje, Konya, Türkiye'de Ekim, Kasım ve Aralık aylarında bisiklet kiralama desenlerini ve trendlerini incelemeyi amaçlamaktadır. Şehirdeki bisiklet kullanımını daha iyi anlamak için veri temizleme, keşif ve görselleştirme içerir.

## Veri Hazırlığı

- Proje, her ay için CSV dosyalarında saklanan bisiklet kiralama verilerini kullanır.
- Veri temizleme adımları şunları içerir:
  - Tarih sütunlarını datetime biçimine dönüştürme.
  - Konum verilerini enlem ve boylama ayırma.
  - Kiralama sürelerini dakika cinsinden hesaplama.
  - Eksik veya tutarsız verileri ele alma.

## Veri Analizi

- Kiralama desenlerini analiz etmek, en popüler kiralama günlerini ve saatlerini içerir.
- Ortalama mesafeleri ve ücretleri hesaplama.
- Kiralama sürelerinin dağılımını incelemek.
- Herhangi bir mevsimsel eğilimi veya anormalliği tanımlama.

## Görselleştirme

- Folium ile etkileşimli haritalar oluşturarak bisiklet kiralama sıcak noktalarını görselleştirme.
- Veri trendlerini göstermek için grafikler ve tablolar oluşturma.
- Kiralama yoğunluğunu görselleştirmek için ısı haritalarını kullanma.

## Başlangıç

1. Deposunu klonlayın:

   ```bash
   git clone https://github.com/kullaniciadiniz/bisiklet-kiralama-analiz.git


