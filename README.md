#electiondata
### Haziran ve Kasım 2015 Türkiye Genel Seçimleri sandık sonuçları

[Haziran verisi](https://drive.google.com/file/d/0B9xGOkFUV2MAbVc2ZWktUE1SVVk/view?usp=sharing …) [@sevketzaim](https://twitter.com/sevketzaim)'in, [Kasım verisi](https://github.com/oztalha/2015-11-01-Elections-Turkey/blob/master/data/ysk.csv) de [@tozCSS](https://twitter.com/tozCSS)'in YSK'nın sitesinden çektiği veriler. Veri setlerinin ilk halini linklerden edinebilirsiniz.

Farklı formattaki iki veri setini rahat karşılaştırabilmek için birkaç değişiklik yaptım:

* İki sette de Türkçe karakterleri İngilizce muadillerine çevirdim
* İki sette de sütun isimlerini anlaşılır tek kelime olacak ve birbiriyle eşleşecek şekilde değiştirdim
* Haziran'da Adana içinde ilk 50 sandık tekrarlıyordu, onları sildim
* Kasım'da Saadet Partisi haricindeki küçük parti ve bağımsız aday sütunlarını `DIGER` sütununda birleştirdim
* Kasım'da tek bölge olarak görünen İstanbul, Ankara ve İzmir'i ilçelerine göre sırasıyla 3, 2 ve 2 bölgeye böldüm
* İki sete de coğrafi bölge sütunu ekledim

Her iki sette de bulunan sütunlar ve içerikleri şöyle:
* `BOLGE`: ilin dahil olduğu coğrafi bölge
* `IL`: ilin adı (İstanbul üç, Ankara ve İzmir ikişer ayrı il olarak gözüküyor. ör: `ANKARA-1`, `IZMIR-2`, `ISTANBUL-3`)
* `ILCE`: ilçe adı (bazı büyük ilçeler de birden fazla bölgeye ayrılmış. ör: `MELIKGAZI-1`, `TARSUS-2`, `UMRANIYE-3`)
* `MAHALLE`: mahalle/köy adı (birleşik isimli köyler (`TEPEKOY`, `CINARKOY` vb) haricindeki isimlerin sonunda '`MAH.`', '`KOYU`' ekleri bulunuyor)
* `SANDIK`: sandık numarası (numaralar ilçeler arası tekrar edebilir, ama ilçe içinde tekrar etmez)
* `SECMEN`: kayıtlı seçmen sayısı
* `OY`: kullanılan oy (yüksek katılımlı sandıklarda, oy veren sandık görevlileriyle beraber kayıtlı seçmen sayısını geçebilir)
* `ITIRAZLI`: itirazlı geçerli oy sayısı
* `ITIRAZSIZ`: itirazsız geçerli oy sayısı
* `GECERLI`: geçerli oy sayısı (`AKP+CHP+MHP+HDP+SAADET+DIGER` toplamına eşit olmalı)
* `GECERSIZ`: geçersiz oy sayısı
* `AKP`: Adalet ve Kalkınma Partisi'nin aldığı oy sayısı
* `CHP`: Cumhuriyet Halk Partisi'nin aldığı oy sayısı
* `MHP`: Milliyetçi Hareket Partisi'nin aldığı oy sayısı
* `HDP`: Halkların Demokratik Partisi'nin aldığı oy sayısı
* `SAADET`: Saadet Partisi'nin aldığı oy sayısı
* `DIGER`: adı geçmeyen partilerin ve bağımsız adayların aldığı toplam oy sayısı
