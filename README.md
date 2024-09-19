# Asteroids

## Giriş
Bu proje, Nearest Earth Objects(1910-2024) veri setini kullanarak çeşitli makine öğrenimi ve derin öğrenme modellerinin performansını değerlendirmeyi amaçlamaktadır. Nearest Earth Objects(1910-2024) veri seti, 338.199 tane veriden oluşur. Modeller doğruluk, hassasiyet, geri çağırma, F1 puanı gibi metrikler kullanılarak değerlendirilir.

## Modeller ve Performansları
### Gözetimli Öğrenme Algoritmaları
#### Random Forest
##### Neden Uygun Olabilir:
##### Yüksek Doğruluk: Sınıflandırma ve regresyon problemlerinde yüksek doğruluk oranları sağlar.
##### Öznitelik Önem Derecelendirmesi: Özelliklerin ne kadar önemli olduğunu belirlemek için kullanılabilir, bu da modelin anlaşılmasını kolaylaştırır.
##### Çeşitli Verilere Uyum Sağlama: Hem sürekli hem de kategorik verilerle iyi çalışır.
- **Accuracy(Doğruluk):** 98%
- **Precision(Kesinlik):** 94%
- **Recall(Duyarlılık):** 90%
- **F1-Score(F1-Skoru):** 92%

#### Random Forest Regressor
##### Neden Uygun Olabilir:
##### Aşırı Öğrenmeyi Azaltma: Birden fazla karar ağacının birleşimi, modelin aşırı öğrenme riskini azaltır ve genel performansı artırır.
##### Robust ve Esnek: Özellikle karmaşık ilişkileri öğrenmede başarılıdır ve çok boyutlu verilerle iyi çalışır.
- **Çapraz Doğrulama Skorları (Negatif MSE):** [-0.02145228 -0.02151575 -0.02131142 -0.02126772 -0.02140523]
- **Ortalama Çapraz Doğrulama Skoru (Negatif MSE):** -0.02139048015127403 
- **Fitting 5 folds for each of 36 candidates, totalling 180 fits**
- **En İyi Hiperparametreler:** {'max_depth': None, 'min_samples_split': 2, 'n_estimators': 200}
- **Ortalama Karesel Hata (MSE):** 0.01803394876912841
- **Ortalama Mutlak Hata (MAE):** 0.05067975160789532
- **R-Kare (R²) Skoru:** 0.8366493653805481

### Gözetimsiz Öğrenme Algoritmaları
#### K-Means
##### Neden Uygun Olabilir: 
##### Kümeleme Görevleri İçin: K-Means, etiketlenmemiş veri kümesi üzerinde çalışarak doğal veri gruplarını belirlemenizi sağlar.
##### Basit ve Hızlı: Hesaplama maliyeti görece olarak düşüktür, bu nedenle büyük veri setlerinde hızlı bir şekilde çalışabilir.
 - **k=2 için Silhouette Skoru:** 0.26243137977962455
 - **k=2 için Davies-Bouldin Skoru:** 1.4532705750202262
 - **k=2 için Calinski-Harabasz Skoru:** 24850.55953990036
 - **k=2 için Inertia:** 1238498.0294166335
 - **k=3 için Silhouette Skoru:** 0.2619930060273644
 - **k=3 için Davies-Bouldin Skoru:** 1.4556209605724961
 - **k=3 için Calinski-Harabasz Skoru:** 24858.229990747608
 - **k=3 için Inertia:** 1064219.3090256937
 - **k=4 için Silhouette Skoru:** 0.29154190859661533
 - **k=4 için Davies-Bouldin Skoru:** 1.2852736935521019
 - **k=4 için Calinski-Harabasz Skoru:** 24506.74202552871
 - **k=4 için Inertia:** 845755.7322087944
 - **k=5 için Silhouette Skoru:** 0.2864132210977454
 - **k=5 için Davies-Bouldin Skoru:** 1.1788905185729415
 - **k=5 için Calinski-Harabasz Skoru:** 23775.537603551886
 - **k=5 için Inertia:** 707519.0918807951
 - **k=6 için Silhouette Skoru:** 0.2627995619385045
 - **k=6 için Davies-Bouldin Skoru:** 1.1493767259970908
 - **k=6 için Calinski-Harabasz Skoru:** 22990.96680505978
 - **k=6 için Inertia:** 617242.7820044702
 - **k=7 için Silhouette Skoru:** 0.2609579430435438
 - **k=7 için Davies-Bouldin Skoru:** 1.1332847269189055
 - **k=7 için Calinski-Harabasz Skoru:** 21885.29371018776
 - **k=7 için Inertia:** 557597.3246596985
 - **k=8 için Silhouette Skoru:** 0.2571250760633941
 - **k=8 için Davies-Bouldin Skoru:** 1.0923053996583818
 - **k=8 için Calinski-Harabasz Skoru:** 20818.341181135158
 - **k=8 için Inertia:** 512420.2826702844
 - **k=9 için Silhouette Skoru:** 0.25568476206539603
 - **k=9 için Davies-Bouldin Skoru:** 1.071328915480513
 - **k=9 için Calinski-Harabasz Skoru:** 19999.0313404369
 - **k=9 için Inertia:** 476265.32362160395
 - **k=10 için Silhouette Skoru:** 0.24980952353161134
 - **k=10 için Davies-Bouldin Skoru:** 1.0926866138017723
 - **k=10 için Calinski-Harabasz Skoru:** 18841.848191923782
 - **k=10 için Inertia:** 453152.63685881987
 - **En İyi k Değeri (Silhouette Skoru):** 4
 - **En İyi k Değeri (Davies-Bouldin Skoru):** 9
 - **En İyi k Değeri (Calinski-Harabasz Skoru):** 3
 - **En İyi k Değeri (Inertia):** 10
 - **En İyi k-Değeri ile Silhouette Skoru:** 0.29154190859661533
 - **En İyi k-Değeri ile Davies-Bouldin Skoru:** 1.2852736935521019
 - **En İyi k-Değeri ile Calinski-Harabasz Skoru:** 24506.74202552871
 - **En İyi k-Değeri ile Inertia:** 845755.7322087943

## Kaggle Linki
https://www.kaggle.com/datasets/oruntrkokulolu/asteroids
