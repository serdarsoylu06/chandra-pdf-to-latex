# chandra-pdf-to-latex

PDF dosyalarını LaTeX'e dönüştürmeyi hedefleyen bu proje için başlangıç seviyesinde proje dokümantasyonu.

## Proje Amacı

Bu depo, PDF içeriğini analiz ederek LaTeX çıktısına dönüştüren bir uygulama geliştirmek için kullanılmaktadır. Şu anda depo çok erken aşamadadır ve uygulama kodu henüz eklenmemiş görünmektedir.

## Mevcut Durum

- Depoda şu anda yalnızca `README.md` bulunmaktadır.
- Uygulama kaynak kodu, bağımlılık tanımları ve çalıştırma komutları henüz bulunmamaktadır.
- Bu nedenle aşağıdaki plan, hedeflenen uygulama yapısını ve geliştirme yönünü tanımlar.

## Hedeflenen Özellikler

- PDF dosyası yükleme veya dosya yolu üzerinden alma
- PDF içindeki metin, başlık, denklem ve temel yapıların ayrıştırılması
- LaTeX çıktısı üretimi
- Çıktının `.tex` dosyası olarak kaydedilmesi
- Gerekirse görsel, tablo ve formül tespiti için ek işleme adımları
- Hata yönetimi ve dönüştürme raporlaması

## Önerilen Mimari

Aşağıdaki modüler yapı önerilir:

- `src/ingestion/`: PDF alma ve ön işleme
- `src/parsing/`: metin, blok, başlık ve yapı ayrıştırma
- `src/conversion/`: LaTeX üretimi
- `src/output/`: `.tex` ve yardımcı çıktıların yazılması
- `src/cli/` veya `src/api/`: komut satırı arayüzü veya servis katmanı
- `tests/`: birim ve entegrasyon testleri
- `docs/`: ek teknik dokümantasyon

## Önerilen Girdi / Çıktı Akışı

1. Kullanıcı PDF dosyasını verir.
2. Sistem PDF içeriğini sayfa sayfa okur.
3. Metin blokları ve yapısal öğeler ayrıştırılır.
4. İçerik LaTeX temsiline dönüştürülür.
5. Sonuç `.tex` dosyası olarak dışa aktarılır.
6. Gerekirse hata ve kalite raporu üretilir.

## MVP Kapsamı

İlk sürüm için önerilen minimum kapsam:

- Metin ağırlıklı PDF'leri işleme
- Başlık, paragraf ve basit liste yapılarının korunması
- Temel LaTeX belge iskeleti üretimi
- Komut satırından tek dosya dönüştürme
- Başarısız dönüşümlerde anlaşılır hata mesajları

## Gelecek Geliştirmeler

- Tablo dönüştürme desteği
- Matematiksel ifade tespiti
- Görsel çıkarma ve LaTeX referanslama
- Web arayüzü
- Toplu PDF işleme
- Şablon seçimi ve özelleştirilebilir çıktı biçimi

## Kurulum

Henüz proje bağımlılıkları veya çalışma komutları tanımlanmamıştır.

Planlanan adımlar:

1. Kullanılacak teknoloji yığını belirlenir.
2. Paket yöneticisi ve bağımlılıklar eklenir.
3. Geliştirme ortamı yapılandırılır.
4. Örnek giriş/çıkış dosyaları hazırlanır.

## Geliştirme İçin Önerilen Dosyalar

Projeye eklenmesi faydalı olacak dosyalar:

- `LICENSE`
- `.gitignore`
- `CONTRIBUTING.md`
- `docs/architecture.md`
- `docs/roadmap.md`
- `tests/`
- örnek PDF ve örnek LaTeX çıktı klasörleri

## Katkı Süreci

Katkı vermeden önce aşağıdaki başlıkların netleştirilmesi önerilir:

- Hangi programlama dili kullanılacak?
- Dönüştürme kural seti nasıl tanımlanacak?
- Matematik, tablo ve görseller nasıl ele alınacak?
- Başarı ölçütü nedir?

## Yol Haritası

### Aşama 1
- Proje iskeletinin kurulması
- Teknoloji seçimi
- Basit PDF metin çıkarımı

### Aşama 2
- Metinden temel LaTeX üretimi
- Test altyapısı
- Örnek dosyalarla doğrulama

### Aşama 3
- Gelişmiş yapı algılama
- Tablo ve denklem desteği
- Çıktı kalitesinin artırılması

## Not

İstersen bir sonraki adımda bu repoya doğrudan şu dosyaları da ekleyebilirim:

- `.gitignore`
- `LICENSE`
- `CONTRIBUTING.md`
- `docs/architecture.md`
- `docs/roadmap.md`