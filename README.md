# Proje: Sevk İrsaliye Tarihi Tahmini

Bu proje, kullanıcıdan alınan **Kilo**, **Metre** ve **İşlem Grubu** bilgilerine dayanarak sevk irsaliye tarihini tahmin eder. Kullanıcıdan gelen veriler işlenir ve eğitilmiş bir **Gradient Boosting Regressor** modeli kullanılarak sevk için kalan gün sayısı tahmin edilir. Bu tahmin edilen gün sayısı mevcut tarihe eklenerek sevk irsaliye tarihi hesaplanır.

## Gerekli Kütüphaneler

Projeyi çalıştırmak için aşağıdaki Python kütüphaneleri gereklidir:

- `pandas`
- `sklearn`
- `datetime`
- `numpy`

Bu kütüphaneleri yüklemek için şu komutu kullanabilirsiniz:


pip install pandas scikit-learn numpy


# Proje Akışı
Kullanıcıdan Veri Alma: Kilo, Metre ve İşlem Grubu bilgileri kullanıcıdan alınır.
## Veri Ön İşleme:
- Kategorik Veriler: İşlem Grubu gibi kategorik veriler Label Encoding ile sayısal değerlere dönüştürülür.
- Sayısal Veriler: Kilo ve Metre gibi sayısal veriler MinMaxScaler kullanılarak ölçeklendirilir.
- Tahmin Yapma: Eğitilmiş Gradient Boosting modeli ile sevk irsaliye tarihine kadar kaç gün kaldığı tahmin edilir.
- Tarih Hesaplama: Mevcut tarihe tahmin edilen gün sayısı eklenerek sevk irsaliye tarihi hesaplanır ve ekrana yazdırılır.
