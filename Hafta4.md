## Dosya Sistemleri ve Depolama Mantığı##
NTFS (New Technology File System; Yeni Teknoloji Dosya Sistemi), Windows NT'nin standart dosya sistemidir ve Windows 2000, Windows XP, Windows Server 2003,Windows Vista, Windows 7, Windows 8 ve 8.1, Windows 10 ve Windows 11'de de standart olarak kullanılmıştır. Microsoft'un önceki FAT dosya sisteminin yeniden yapılandırılmasıyla oluşmuştur.
- **NTFS'nin bazı özellikleri:**
- **Dosya izinleri:** Dosya düzeyinde izinler, şifreleme, sıkıştırma, günlük kaydı ve SSD TRIM işlemlerini destekler. 12
- **Güvenilirlik:** İşlem tabanlı günlük dosyası ve denetim noktası bilgileri ile sistem hatası durumunda veri kaybı riskini azaltır. 5
- **Uyumluluk:** Windows dışında uyumluluğu sınırlıdır; Mac sistemlerinde sadece okuma desteği vardır. 23
Büyük dosya desteği: 16 EB'a kadar dosya boyutu ve 8 PB'a kadar birim boyutunu destekler. 1
NTFS, 5 farklı sürüme sahiptir: 1.0, 1.1, 1.2, 4.0, 5.0 ve 5.1. 1
## Ext4 Ve Ötesi:##
Modern Linux dağıtımlarının çoğu varsayılan olarak ext4 dosya sistemi ile birlikte geliyor. Geçmişte varsayılan olarak kullanılan dosya sistemleri ise ext3, ext2 ve çok daha geçmişe gidilirse ext idi.

Linux platformu ya da dosya sistemleri konusunda bilgi edinmeye henüz başladıysanız ext4 dosya sisteminin ext3 dosya sistemine göre ne yenilikler getirdiğini merak edebilirsiniz. Ayrıca ext4’ün halen geliştirilip geliştirilmediğini ya da btrfs, XFS, ZFS gibi alternatif dosya sistemlerini de merak ediyor olabilirsiniz.

Dosya sistemleri ile ilgili her şeyi tek bir yazının içinde toplamak mümkün değil. Ancak bu yazıda sizlere olabildiğince Linux dosya sistemlerinin gelişimini, şu an nerede olduğumuzu ve gelecekte neler olabileceği konusunda bilgi vereceğiz.

## APFS NEDİR## 

APFS (Apple File System), Apple'ın 2017 yılında macOS High Sierra ile birlikte tanıttığı modern bir dosya sistemidir. Özellikle SSD'ler için optimize edilmiş olan APFS, veri yönetimini daha verimli hale getirir. APFS, HFS+'ya kıyasla daha hızlı veri erişimi, daha az boş alan kaybı ve daha güçlü veri güvenliği özellikleri sunmaktadır. APFS'nin en dikkat çekici özelliklerinden biri, veri bütünlüğünü sağlamak için kullanılan "copy-on-write" mekanizmasıdır. Bu mekanizma, dosya yazma işlemlerini fiziksel alanda yeni bir konuma yazarak, eski verilerin kaybolmamasını sağlar.

APFS, çoklu dosya sistemleri arasında dinamik bir şekilde geçiş yapmanıza olanak tanır. Ayrıca, dosyaların ve dizinlerin anlık görüntülerini (snapshot) alarak, sistemin belirli bir zamandaki durumunu kaydetmenizi sağlar. Terminal üzerinden APFS'nin özelliklerini incelemek için `diskutil apfs list` komutunu kullanabilirsiniz.

## Blok Nedir?##
"Blockchain" kelimesini duyduğunuzda büyük ihtimalle birbirine bağlı bloklardan oluşan bir görsel hayal edersiniz. İşte tam olarak bu! Blockchain’deki her bir blok, blockchain ağı içerisindeki işlemlerle ilgili verileri içeren bilgi birimidir. Blockchain’deki ilk blok, genesis blok veya blok 0 olarak bilinir.

Bir bloğu, belirli bir süre boyunca kaydedilen tüm işlemleri içeren bir kitabın sayfası gibi düşünün. Blokların kesin yapısı farklı blockchain’lerde değişiklik gösterebilir. Blockchain, birbiriyle kronolojik olarak bağlı çok sayıda bloktan oluşan bütünü temsil eder.

