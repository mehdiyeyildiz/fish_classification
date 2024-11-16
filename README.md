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
+ Train seti için data augmentation işlemi uygulanmadı. Çünkü öğrenme sürecini olumsuz etkiledi.
+ Batch_size=128
+ 5 adet gizli nöron katmanı, her katman için BatchNormalization işlemi ve Dropout(0.2) uygulama.
+ Aktivasyon fonksiyonu ReLu, l2 regularizasyonu uygulama.
+ Optimizer Adam(learning_rate=0.0001).
+ early_stopping monitör değeri val_loss olarak alındı.
+ Özellik çıkarma adımları(CNN) uygulanmamıştır. ANN kullanılarak çalışıldı.

### 100 epoch ardından early_stopping ile 40. epoch için elde edilen değerler:
+ Loss: 1.3800170421600342
+ Accuracy: 0.8993055820465088
+ AUC: 0.9909536838531494

### Test seti için elde edilen sonuçlar:
+ Weighted Accuracy: 0.8883333333333333
+ Weighted Precision: 0.9043748810777505
+ Weighted Recall: 0.8883333333333333
+ Weighted F1 Score: 0.8903298544137181
şeklinde gözlemlendi.
