API nedir, neden var?
iki farklı yazılımın birbiriyle iletişim kurmasını sağlayan bir arayüzdür. 
API, bir programın verilere, sunucu yazılımına veya diğer programlara ulaşabilmek için kullandığı bir bağlantı arayüzüdür. İki makinenin nasıl konuştuğunu belirleyen bir dizi kuralları içerir. Örneğin, bir E-ticaret sitesi, API sayesinde bir bankanın verdiği kredi kartından para çekilmesine izin vererek alışveriş yapılmasını sağlayabiliyor.
API Nasıl Çalışır?
API’ler yazılımlar veya veri tabanları arasında güvenli ve kontrollü bir kapı açmaya yarayan uygulama arayüzüdür. 

API’nin çalışma şekli aşağıdaki gibidir.

Alıcı program bir istek (API Çağrısı) yapar. Bu istek URI aracılığıyla Web sunucusuna istek fiili olarak işlenir. 
İstek alındıktan sonra API, harici program veya web sunucusuna çağrıda bulunur. 
Sunucu istenen bilgileri API’ye bir yanıt olarak gönderir. 
API, isteği yapan alıcı programa aldığı verileri aktarır. 

GET(VERİ ALMAK) – POST(VERİ EKLEMEK) – PUT(GÜNCELLE) – DELETE(SİL)

JSON NEDİR?
JSON = Veriyi düzenli şekilde saklama ve gönderme biçimidir.

Yani API’nin bize veri yollarken kullandığı kutu gibi düşün.
İnsanlar, bilgisayarlar, frontend veya backend fark etmez; JSON hepsiyle anlaşır.

{
  "ad": "Rona",
  "meslek": "Programcı",
  "yas": 26 BUNU 
}

Açalım:

"ad" → anahtar (etiket)
"Rona" → değer
"meslek" → anahtar
"Programcı" → değer
"yas" → anahtar
26 → değer (number, yani sayı)

JSON’UN ÖZELLİKLERİ
Süslü parantez { } → obje (bir kişi, bir ürün)
Köşeli parantez [ ] → liste (birden fazla kişi, ürün)
Anahtarlar ve string değerler tırnak içinde olmalı
Virgül , → birden fazla veri ayırır.

Örnek;

[
  { "ad": "Rona", "yas": 26 },
  { "ad": "gökçe", "yas": 25 }
]

Endpoint = API’nin belirli bir işlevi yapan URL’si / yolu

/users → kullanıcı listesi
/products → ürün listesi
/orders → sipariş listesi

Her endpoint’in ne yaptığı HTTP method’la belli olur:

💥 KISA ÖZET (AKLINA KAZI)

✔️ API = uygulamalar arası köprü
✔️ GET = veri al
✔️ POST = veri ekle
✔️ PUT = güncelle
✔️ DELETE = sil
✔️ JSON = veri formatı
✔️ REST = düzenli API yazma sistemi