Blockchain üzerinde veri içeriği, kriptografik hash ve konsensüs mekanizmaları ile kilitlenir. Blok içeriğinin hash’i, önceki bloktaki hash ile birleştirilir ve veri değişmezliğini sağlar. Her blokun benzersiz bir tanımlayıcısı bulunur ve bu yapı, sadece veri saklamakla kalmaz, aynı zamanda değişikliklere karşı koruma sağlar. Blockchain’e eklenen veriler hiçbir şekilde değiştirilemez. Bu özellik, DeFi (Merkezi Olmayan Finans) alanındaki işlemleri bugünkü en güvenli ve en şeffaf seçeneklerden biri haline getirir.

- **Blok Yapısı**
Blokun ne olduğunu öğrendik. Şimdi, bu yapıya daha yakından bakalım. Blokların yapısı, verileri güvenli bir şekilde saklamak ve korumak üzere dikkatlice tasarlanmıştır. Bir blok, önemli miktarda bilgi içerir, ancak fazla yer kaplamaz. Blok, işlem listesi, blok sürüm numarası, blok yüksekliği, blok hash’i, önceki blok hash’i, zaman damgası, nonce ve hedef zorluğu gibi elementlerden oluşur.
HDD Çalışma Prensibi##
Sabit disk sürücüleri (HDD - Hard Disk Drive), verileri manyetik olarak saklayan mekanik depolama cihazlarıdır. HDD'lerin çalışma prensibi şu temel bileşenlere dayanır:

- **1. Plakalar (Platter) ve Manyetik Kaplama**
HDD içinde bir veya birden fazla dönen disk (plaka) bulunur.
Bu plakalar manyetik kaplama ile kaplanmıştır ve veriler bu yüzeyde manyetik alan değişiklikleri ile saklanır.
Plakalar, sabit bir hızda (örneğin 5400 RPM, 7200 RPM veya daha yüksek) döner.

- **2. Okuma-Yazma Kafası (Read/Write Head)**
Plakalar üzerinde hareket eden okuma-yazma kafası, manyetik alan değişikliklerini algılayarak veriyi okur ve yazma işlemi yapar.
Kafalar, plakalar üzerinde doğrudan temas etmez, çok küçük bir hava boşluğu sayesinde sürtünme olmadan hareket eder.

- **3. Aktuatör Kolu ve Motor (Actuator Arm & Motor)**
Okuma-yazma kafası, aktuatör kolu ile plakalar üzerinde hareket ettirilir.
Aktuatör motoru, kafa konumunu hassas bir şekilde kontrol eder ve istenilen veri sektörüne erişim sağlar.

- **4. Kontrol Kartı (PCB - Printed Circuit Board)**
HDD’nin elektronik kontrolü bu kart ile sağlanır.
Motor hızını düzenler, okuma/yazma işlemlerini yönetir ve bilgisayarla veri alışverişini sağlar.

- **5. Manyetik Veri Saklama**
HDD, verileri manyetik alan değişiklikleri ile saklar.
0 ve 1'ler, manyetik yönelimlerin değişimiyle plakalar üzerine kodlanır.

-**6. Dosya Sistemi ve Bölümler**
HDD’de verilerin organize edilmesi için dosya sistemleri (NTFS, FAT32, exFAT vb.) kullanılır.
Disk bir veya birden fazla bölüme (partition) ayrılabilir.

HDD’nin Avantajları ve Dezavantajları
- **✅ Avantajlar:**

Büyük kapasiteli depolama imkanı
Uygun fiyatlı olması
Uzun süreli veri saklama özelliği

- **❌ Dezavantajlar:**

Mekanik parçalardan dolayı arızalanma riski yüksek
SSD’ye kıyasla daha yavaş okuma/yazma hızı
Fiziksel darbelere karşı hassasiyet

HDD’ler, server sistemlerinden kişisel bilgisayarlara kadar geniş bir kullanım alanına sahiptir. Ancak SSD teknolojisinin gelişmesiyle birlikte HDD’ler daha çok arşivleme ve büyük veri depolama alanlarında tercih edilmektedir.


## SSD Nedir?##

