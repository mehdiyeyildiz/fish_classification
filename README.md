# fish_classification

Çalışma dosyama kaggle üzerinden de erişebilirsiniz. [Kaggle Linki](https://www.kaggle.com/code/mehdiyeyldz/fish-classification-2)

### Veri seti ve çalışma amacı
Veri seti 9 farklı balık türünü içeren homojen dağılımlı 9000 görselden oluşmaktadır.
Çalışmada CNN kullanılmadan, yalnızca ANN kullanılarak balık sınıflarının tahmin edilmesi amaçlanmıştır.

### Çalışmamı yürütürken özetle şu adımları izledim:
+ Görselleri okutup X,y alarak özellikler ve hedef değişkeni ayırma,
+ X’leri standartlaştırma.
+ Y hedef değişkenini one-hot encode etme.
+ Veriye shuffle işlemi uygulayıp train, validasyon, test seti ayrımı yapma.
+ Train seti için data augmentation işlemi uygulama.
+ Batch_size=128
+ 7 adet gizli nöron katmanı, her katman için BatchNormalization işlemi ve Dropout(%20) uygulama.
+ Aktivasyon fonksiyonu ReLu, l2 regularizasyonu uygulama.
+ Optimizer Adam(learning_rate=0.0001).
+ early_stopping monitör değeri val_loss olarak alındı.
+ Özellik çıkarma adımları(CNN) uygulanmamıştır. ANN kullanılarak çalışıldı.

### 100 epoch ardından early_stopping’e takılmadan elde edilen değerler:
+ Loss: 1.5233824253082275
+ Accuracy: 0.6951388716697693
+ AUC: 0.9659389853477478

### Test seti için elde edilen sonuçlar:
+ Weighted Precision: 0.7363105882457222
+ Weighted Recall: 0.7111111111111111
+ Weighted F1 Score: 0.7006632692171472
şeklinde gözlemlendi.
