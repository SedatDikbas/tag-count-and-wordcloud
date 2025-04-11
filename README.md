# Tag Count and Word Cloud Generation from CSV

Bu proje, verilen bir CSV dosyasındaki metin verilerini analiz ederek belirli sütunlardaki etiketlerin (tags) sayımını yapmayı ve bu etiketleri kullanarak bir kelime bulutu (word cloud) oluşturmayı amaçlamaktadır. Kullanılan veriler `dta.csv` dosyasından alınmaktadır.

## Kullanılan Kütüphaneler

- `pandas`: Veri analizi ve işleme için.
- `matplotlib`: Verilerin görselleştirilmesi için.
- `scikit-learn`: Makine öğrenmesi ve değerlendirme metrikleri için.
- `wordcloud`: Kelime bulutu oluşturmak için.
- `collections`: Sayım işlemleri için.

## Veri Seti

Proje, `dta.csv` adındaki bir CSV dosyasını kullanmaktadır. Bu dosya, "name", "combined_genres", "union_genres" gibi sütunlar içermektedir. 

### Sütunlar

- **name:** Metin verileri içeren sütun.
- **combined_genres:** Birden fazla tür içeren etiketlerin birleşimi.

## Adımlar

1. **Veri Yükleme**
   - CSV dosyası `pandas` kullanılarak yüklenir.

2. **Kelime Sayımı**
   - "name" sütunundaki kelimelerin sayımı yapılır. Kelimeler temizlenir, bağlaçlar ve kısa kelimeler göz ardı edilir.

3. **Kelime Bulutu Oluşturma**
   - En çok geçen kelimelerin sayılarıyla birlikte `name_tag.csv` dosyasına kaydedilir.
   - Oluşturulan kelime bulutu `name_tag_cloud.png` olarak kaydedilir.

4. **Tag Sayımı ve Bulutu**
   - "combined_genres" sütunundaki etiketlerin sayımı yapılır ve en çok geçen ilk 100 etiketle kelime bulutu oluşturulur. Sonuç `tag_count.csv` dosyasına kaydedilir.

## Nasıl Kullanılır?

1. Gerekli kütüphaneleri yükleyin:
   ```bash
   pip install pandas matplotlib wordcloud
