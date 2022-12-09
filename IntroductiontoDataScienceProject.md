# VERİ ÖN İŞLEME

## 1. Veri Seti Analizi

Model eğitimi gerçekleşmeden önce belirli başlıca işlemler vardır. Bu işlemler her zaman
gerçekleştirilir. Çünkü modelin iyi sonuçlar vermesinde yardımcı olmaktadır. İlk olarak veri setinin 
özellikleri (features) hakkında araştırma yapılır. Daha sonra istatiksel özelliklerine bakmak için describe 
fonksiyonu kullanılır. Aşağıdaki örnek bir veri seti için kullanıldı.

![image](https://user-images.githubusercontent.com/116020808/206808432-48df40a9-e9be-46d4-a5ec-698e9dfa8df7.png)

Kullanılan fonksiyon sayesinde veri setinin belirli özelliğinin sayısını, ortalamasını, standart
sapmasını, minimum ve maksimum değerleri hakkında bilgiler edinildi. Özellikler hakkında ek bilgi
olarak seaborn kütüphanesi yardımıyla histogram dağılımına bakılır.

![image](https://user-images.githubusercontent.com/116020808/206808576-4ecbffda-3dc7-4f69-a48c-de0d808f0ab3.png)

Veri seti üzerinde değişiklik yapmadan önce analiz için bakılan başlıca fonksiyonlardan bir diğeri
ise veri setinin ısı haritasını (heatmap) incelemektir. Kullanılan veri setinin özellikleri arasında
korelasyonu incelenir.

![image](https://user-images.githubusercontent.com/116020808/206808720-236d305f-080a-4beb-a83b-fd9f56356387.png)

Bu incelemeler sonrasında birtakım kontroller ve işlemler gerçekleştirilir. İlk bakılacak kontrol veri
setinde eksik veri kontrolüdür. Tüm sütunların kontrolü tek bir fonksiyon ile gerçekleştirilir.

![image](https://user-images.githubusercontent.com/116020808/206808782-d528e839-b3ab-481c-a6a6-a06c0cda0517.png)

Kontrol sonrası eğitilen model algoritmasına göre kaldırabilir ya da farklı bir işlem yapılabilir.
Kaldırılmak istenilirse “dropna” fonksiyonu kullanabilir, yerine değer ile doldurulmak istenilirse
“fillna” fonksiyonu yardımıyla yapılabilir.

## 2. Veri Setlerinin Ölçeklenmesi
Modellerin eğitilmeden önce yapılması gerekenlerde ölçekleme önemli rol oynamaktadır. Verilerin
ölçeklenmesi en doğru model ve analizlerin olmasına yardım eden bir yöntemdir. Başlıca en çok
kullanılan yöntemler;

• Standardizasyon

• Minimum Maksimum Ölçeklendirme

• Mutlak Maksimum Ölçeklendirme

• Normalizasyon

• Binarizasyon

Ölçeklendirme yapmanın en önemli faydası eğitimi daha hızlı hale getirmesidir. Bunun yanında
optimizasyon da yerel minimumda kalmasını önlemektedir. Genellikle büyük fark olan verilerde iyi
iş çıkarmaktadır. 

## 3. Veri Setlerinde Kategorik Verilerin İşlenmesi
Kategorik veriler modellerin eğitiminde hatalar vermesine sebep olmaktadır. Hataların sebebi
modelleri oluşturulurken kullanılan algoritmalarda yapılan matematiksel işlemlerdir. Bundan
kurtulmak için 3 farklı yol bulunmaktadır. İşlem yapılan yollar;

• Label Encoder

• One-Hot Encoder

İşlem yapılmayarak direk o özelliklerin kaldırılmasıdır. Bu yöntemde denilerek özelliklerin model
üzerinde etkisi kontrol edilir. Bu yollardan özelliklerin kaldırılması ve one-hot encoder bazı veri
setlerinde büyük dezavantajları bulunmaktadır. Özelliklerin kaldırılması veri setinde önemli en
etkiye sahip verilerin yok olmasına sebep olurken, one-hot encoder ise sütunda fazla sayıda farklı
değişkenin bulunması durumunda veri setinin anormal şekilde genişlemesine sebep olmaktadır.
Çalışmalar en iyi sonuç veren modeli bulmak için sırayla bu yollar denenmektedir.

## 4. Aykırı Veri Tespit Yöntemleri
Aykırı veri tespiti (Outlier detection) makine öğrenmesinde hatalı verilerin en aza indirilmesi önemli
bir rol oynamaktadır. Aykırı veriler sisteme yanlış kaydedilmesi, sensörlerin yanlış değerler
okuması vb. nedenlerden dolayı veri setine verilerin hatalı aktarılmasından kaynaklanmaktadır. Bu
hatalı veriler modelin eğitiminde sorunlara sebep olur. Çünkü aykırı veriler veri setinin ortalamasına
ve standart sapması üzerinde kötü etki bırakır. Bu sorunu çözmek için istatiksel yöntemler dahil
birçok çözüm yolları vardır. Bazı çözüm yöntemleri;

• IQR Aykırı Veri Tespiti

• Z Skor Yöntemi

• Yerel Aykırı Değer Faktörü (Local Outlier Factor)

• STL Kullanarak Aykırı Veri Tespiti

• Isolation Forest ile Aykırı Veri Tespiti
