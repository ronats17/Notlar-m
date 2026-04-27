Monolitik ve mikro hizmet mimarileri, yazılım sistemleri oluşturmaya yönelik iki farklı yaklaşımdır ve her birinin kendine özgü güçlü ve zayıf yönleri vardır.

Monolitik mimari, tüm uygulamayı tek, birleşik bir kod tabanı olarak yapılandırır; burada tüm bileşenler (kullanıcı arayüzü, iş mantığı ve veri erişimi) sıkıca birbirine bağlıdır ve birlikte dağıtılır. Bu yaklaşım, başlangıçta geliştirilmesi daha basittir, test edilmesi daha kolaydır ve küçük uygulamalar için maliyet etkinliği yüksektir. Ancak, uygulama büyüdükçe, bireysel özellikleri ölçeklendirmek, yeni teknolojileri benimsemek veya güncellemeleri hızlı bir şekilde yayınlamak zorlaşır.

Öte yandan, mikro hizmet mimarisi, bir uygulamayı her biri belirli bir iş yeteneğinden sorumlu küçük, bağımsız hizmetlere böler. Bu hizmetler API'ler aracılığıyla iletişim kurar ve bağımsız olarak geliştirilebilir, dağıtılabilir ve ölçeklendirilebilir. Bu, daha hızlı yayınlar, daha iyi ölçeklenebilirlik ve gelişmiş hata izolasyonu sağlar, ancak daha yüksek karmaşıklık getirir, güçlü DevOps uygulamaları gerektirir ve operasyonel yükü artırır.

Örnek: Bir e-ticaret platformunda:

Monolitik: Arama, kullanıcı hesapları, sepet, envanter ve ödeme işlemleri tek bir uygulamanın parçasıdır. Ödeme işlemini güncellemek, tüm sistemin yeniden dağıtılmasını gerektirir.

Mikroservisler: Her özellik ayrı bir servistir. Ödeme işlemi, diğer servisleri etkilemeden güncellenebilir veya ölçeklendirilebilir.

Temel Farklar:

Dağıtım: Monolitik yapı tüm uygulamayı yeniden dağıtır; mikroservisler servisleri bağımsız olarak dağıtır.

Ölçeklenebilirlik: Monolitik yapı bir bütün olarak ölçeklenir; mikroservisler belirli servisleri ölçeklendirir.

Teknoloji Esnekliği: Monolitik yapı sınırlıdır; mikroservisler servis başına farklı teknoloji yığınlarına izin verir.

Hata İzolasyonu: Monolitik arızalar tüm uygulamayı çökertebilir; mikroservisler arızaları izole eder.

Ne Zaman Seçilmeli:

Monolitik: Yeni başlayan şirketler, küçük uygulamalar veya basitlik ve pazara hızlı giriş öncelikli olduğunda en iyisidir.

Mikroservisler: Ölçeklenebilirlik, dayanıklılık ve sık yayınlara ihtiyaç duyan büyük, karmaşık veya hızla gelişen sistemler için idealdir.

İpucu: Birçok şirket hız için monolitik yapıyla başlar.

Doğru mimariyi seçmek API veya uygulamanızı başarıya dönüştürebilir ya da bozabilir. MVC ve MVVM gibi klasikler zamanın testine dayanmış olsa da, MVI, Redux, Clean Architecture ve Composable Architecture gibi yeni kalıplar tepkisel ve büyük ölçekli uygulamalar çağında popülerlik kazanıyor.

MVC (Model–Görünüm–Kontrolör)
(mimarilerin başlangıç şablonu)


Kavram:

Model → İş mantığı ve veri.
Sunum/UI veya API çıktısını → görüntüleyin.
Kontrolör → Girişi mantığa bağlar.
Bir benzetme: Menü (görünüm), mutfak (model), garson (kontrolör) → bir restoran.

Kullanım Durumu:

Spring Boot, Django REST, Rails API'leri.
Erken Instagram sadelik için MVC kullanıyordu.
En iyisi: Küçük ve orta ölçekli uygulamalar.

MVVM (Model–ViewModel)

(tepkisel ve ölçeklenebilir)

Kavram:

ViewModel, Model verilerini View-ready formuna dönüştürür.
Tepkisel arayüzler ve test edilebilir API'leri etkinleştirir.
Bir benzetme: Bir çevirmen, ham bilgiyi dinleyici duymadan önce yeniden formatlar.

Kullanım Durumu:

Netflix, API yanıt şekillendirmesinde MVVM kullanıyor.
Microsoft Office 365, temiz ayırım için MVVM'yi benimsedi.
En iyisi: API'lerle sıkı senkronize olan karmaşık arayüzler.

MVVMC (Model–ViewModel–Koordinatörü)
(akışlar veri kadar önemlidir)


Kavram: Navigasyon ve akış için Koordinatör ekliyor.

Bir benzetme: Bir havaalanı → personel sizi check-in'den biniş kapısına kadar yönlendirir.

Kullanım Durumu:

Spotify, mobil API iş akışları için koordinatörler kullanır.
FinTech uygulamaları (KYC gibi bankacılık akışları → hesap → ödeme).
En iyisi: Çok adımlı kullanıcı yolculuğuna sahip uygulamalar.

VIPER (View–Interactor–Presenter–Entity–Router)

(kurumsal düzeyde ayrım)

Kavram: Uygulamayı 5 yüksek şekilde ayrılmış katmana bölüyor.

