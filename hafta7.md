Relational database (ilişkisel veritabanı)= verileri tablolar halinde organize eden ve bu tablolar arasında ilişkiler kuran bir veritabanı türüdür.

Tablolar (Tables)= Veriler satır ve sütunlardan oluşan tablolarda saklanır. Her sütun bir özelliği (attribute), her satır ise bir kaydı (record) temsil eder.

İlişkiler (Relationships)= Tablolar arasında bağlantılar kurulur. Örneğin, "Müşteriler" tablosu ile "Siparişler" tablosu birbirine bağlanabilir.

Primary Key (Birincil Anahtar)= Her tabloda kayıtları benzersiz şekilde tanımlayan bir anahtar vardır.

Foreign Key (Yabancı Anahtar)= Tablolar arasındaki ilişkileri sağlamak için kullanılır.

AVANTAJLARI;
✅ Verilerin organize ve yapılandırılmış olması
✅ Veri tutarlılığı (data integrity)
✅ Güvenli sorgu yapısı (SQL)
✅ İlişkiler sayesinde veri tekrarını azaltma

SELECT = Veri tabanından veri çekmek için kullanırız.
SELECT ad, soyad, email FROM musteri; (Müşteri tablosu olarak ad soyad email adresi getir.) eğer orada ad soyad erine * kullansaydım tüm bilgileri getir derdik.

JOIN;
INNER JOIN: Her iki tabloda da eşleşen kayıtlar
LEFT JOIN: Sol tablodaki tüm kayıtlar + eşleşen sağ kayıtlar
RIGHT JOIN: Sağ tablodaki tüm kayıtlar + eşleşen sol kayıtlar
FULL JOIN: Her iki tablodaki tüm kayıtlar

GROUP BY;
COUNT()	Kayıt sayısını hesaplar
SUM()	Toplam değer
AVG()	Ortalama değer
MAX()	En yüksek değer
MIN()	En düşük değer

SELECT musteri_id, COUNT(*) as siparis_sayisi
FROM siparisler
GROUP BY musteri_id; (Her müşterinin tüm siparişlerini gösterir.)

Index Ne İşe Yarar?
Index, veritabanında veri arama hızını artıran bir yapıdır. Kitabın sonundaki "İçindekiler" gibi çalışır.

Avantajları:
✅ Sorgu hızını önemli ölçüde artırır
✅ Arama işlemlerini hızlandırır
✅ WHERE ve JOIN sorgularında performans sağlar.