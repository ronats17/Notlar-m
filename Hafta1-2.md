<h1>Welcome to DriveNow 🚗</h1>
Frontend ve backend yazıyoruz ama hepsi en sonunda bir işletim sistemi üzerinde çalışıyor. Yani kodunun evi işletim sistemi.
En yaygın örnek:
Windows
Linux
macOS

## 1️⃣ Kernel Nedir?##
İşletim sistemlerinin temel bileşenlerinden biri olan çekirdek (kernel), donanım ile yazılım arasında köprü görevi görerek sistem kaynaklarını yönetir. Çekirdek, modern bilgisayarların işleyişinde kritik bir rol oynar; bellek yönetiminden işlem zamanlamasına kadar pek çok temel işlevi üstlenir.
Kernel = işletim sisteminin kalbi.

Bilgisayar:
RAM’i
CPU’yu
Disk’i Donanımı kontrol eden ana merkezdir.

Sen JavaScript yazıyorsun → Tarayıcı çalışıyor → Tarayıcı kernel’dan RAM ve CPU istiyor. Yani kernel arka plandaki patron.

## 2️⃣ Process vs Thread##
Process (Süreç) bir programın çalışan hali.Her uygulama bir process değildir; çalıştırılmadığı sürece sadece bir dosyadır. Ancak çalıştırıldığında, işletim sistemi tarafından bir process’e dönüşür.

Mesela; Chrome açtın → bir process
VS Code açtın → başka bir process
Her process’in kendi belleği vardır.
Başka bir örnek; Masaüstündeki Apache NetBeans sadece bir uygulamadır; ancak açıldığında artık çalışan bir process olur.

Thread (İş Parçacığı)

Process’in içindeki küçük görev çalışanları.Bir process içinde birden fazla thread olabilir. Örneğin, Apache NetBeans çalıştırıldığında bir process olur; bu process içinde aynı anda birden fazla işlemi yürüten her bir görev parçası ise thread olarak adlandırılır.

Chrome bir process.
Ama sekmeler, arka plan işlemleri ayrı thread’lerde çalışabilir. Başka bir örnek;Apache NetBeans açıldığında bir process’tir; bu process içinde çalışan her paralel görev ise bir thread’dir.

Process = büyük ev
Thread = evin içindeki çalışanlar veya odalar olarak nitelendire biliriz.

## 3️⃣ Bellek Yönetimi##
▪ Bir programın çalışabilmesi için;
▪ diskten belleğe getirilmesi ve
▪ bir süreç içerisine yerleştirilmesi gerekir.
▪ Ana bellek ve yazmaçlar, CPU'nun doğrudan erişebildiği alanlardır.
▪ Bellek birimi şu akışları görür:
▪ adres + okuma isteği,
▪ adres + veri + yazma isteği.
▪ Yazmaç erişimi bir CPU döngüsünde yapılır.
▪ Ana bellek erişimi, duraklamaya neden olacak kadar birçok döngü alabilir.
▪ Önbellek (cache), ana bellek ile yazmaçlar arasında bulunur.
▪ Bellek, kısıtlı bir kaynak.
▪ Bu nedenle bellek hiyerarşisi var.
▪ Önbellek (cache)(hızlı)
▪ Ana bellek
▪ Disk (yavaş)
▪ Bellek yöneticisi, bellek soyutlaması yapmak için hiyerarşi kullanır.
▪ Bellek (RAM) önemli ve kısıtlı bulunan bir kaynaktır.
▪ Programlar, genişleyerek kendilerine sunulan belleği doldururlar.
▪ Programcının istediği,
▪ Belleğin korumalı, sonsuz büyük, sonsuz hızlı, ve kalıcı olması..☺
▪ Gerçekte olan,
▪ Akla gelen en iyi çözüm: bellek hiyerarşisi. 
▪ Yazmaç, önbellek, bellek, disk, teyp.
▪ Bellek yöneticisi,
▪ Belleği verimli bir şekilde yönetir.
▪ Serbest bırakılan bellek alanlarını takip eder.
▪ İhtiyaç halinde programlara tahsis eder.

RAM sınırsız değil.

İşletim sistemi:Hangi program ne kadar RAM kullanacak?, Kullanılmayan bellek nasıl temizlenecek? ,Program çökerse bellek nasıl korunacak?
## 4️⃣ CPU Zamanlayıcıları##

CPU aynı anda tek bir işi yapar ama çok hızlıdır. İşletim sistemi der ki: 1 ms sen çalış sonra 1 ms başka program sonra tekrar sen, buna zamanlama (scheduling) denir.Bu sayede çoklu görev (multitasking) mümkün olur.