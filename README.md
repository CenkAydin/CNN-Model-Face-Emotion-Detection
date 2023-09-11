# CNN-Model-Face-Emotion-Detection


## Veri Seti

Notebook dosyasında veri seti olarak FER-2013 kullanılmıştır. (https://www.kaggle.com/datasets/msambare/fer2013)
Veri setindeki "disgust" sınıfı doğruluk oranını düşürdüğü için ve diğer sınıflara göre daha az örnek içerdiği için atılmıştır.

Eğitilen modeli hedefi insan yüzündeki 'angry', 'fear', 'happy', 'neutral', 'sad', 'surprise' duygularını sınıflandırmaktır. 

## Veri Hazırlama

Veriler train, test ve validation olarak bölünmüştür. Bu veriler augmentation işleminden geçirilmiştir. Ayrıca bar grafiği ile sınıflara göz atılmıştır.

## Model Oluşturma

Model convolution, padding, activation, batch normalization, dropout, flatten ve son olarak fully connected katmanlarından oluşturulmuştur. 
Optimizasyon algoritması olarak Adam kullanılmış, 0.0001 öğrenme oranı verilmiştir. Loss function olarak categorical_crossentropy tercih edilmiş ve metrik olarak da accuracy tercih edilmiştir.

## Eğitim

Eğitim için başlangıçta 100 epoch değeri verilmiş ayrıca batch_size 64 olarak belirlenmiştir. Overfitting olmaması için early_stopping eklenmiştir. Eğitimin tamamlanmasının ardından eğitim görselleştirilmiştir. Modeli daha sonra kullanmak amacıyla da kaydetme işlemi yapılmıştır. 

## Test

Test yapmak amacıyla confusion matrix gibi metriklere göz atılmıştır. Ayrıca Webcam ile test yapmak amacıyla en notebook'un en sonuna yüz tanıma + yüzde duygu tanıma yapan hücre eklenmiştir.

