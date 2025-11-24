# TechIstPyBootcampProje_Titanic_Veri_Analizi_Raporu

# 🚢 Titanic Veri Analizi ve Makine Öğrenmesi (Core Integration Project)

Bu depo, ünlü Titanic veri setini kullanarak temel veri bilimi, veri görselleştirme ve makine öğrenmesi tahmin modellerini uygulayan bir **Temel Entegrasyon Projesi**'dir. Proje, Pandas, Seaborn ve Scikit-learn kütüphanelerinin temel kullanımını sergilemeyi amaçlamaktadır.

## 🎯 Proje Amacı

Projenin temel hedefleri şunlardır:

1.  **Veri Temizliği:** Eksik verileri (özellikle `Age` sütununu **medyan** ile) doldurmak ve veri setini analize hazırlamak.
2.  **Keşifçi Veri Analizi (EDA):** Hayatta kalma oranlarını `Sex` (Cinsiyet) ve `Pclass` (Yolcu Sınıfı) gibi önemli değişkenlere göre incelemek.
3.  **Görselleştirme:** Elde edilen bulguları Seaborn kütüphanesi ile Countplot ve Boxplot kullanarak görselleştirmek.
4.  **Tahmin Modellemesi:** Yolcuların hayatta kalıp kalmayacağını tahmin etmek için bir Makine Öğrenmesi modeli (Genellikle **Random Forest** veya **Logistic Regression**) oluşturmak.

## ⚙️ Teknolojiler ve Kütüphaneler

Bu projede kullanılan temel araç ve kütüphaneler:

* **Python 3.x**
* **Pandas:** Veri manipülasyonu ve temizliği.
* **NumPy:** Sayısal işlemler.
* **Matplotlib/Seaborn:** Veri görselleştirme.
* **Scikit-learn:** Veri bölme (`train_test_split`) ve Makine Öğrenmesi algoritmaları (`RandomForestClassifier`, `LogisticRegression`).
* **XGBoost:** (Opsiyonel olarak dahil edilebilir) Gelişmiş sınıflandırma modeli.

## 📂 Dosya Yapısı
├── titanickagglev4.ipynb # Temel veri analizi ve makine öğrenmesi kodu ├── titanic.csv # Eğitim veri seti (Gerekli)

## ✅ Temel Analiz ve İşlemler

Aşağıdaki adımlar not defteri (`titanickagglev4.ipynb`) içinde gerçekleştirilmiştir:

### 1. Veri Ön İşleme ve Temizleme

* Eğitim ve Test veri setleri yüklendi.
* Eksik **`Age`** değerleri, veri setindeki yaşın **medyanı** ile dolduruldu.
* `Fare`, `Embarked` gibi diğer önemli sütunlardaki eksik değerler ele alındı.
* `Sex`, `Embarked`, `Pclass` gibi kategorik değişkenler makine öğrenmesi için sayısal formatlara dönüştürüldü (Label Encoding / One-Hot Encoding).

### 2. İstatistiksel Hesaplamalar

* **`Sex`** ve **`Pclass`**'a göre hayatta kalma oranları (`Survived` ortalaması) **`groupby()`** fonksiyonu kullanılarak hesaplandı.

### 3. Zorunlu Görselleştirmeler

| Grafik Türü | İlişki | Açıklama |
| :--- | :--- | :--- |
| **Seaborn Countplot** | Cinsiyet ve Hayatta Kalma | Kadın ve erkeklerin hayatta kalma sayılarını karşılaştırır. |
| **Seaborn Boxplot** | Pclass ve Fare | Yolcu sınıfına göre ödenen ücret dağılımını gösterir (Sınıf 1'in en yüksek ücreti ödediği beklenir). |

### 4. Makine Öğrenmesi

* Özellikler (`X`) ve hedef değişken (`y`) tanımlandı.
* Veri seti eğitim ve test setlerine ayrıldı.
* **RandomForestClassifier** ve/veya **LogisticRegression** modelleri eğitildi.
* Model tahminleri (`y_pred`) oluşturuldu ve Kaggle formatında CSV dosyası olarak kaydedildi.

## 🚀 Nasıl Çalıştırılır?

Projeyi yerel ortamınızda veya Google Colab/Jupyter'da çalıştırmak için aşağıdaki adımları izleyin:

1.  **Depoyu Klonlayın:**
    ```bash
    git clone [https://github.com/KULLANICI_ADINIZ/REPO_ADINIZ.git](https://github.com/KULLANICI_ADINIZ/REPO_ADINIZ.git)
    cd REPO_ADINIZ
    ```
2.  **Veri Setini Edinin:** `titanic.csv` dosyasını (train veri seti) aynı dizine yerleştirin. Bu dosya Kaggle'dan temin edilebilir.
3.  **Kütüphaneleri Yükleyin:** Gerekli tüm Python kütüphanelerini kurun.
    ```bash
    # XGBoost'u da dahil ediyoruz
    pip install pandas numpy matplotlib seaborn scikit-learn xgboost
    ```
4.  **Notebook'u Çalıştırın:** `titanickagglev4.ipynb` dosyasını açın ve tüm hücreleri sırasıyla çalıştırın.

## 📧 Katkıda Bulunma

Bu projenin geliştirilmesine katkıda bulunmak isterseniz, lütfen bir Pull Request (Çekme İsteği) açmaktan çekinmeyin!