SSD (Solid State Drive), verileri depolamak için flash bellek kullanan bir depolama cihazıdır. Geleneksel sabit disklerin (HDD) aksine, SSD'lerde hareketli parçalar bulunmaz. Bu da onları daha hızlı, daha dayanıklı ve daha sessiz hale getirir.

- **SSD Nasıl Çalışır?**

SSD'ler, NAND flash bellek hücreleri üzerinde verileri depolar. Bu hücreler, verileri elektriksel yükler aracılığıyla saklar ve okur. SSD'lerin çalışma prensibi şu şekildedir:

Veri Yazma:Veriler, NAND flash bellek hücrelerine yazılır. Bu hücreler, elektriksel yüklerle doldurulur ve bu yükler, verilerin bitlerini temsil eder.
Veri Okuma:Veriler, NAND flash bellek hücrelerinden okunur. Elektriksel yükler, hücrelerdeki bitleri temsil eder ve bu bitler okunarak veri elde edilir.
Veri Silme:Veriler, belirli bir hücre bloğundan silinir. Bu işlem, hücrelerin elektriksel yüklerinin sıfırlanması ile gerçekleştirilir.

- **SSD'nin Avantajları**

Hız:SSD'ler, HDD'lere göre çok daha hızlıdır. Verilere erişim süresi ve veri transfer hızları oldukça yüksektir. Bu da bilgisayarın açılış süresini, uygulamaların yüklenme hızını ve dosya transfer sürelerini kısaltır.
Dayanıklılık:Hareketli parçalara sahip olmadıkları için darbelere ve titreşimlere karşı daha dayanıklıdır. Bu da özellikle dizüstü bilgisayarlar gibi taşınabilir cihazlar için büyük bir avantajdır.
Sessizlik:Mekanik bileşenler içermediğinden sessiz çalışır. HDD'lerdeki disk dönme sesi ve kafa hareketleri gibi sesler SSD'lerde bulunmaz.
Düşük Güç Tüketimi:SSD'ler, HDD'lere göre daha az enerji tüketir. Bu da özellikle laptoplar için daha uzun pil ömrü anlamına gelir.

- **SSD Türleri**

1. SATA SSD:Geleneksel HDD'lerin kullandığı SATA arayüzünü kullanan SSD'lerdir. SATA SSD'ler, yüksek performans sunar ancak NVMe SSD'ler kadar hızlı değildir.

2. NVMe SSD:NVMe (Non-Volatile Memory Express) arayüzünü kullanan SSD'lerdir. PCIe bağlantısı üzerinden çalışır ve çok daha yüksek hızlar sunar. NVMe SSD'ler, en yüksek performansı arayan kullanıcılar için idealdir.

3. M.2 SSD:M.2 form faktöründe olan SSD'lerdir. Hem SATA hem de NVMe arayüzünü destekleyebilir. İnce ve küçük yapısı sayesinde özellikle ultrabook ve mini PC'lerde tercih edilir.

4. U.2 SSD:U.2 arayüzünü kullanan SSD'lerdir. Genellikle veri merkezleri ve sunucular için yüksek performans ve kapasite sunar.

- **SSD Seçim Kriterleri**

1. Kapasite:İhtiyacınıza uygun depolama kapasitesini seçin. 256GB, 512GB, 1TB ve daha yüksek kapasiteler arasında seçim yapabilirsiniz.
2. Hız: NVMe SSD'ler, SATA SSD'lere göre daha yüksek hız sunar. İhtiyacınıza ve bütçenize uygun bir hız seçimi yapın.
3. Dayanıklılık: SSD'nin dayanıklılığı, yazma döngüleri ile ölçülür. Daha yüksek yazma döngüsüne sahip SSD'ler daha uzun ömürlüdür.
4. Fiyat: SSD'nin dayanıklılığı, yazma döngüleri ile ölçülür. Daha yüksek yazma döngüsüne sahip SSD'ler daha uzun ömürlüdür.

SSD'ler, bilgisayar performansını artırmak isteyen kullanıcılar için mükemmel bir seçenektir. Hızlı veri erişimi, dayanıklılık, sessizlik ve düşük güç tüketimi gibi avantajları ile SSD'ler, geleceğin depolama çözümü olarak öne çıkıyor. İhtiyacınıza uygun bir SSD seçerek bilgisayar deneyiminizi bir üst seviyeye taşıyabilirsiniz.