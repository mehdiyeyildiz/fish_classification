# fish_classification

Çalışma dosyama kaggle üzerinden de erişebilirsiniz. [kaggle linki](https://www.kaggle.com/code/mehdiyeyldz/fish-classification-2)

###Çalışmamı yürütürken özetle şu adımları izledim:
1. Görselleri okutup X,y alarak özellikler ve hedef değişkeni ayırma,
2. X’leri standartlaştırma.
3. Y hedef değişkenini one-hot encode etme.
4. Veriye shuffle işlemi uygulayıp train, validasyon, test seti ayrımı yapma.
5. Train seti için data augmentation işlemi uygulama.
6. Batch_size=128
7. 7 adet gizli nöron katmanı, her katman için BatchNormalization işlemi ve Dropout(%20) uygulama.
8. Aktivasyon fonksiyonu ReLu, l2 regularizasyonu uygulama.
9. Optimizer Adam(learning_rate=0.0001).
10. early_stopping monitör değeri val_loss olarak alındı.
11. Özellik çıkarma adımları(CNN) uygulanmamıştır. ANN kullanılarak çalışıldı.

###100 epoch ardından early_stopping’e takılmadan elde edilen değerler:
1. Loss: 1.5233824253082275
2. Accuracy: 0.6951388716697693
3. AUC: 0.9659389853477478

###Test seti için elde edilen sonuçlar:
1. Weighted Precision: 0.7363105882457222
2. Weighted Recall: 0.7111111111111111
3. Weighted F1 Score: 0.7006632692171472
şeklinde gözlemlendi.