Bir benzetme: Bir film ekibi → senaryo, yönetmen, görüntü yönetmeni, ekran, dağıtıcı.

Kullanım Durumu:

Uber (iOS) VIPER ile ride API'leri oluşturdu.
Airbnb, modüler rezervasyon API'leri sağlar.
En iyisi: Sıkı kurallara ve uyum gereksinimlerine sahip büyük uygulamalar.

Modern ve Gelişmekte Olan Mimarlıklar
Bu kalıplar, günümüz uygulamalarında durum yönetimi, modülerlik ve ölçeklenebilirlik zorluklarını çözen yeni girişimler veya yeniden canlandırılmış yaklaşımlardır.

MVI (Model–Görünüm–Niyet)

Kavram: Tek yönlü akış:

View, Niyetler (kullanıcı/API eylemleri) gönderir.
Model işlemleri durumu.
Görüntü durumu gösteriyor.
Bir benzetme: Canlı kriket maçı→ seyirci bağırıyor niyet ("cheer"), yorumcu güncellemeleri (model), skor tablosu gösteriliyor (görüntü).

Kullanım Durumu:

Android Jetpack Compose uygulamaları.
Öngörülebilir durum akışları gerektiren uygulamalarda popülerdir.
En iyisi: Tepkisel kullanıcı arayüzleri, karmaşık durum yönetimi.

State Management (Durum Yönetimi) Nedir?
State, basitçe uygulamanın mevcut durumunu temsil eder. Uygulama geliştirmenin temelinde, bir uygulamanın durumunu yönetmek (state management), kullanıcı etkileşimlerini takip etmek ve uygulama davranışını kontrol etmek için kritik bir rol oynar.

State, bir uygulamadaki verilerin anlık durumunu temsil eder. Kullanıcı girişleri, API çağrıları, veya içsel olaylar gibi değişikliklere tepki olarak güncellenir. Bu nedenle, verilerin güncel, tutarlı ve doğru bir şekilde işlenmesi ve depolanması için uygulama durumunun düzenli bir şekilde yönetilmesi önemlidir.

State’in iki temel türü vardır: local state (yerel durum) ve global state (genel durum). Local state, genellikle bir bileşenin (component) içinde tutulup ve sadece o bileşenle ilgili durumu ifade ederken, global state birden çok bileşen arasında paylaşılabilir.


Press enter or click to view image in full size
State (durum), belirli bir zamandaki uygulama durumunu tanımlar.
 View (görünüm), mevcut durumdaki UI’ı temsil eder. UI bu duruma göre render edilir.
 Actions (eylemler), kullanıcı girişine dayalı olarak uygulama durumunu güncelleyen olayları temsil eder. Durum meydana gelen eyleme bağlı olarak güncellenir. 


Redux Nedir?
Redux, JavaScript uygulamalarındaki durum yönetimi ve güncellemeleri için tercih edilen bir desen ve kütüphanedir.

Özellikle büyük ve karmaşık uygulamalarda, durum merkezi bir depoda (store) tutulur bu da uygulamanın yönetimini kolaylaştırır.

Press enter or click to view image in full size

Aynı durumu paylaşan birden çok bileşen olduğunda yaşanılan kod karmaşıklığını önlemek için, bileşenlerden paylaşılan durumu çıkarmak ve onu bileşen ağacının dışında merkezi bir konuma koymak fikri üzerine gelişmiştir. Böylece, herhangi bir bileşen, ağacın neresinde olursa olsun, duruma erişebilir veya eylemleri tetikleyebilir.

Action

Eylemler, uygulamanın durumunu güncellemek için kullanılan bir tür sözleşmedir ve uygulamanın olaylarını açıklamak için önemli bir rol oynarlar.

Action, type ve payload alanlarına sahip basit bir JavaScript nesnesidir. Type alanı, bu eyleme açıklamalı bir ad veren bir dizedir, genellikle “domain/eventName” şeklinde yazarız, burada ilk kısım, bu eylemin ait olduğu özellik veya kategori, ikinci kısım ise meydana gelen belirli olayı temsil eder. Meydana gelen olayla ilgili ek bilgiler “payload” adlı alanda saklanır.

Reducer

Reducer, mevcut durumu ve bir eylem nesnesini alan, gerektiğinde durumu nasıl güncelleyeceğine karar veren ve yeni durumu döndüren bir fonksiyondur: (state, action) => newState.

Bir reducer’ı, alınan eylem (action) türüne dayanarak olayları işleyen bir olay dinleyici olarak düşünebiliriz.

Reducerlar mevcut durumu direkt değiştirmez, mevcut durumu kopyalar ve kopyayı yeni değerlere günceller ve onu döndürür.

Katmanlı mimari, yazılım sistemlerini işlevlerine göre farklı katmanlara ayırarak geliştirme yaklaşımıdır

Controller: Kullanıcıdan gelen istekleri alır ve iş akışlarını yönetir.
Service: İş kurallarını ve iş akışlarını yönetir, veri tabanı işlemlerini gerçekleştirmek yerine, arada soyutlama sağlar.
Repository: Veri erişimi ile ilgili işlemleri kapsar, CRUD işlemleri gibi veritabanı sorgularını yürütür ve ORM işlemlerini içerir.
Bu yapı, kodun okunabilirliğini artırır, test edilebilirliğini artırır ve ekip çalışmasını kolaylaştırır. Katmanlı mimari, özellikle büyük projelerde kodun sürdürülebilirliğini ve test edilebilirliğini sağlamak için kritik öneme sahiptir.
