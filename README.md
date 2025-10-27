# Cat_and_Dog_CNN

Bu proje, **Convolutional Neural Network (CNN)** kullanılarak kedi ve köpek görsellerinin sınıflandırılmasını amaçlamaktadır.  
Proje Akbank Derin Öğrenme Bootcamp: Yeni Nesil Proje Kampı kapsamında geliştirilmiştir.
---
##  Veri Seti
- Kullanılan veri seti: https://www.kaggle.com/datasets/tongpython/cat-and-dog 
- Görseller eğitim ve test seti olarak ikiye ayrılmıştır.

---

##  Model
- CNN tabanlı bir model tasarlanmıştır.
- Eğitim süresince **train/validation accuracy** ve **loss** değerleri takip edilmiştir.

---

##  Eğitim Süreci

Aşağıdaki grafiklerde modelin epoch=50 ve batch=32 boyunca gösterdiği performans yer almaktadır:

- **Model Değerlendirilmesi**
<img width="1489" height="490" alt="download" src="https://github.com/user-attachments/assets/b0de1b04-88b5-4867-9c7d-c93c975772f0" />


## Sonuçlar

**Confusion Matrix:**

<img width="649" height="548" alt="download" src="https://github.com/user-attachments/assets/5552c292-e758-4cf0-b81d-956c30a0e626" />



**Classification Report:**

                precision    recall  f1-score   support

        Cat     0.75      0.85      0.79      1011
       Dog       0.82      0.72      0.77      1012

      accuracy                           0.78      2023
    macro avg       0.79      0.78      0.78      2023
    weighted avg       0.79      0.78      0.78      2023
 
---

## Grad-CAM Analizi

Grad-CAM, modelin hangi bölgeleri dikkate alarak karar verdiğini görselleştirmektedir.

Örnek görseller:  

<img width="1117" height="683" alt="image" src="https://github.com/user-attachments/assets/0fb1dd89-be3a-4f6b-b7e7-ad8d80801775" />
<img width="1104" height="697" alt="image" src="https://github.com/user-attachments/assets/d67072e8-d946-4dee-9e46-a0b992c16d14" />



- Köpek görsellerinde kafa ve gövde bölgeleri öne çıkmıştır.  
- Kedi görsellerinde ise yüz kısmı daha çok dikkate alınmıştır.  

---

## Yorumlar
- Model, temel ayırt edici özellikleri öğrenmiştir.
- Batch sayısı büyüdükçe her güncelleme daha az adım sayısına sahip olduğu için öğrenme durumu daha dalgalı hale gelmiştir.
- Epoch sayısı çok küçük olduğunda model yeterince öğrenemedi ve hatalı yanıtlar verdi.
- Epoch sayısı çok büyük olunca program aşırı yavaş çalıştı ve yine hatalı cevap verme oranı arttı.
- Veri artırımı (Data Augmentation), daha derin CNN mimarileri veya Transfer Learning ile başarı artırılabilir.  

---

## Gelecek Çalışmalar
- **Transfer Learning**: VGG16, ResNet, EfficientNet gibi hazır mimariler kullanılabilir.  
- **Veri Seti**: Daha dengeli ve geniş veri setleri ile performans artırılabilir.  
- **Deployment**: Streamlit veya Flask ile kullanıcı arayüzü eklenip proje deploy edilebilir.  

---

## Linkler
  [https://www.kaggle.com/code/aysenciftci/cat-and-dog-cnn/edit](https://www.kaggle.com/code/aysenciftci/cat-and-dog-cnn)

---
 Lisans: MIT  
