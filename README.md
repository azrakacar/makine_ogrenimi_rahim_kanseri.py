# Rahim Ağzı Kanseri Risk Tahmini
Rahim ağzı kanseri,rahimin vajinaya bağlanan alt kısmı olan rahim ağzında gelişen bir kanser türüdür.Bu proje, uterus (rahim) kanseri hastalarına ait klinik ve moleküler verileri kullanarak, tümör sınıflandırması ve sağkalım durumlarını tahmin etmeyi amaçlayan bir makine öğrenmesi çalışmasıdır.Veri seti üzerinde veri temizleme,keşifsel veri analizi(EDA) eksik veri tamamlama (imputation), dengesiz sınıf yönetimi (SMOTE) ve özellik mühendisliği adımları uygulanmıştır. Model olarak, mesafe tabanlı bir algoritma olan K-Nearest Neighbors (KNN) tercih edilmiştir.

Kullanılan Teknolojiler ve Kütüphaneler:Veri Analizi: Pandas, NumPy, Görselleştirme: Matplotlib, Seaborn, Missingno (Eksik veri analizi için), Makine Öğrenmesi: Scikit-Learn, Veri Önişleme: IterativeImputer, MinMaxScaler, LabelEncoder, Dengesiz Veri (Imbalanced Data): Imbalanced-learn (SMOTE, NearMiss)

Veri Seti ve Önişleme:
Projede odaklanılan temel özellikler şunlardır: Klinik Veriler: Teşhis Yaşı, Sağkalım Durumu, Hastalıksız Sağkalım. Moleküler Veriler: MSI MANTIS Skoru, MSIsensor Skoru, Mutasyon Sayısı, Genom Değişim Oranı. Sınıflandırma: Histopatolojik ve Moleküler tümör sınıflandırmaları.

Modelin genelleme yeteneğini ölçmek adına veri seti %70 eğitim ve %30 test olacak şekilde ayrılmıştır. Rastgelelik etkisini sabitlemek için random_state=100 kullanılmıştır.

Veri Dağıtım Analizi:Sayısal özelliklerin dağılımı incelenmiştir. Özellikle Mutation Count ve MSI Score gibi değişkenlerdeki yoğunlaşmalar, modelin bu özellikleri nasıl işleyeceği konusunda kritik ipuçları sunmaktadır. Dağılımların farklı ölçeklerde olması nedeniyle modele giriş öncesi MinMaxScaler uygulanmıştır.



