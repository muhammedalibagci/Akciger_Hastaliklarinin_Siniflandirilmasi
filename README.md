İleri Python Proje EfficientNetB0 ile Akciğer Hastalıkları Sınıflandırma Sistemi Veri seti: Kaggle - Göğüs Röntgeni Veri Seti

Projenin Genel Amacı Bu projede, EfficientNetB0 tabanlı bir derin öğrenme modeli, akciğer röntgen görüntülerinden bakteriyel pnömoni, korona virüsü (COVID-19), normal, tüberküloz ve viral pnömoni olmak üzere beş farklı listede sınıflandırılması.
Modelin öğrenmesi ve genelleme başarısı, veri iyileştirme teknikleri, sınıf dengesizliklerini azaltan stratejiler ve rejim yöntemleriyle güçlendirilir. Projenin temel hedefi, sağlık alanında doğru ve hızlı tanı desteği sunabilecek bir yapay zeka sistemi geliştirmektir.

Kullanılan Teknolojiler ve Kütüphaneler Python: Projenin temel programlama dili.
TensorFlow & Keras: Derin öğrenme modeli oluşturma ve eğitme.

Pandas & NumPy: Veri işleme ve düzenleme işlemleri için.

Matplotlib & Seaborn: Görselleştirme (doğruluk, kayıp grafikleri, karışıklık matrisi).

Scikit-learn: Sınıflandırma raporu ve F1-score hesaplamaları için.

OpenCV/PIL: Görüntü işleme işlemleri.

Dengesiz öğrenme: Sınıf ağırlıkları ve kontrol teknikleri.

Google Colab / Jupyter Notebook: Geliştirme ortamı.

OS & glob: Dosya işletmeleri için.

Kodun Ana Bölümleri a. Veri Ön İşleme Görüntüler yeniden boyutlandırıldı (224x224).
Normalize edildi (0-1 aralığına).

Etiketler, one-hot kodlama yöntemiyle dönüştürüldü.

B. Model Mimarisi: EfficientNetB0 ImageNet ağırlıklarıyla birlikte sınıflandırılmış EfficientNetB0 modeli kaydedildi.

Üst katmanlar özelleştirildi: GlobalAveragePooling, Dense, Dropout ve Softmax katmanları eklendi.

C. Eğitim Stratejisi Kayıp fonksiyonu: Kategorik Krosentropi.

Optimizasyon: SGD (düşük öğrenme oranı), momentum.

Regularizasyon: Dropout ve Gradient Clipping'i uygulayabilirsiniz.

EarlyStopping & ModelCheckpoint callback'leri ile eğitim optimize edildi.

D. Performans Ölçümü Doğruluk, kesinlik, geri çağırma, F1 skoru gibi metrikler hesaplandı.

Karışıklık matrisi ile modelin sınıflar arası başarı oranları analiz edildi.

e. Veri Artırma ve Sınıf Dengesi ImageDataGenerator ile döndürme, yakınlaştırma, yansıma gibi veri artırma işlemlerinin yapılması.

Sınıf ağırlığı hesaplanmış ve dengesiz sınıflar için eğitim sırasında ağırlıklar azaltılmıştır.

Projenin İşleyişi Görüntü Verisi ile Eğitimi Başlat Kullanıcı, etiketlenmiş veri setini sağlar.

Model, eğitim süreci süreci boyunca görüntüler.

Yeni Görüntü Sınıflandırma Kullanıcı, yeni bir röntgen görüntüsü yüklediğinde modelin sınıflandırarak hangi aralıklara ait olduğunu tahmin eder.

Sonuçların Görselleştirilmesi Eğitim ve kayıp kaybı ile doğruluk grafikleri.

Karışıklık matrisi ve sınıf tabanlı başarı metrikleri görselleştirilir.

Sonuç Bu proje, veriye dayalı bir derin terapi tedavisi ile akciğer hastalıklarının otomatik olarak sınıflandırılmasını hedefledi. EfficientNetB0 mimarisi sayesinde düşük donanımda bile yüksek doğrulukta sonuçlar elde edilmiştir.
En yüksek başarı tüberküloz sınıfında gözlenmiştir. Benzer görsel yapıya sahip viral ve bakteriyel pnömoni sınıflarında karışıklık yaşanmış, bu durum ileride daha fazla örnekle ve farklı mimarilerle iyi seçilebilir.

Bu proje, tedavi alanında görüntülemenin etkili ve optimize edilmiş bir karar destek sistemi olarak değerlendirilebilir.
