# Cat_and_Dog_CNN

Bu proje, **Convolutional Neural Network (CNN)** kullanılarak kedi ve köpek görsellerinin sınıflandırılmasını amaçlamaktadır.  
Proje Global AI Hub bootcamp kapsamında geliştirilmiştir.
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

- **Model Accuracy**
- <img width="723" height="575" alt="image" src="https://github.com/user-attachments/assets/93add844-27a8-4090-a703-04cb49261ab0" />

- **Model Loss**
- <img width="723" height="572" alt="image" src="https://github.com/user-attachments/assets/dd5165d3-6bf8-421d-9456-6b83a282b171" />
---

## Sonuçlar

**Confusion Matrix:**
<img width="810" height="686" alt="image" src="https://github.com/user-attachments/assets/f775e276-0462-4e48-8906-5605aaee16de" />


**Classification Report:**

                 precision    recall  f1-score   support
              
         Cat       0.48      0.43      0.46      1011
         
         Dog       0.49      0.54      0.51      1012
         
    accuracy                           0.49      2023
    
    macro avg       0.49      0.49      0.48      2023
   
    weighted avg       0.49      0.49      0.48      2023

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
- Model, temel ayırt edici özellikleri öğrenmiştir ancak doğruluk oranı %46 seviyesinde kalmıştır.
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
