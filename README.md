# Vehicle Price Prediction 🚗

Hi.In this project, I built a machine learning model to predict used car prices based on features like fuel type, transmission, and color. My main focus was on data cleaning and preventing data leakage.

## What I Did

* **Preventing Data Leakage:** I split the data into `X_train` and `X_test` *first*. After that, I filled the missing values. I used the median for numerical columns and the mode for categorical columns.
* **Feature Engineering:** I grouped some columns like `Fuel Type` and `Color` to keep things simple. Also, I mapped text values to numbers (for example Manual: 0, Automatic: 1).
* **Encoding:** Used `pd.get_dummies` for the rest of the categorical data.

## Model & Results

I used **Decision Tree Regressor** for this project. 

To make sure my model doesn't overfit, I used `GridSearchCV` to find the best parameters. Finally, I tested the real performance with **5-Fold Cross Validation** using the combined clean data.

* **My Average R2 Score:** **~0.874**

## Files in this Repository
* `vehicle_price_model.ipynb`: My main code with data cleaning, EDA, and modeling.
* `processed_vehicles_data.csv`: The final, cleaned dataset.
* `requirements.txt`: Libraries you need to run the code.

---
*Mustafa Kılıç - 3rd Year Computer Engineering Student*


# Araç Fiyat Tahmini 🚗

Merhaba.Bu projede, yakıt tipi, vites türü ve renk gibi özelliklere dayanarak ikinci el araç fiyatlarını tahmin eden bir makine öğrenmesi modeli geliştirdim. Temel odak noktam veri temizliği ve veri sızıntısını (data leakage) önlemekti.

## Neler Yaptım?

* **Veri Sızıntısını Önleme:** Veriyi *ilk önce* `X_train` ve `X_test` olarak ikiye böldüm. Daha sonra eksik verileri doldurdum. Sayısal kolonlar için medyan (ortanca), kategorik kolonlar için ise mod (en çok tekrar eden) değerlerini kullandım.
* **Özellik Mühendisliği (Feature Engineering):** İşleri sade tutmak için `Fuel Type` ve `Color` gibi bazı kolonları gruplandırdım. Ayrıca, metin değerlerini sayılara çevirdim (örneğin Manual: 0, Automatic: 1).
* **Encoding:** Geriye kalan kategorik veriler için `pd.get_dummies` kullandım.

## Model ve Sonuçlar

Bu proje için **Decision Tree Regressor (Karar Ağacı)** kullandım. 

Modelimin ezberleme (overfitting) yapmadığından emin olmak için `GridSearchCV` kullanarak en iyi parametreleri buldum. Son olarak, birleştirilmiş temiz veri üzerinde **5 Katlı Çapraz Doğrulama (5-Fold Cross Validation)** ile modelin gerçek performansını test ettim.

* **Ortalama R2 Skorum:** **~0.874**

## Bu Repodaki Dosyalar
* `vehicle_price_model.ipynb`: Veri temizleme, EDA (Keşifçi Veri Analizi) ve modelleme işlemlerini içeren ana kodum.
* `processed_vehicles_data.csv`: Temizlenmiş ve son haline getirilmiş veri seti.
* `requirements.txt`: Kodu çalıştırmak için gerekli kütüphaneler.

---
*Mustafa Kılıç - 3. Sınıf Bilgisayar Mühendisliği Öğrencisi*
