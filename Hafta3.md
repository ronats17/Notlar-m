## Ip Nedir?##
İnternet'e bağlanan her cihaza, İnternet Servis Sağlayıcısı tarafından bir "public" IP adresi atanır ve internete bağlı cihazlar birbirleriyle bu "public" IP adresleri üzerinden ulaşırlar. IP adresine sahip iki farklı cihaz aynı ağda olmadıkları durumlarda, yönlendiriciler (router) ya da yönlendirme (routing) özelliği olan cihazlar vasıtası ile birbirleri ile iletişim kurarlar.

## Port Nedir?##
Port; bilgisayarlar arası iletişimi sağlayan ve bu iletişimde köprü görevi gören bir teknolojidir.

İnsanların birbirleriyle iletişim kurabilmelerini sağlayan telefon numaraları gibi bilgisayarların da bağlı oldukları internet ağı aracılığı ile birbirleriyle iletişim kurmak üzere kullandıkları birer dinamik veya statik IP adresi bulunur.

## Domain Name System (DNS) Nedir##
İnternet uzayını bölümlemeye, bölümleri adlandırmaya ve bölümler arası iletişimi organize etmeye yarayan, bilgisayar, servis, internet veya özel bir ağa bağlı herhangi bir kaynak için hiyerarşik dağıtılmış bir adlandırma sistemidir.

İnternet ağını oluşturan her birim sadece kendine ait bir IP adresine sahiptir. Bu IP adresleri kullanıcıların kullanımı için www.site_ismi.com gibi kolay hatırlanır adreslere karşılık düşürülür. DNS sunucuları, internet adreslerinin IP adresi karşılığını kayıtlı tutmaktadır.

## TCP Nedir?##
TCP, verilerin güvenli, sıralı ve eksiksiz iletilmesini sağlayan bir iletişim protokolüdür.
İlk ağ implementasyonunda, İnternet Protokolü (IP) ile birlikte çalışarak TCP ortaya çıkmıştır. Bu nedenle, tüm takım genellikle TCP/IP olarak adlandırılır. TCP, IP ağı üzerinden iletişim kuran uygulamalar arasında bir dizi oktetin (baytların) güvenilir, sıralı ve hata kontrolü yapılmış bir şekilde iletimini sağlar.

## UDP Nedir?##
Gelişmiş bilgisayar ağlarında paket anahtarlı bilgisayar iletişiminde bir datagram modu oluşturabilmek için UDP protokolü yazılmıştır. Bu protokol minimum protokol mekanizmasıyla bir uygulama programından diğerine mesaj göndermek için bir prosedür içerir. Bu protokol 'transaction' yönlendirmelidir. Paketin teslim garantisini isteyen uygulamalar TCP protokolünü kullanır.

Geniş alan ağlarında (WAN) ses ve görüntü aktarımı gibi gerçek zamanlı veri aktarımlarında UDP kullanılır.

## Paket Yapısı Nedir?​##
Java’da proje oluştururken özellikle büyük ve kapsamlı projelerde sınıflar mantıksal ve yapısal durumlarına göre farklı paketler altında tutulurlar. Paket Yapısı kullanılması hem kodun daha düzenli olmasını hem kullanımın kolay olmasını hem de sınıfların birbirleriyle iletişimlerinde meydana gelecek sınırlandırmaların ayarlanabilmesini sağlarlar. Paket yapısı aslında Java içerisinde dosya yolu tanımlamaktır. Oluşturduğumuz sınıfları farklı paketler altına koymak aslında bu sınıfları farklı dosya yolları içerisine kaydetmek demektir. Bu dosya yollarıyla Java hangi sınıfa nereden erişeceğini rahat bir şekilde anlayabilir. Ayrıca farklı paketler altında sınıf oluştururken aynı isimler kullanılabilir.​

## Java’da Paket Yapısı​##
Java’da paket yapısı kullanılırken çoğunlukla domain ismi baz alınır ve bu domain ismi üzerinden isimlendirme yapılır. 

## PİNG Nedir?##
Ping programı, 1983 yılında Mike Muuss tarafından yazılmış bir programdır. Çalışma prensibi hedefe 64 baytlık bir ICMP paketi göndermek ve aynı paketin geri gelmesini beklemek üzerine kuruludur. Sunucu istemciye ne kadar uzak ise, bekleme süresi o kadar artmaktadır.

Örneğin;
Türkiye'deki bir kaynaktan Türkiye'deki bir hedefe ping yollayan bir istemci geri dönüş alabilmesi için 3 saniye beklerken, aynı istemci Almanya'daki bir hedefe ping yolladığında 5 saniye bekleyebilir.

## 🌍 Traceroute Nedir?##

Traceroute, bir verinin bilgisayarından çıkıp hedef sunucuya gidene kadar
hangi cihazlardan (router’lardan) geçtiğini gösteren komuttur.
Yani internet yol haritası 🗺️

### Ne İşe Yarar?###

- ** İnternet yavaşsa nerede sorun var gösterir 
- ** Hangi ülkelerden / hangi ağlardan geçtiğini gösterir
- ** Paketlerin kaç “durak” (hop) yaptığını gösterir

Nslookup Komutu Nedir?: Dns Serverin Düzgün çalışıp çalışmadığı kontrol etmek için kullanılır.

## Nslookup Komutu Nedir?##
Bu Komut Nasıl  Çalışır?: Bunun için Win + R tuşları ile birlikte basılır (Veya  başlat menüsünde arama kısmına Çalıştır yazarak da ulaşılabilirsiniz). Çalıştır komutuna cmd yazarak dos penceresini açmış oluruz.