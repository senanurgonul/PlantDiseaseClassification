# 🌿 PlantDiseaseClassification

Bu proje, bitki yaprakları üzerindeki hastalıkları görüntü sınıflandırma teknikleri ile otomatik olarak tespit etmeye yönelik geliştirilmiştir. Derin öğrenme yöntemleri ve transfer öğrenme yaklaşımları kullanılarak görsel veriden hastalık sınıflandırması yapılmıştır.

---

## 🎯 Projenin Amacı

Tarım alanında yaygın olan bitki hastalıklarının zamanında tespiti, ürün verimliliği ve tarımsal sürdürülebilirlik açısından büyük önem taşımaktadır. Bu projede, yaprak görüntüleri üzerinden bitkilerdeki hastalıkları sınıflandıran bir yapay zeka sistemi oluşturulması hedeflenmiştir.

---

## 🗂️ Kullanılan Veri Seti

- **Veri seti kaynağı:** [PlantVillage Dataset](https://www.kaggle.com/datasets/emmarex/plantdisease)
- Görseller çeşitli hastalık tiplerini ve sağlıklı yaprakları içermektedir.
- Toplamda 4 sınıfa ait görüntüler kullanıldı.
- Görseller eğitim öncesinde yeniden boyutlandırıldı ve normalize edildi.

---

## 🔧 Uygulama Adımları

1. **Veri Hazırlama:**
   - Görseller `train`, `validation` ve `test` olarak üçe ayrıldı.
   - Görsellerin boyutu sabitlenerek modele uygun hale getirildi.
   - `ImageDataGenerator` ile veri arttırma (augmentation) uygulandı.

2. **Modelleme:**
   - Üç farklı modelle çalışıldı:
     - **Özel Tasarım CNN**: Katmanları sıfırdan tasarlandı.
     - **VGG16 (Transfer Learning)**: Önceden eğitilmiş model kullanıldı.
     - **EfficientNetB0 (Transfer Learning)**: Daha az parametre ile hızlı eğitim sağladı.
   - Her model için `Adam` optimizer, `categorical_crossentropy` loss fonksiyonu kullanıldı.

3. **Eğitim Süreci:**
   - Modeller `Google Colab` üzerinde GPU desteğiyle eğitildi.
   - Epoch sayısı, batch size ve öğrenme oranları modele göre optimize edildi.
   - Eğitim sırasında kayıp ve doğruluk değerleri takip edildi.

4. **Değerlendirme:**
   - Eğitim ve doğrulama doğrulukları karşılaştırılarak overfitting kontrol edildi.
   - Confusion matrix ve sınıf bazlı başarı oranları analiz edildi.

---

## 🧰 Kullanılan Kütüphaneler

- Python
- TensorFlow / Keras
- OpenCV
- Matplotlib, NumPy
- Scikit-learn

---
