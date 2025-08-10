<p align="center">
  <img src="https://img.icons8.com/external-flaticons-lineal-color-flat-icons/64/000000/external-coding-web-development-flaticons-lineal-color-flat-icons.png" alt="Coding Icon" />
</p>

## 🔍⭐Backend geliştirici ne iş yapar, frontend’ten farkı nedir?
Backend geliştirici, bir yazılım ya da web uygulamasının görünmeyen kısmını yönetir. Yani kullanıcının tarayıcıda gördüğü arayüzün arkasındaki tüm iş mantığı, veri yönetimi, kullanıcı oturumları, güvenlik, API’ler ve veritabanı işlemleri gibi konular backend tarafında yürütülür.

Frontend, kullanıcının doğrudan etkileşimde olduğu arayüzü inşa ederken; backend geliştirici ise bu arayüzün ihtiyaç duyduğu veriyi sağlamak ve işlemleri gerçekleştirmekle sorumludur.

Örneğin bir kullanıcı bir form gönderdiğinde, bu veriyi alıp veritabanına kaydeden, doğrulayan ve gerektiğinde analiz eden sistem backend tarafında çalışır.

Ben de backend tarafını seçtim çünkü işin mantık ve veri kısmıyla ilgilenmek, karmaşık problemleri çözmek ve sistemin temelini oluşturmak bana çok daha anlamlı ve cazip geliyor.
<hr style="border: 50px solid #4CAF50; margin: 20px 0;">

## 🔍⭐Rest API nedir? Ne işe yarar?
REST API, farklı sistemlerin birbiriyle iletişim kurmasını sağlayan bir yapıdır. Özellikle frontend ve backend’in birbirine veri gönderip alabilmesi için kullanılır.

REST, ‘Representational State Transfer’ anlamına gelir ve HTTP protokolü üzerinden çalışır. API ise bir uygulamanın dış dünya ile iletişim kapısı gibidir.

Örneğin, bir kullanıcı uygulama arayüzünden bir ürün listesi görmek istediğinde, frontend bu isteği backend’e bir REST API aracılığıyla gönderir. Backend bu isteği alır, işleyip veritabanından veriyi çeker ve frontend’e geri gönderir.

✅REST API’ler sayesinde sistemler birbirinden bağımsız çalışabilir, bu da yazılımın ölçeklenmesini ve yönetilmesini kolaylaştırır.

<hr style="border: 50px solid #4CAF50; margin: 20px 0;">

## 🔍⭐HTTP metodları nelerdir? Ne işe yarar?(GET, POST, PUT, DELETE)

“HTTP metodları, bir istemcinin (genellikle frontend’in), sunucuya (backend’e) ne yapmak istediğini belirtmesini sağlar.

En yaygın kullanılan dört temel HTTP metodunu şöyle açıklayabilirim:

GET: Sunucudan veri almak için kullanılır. Örneğin, bir ürün listesini görüntülemek istediğimizde, frontend backend’e GET isteği gönderir.

POST: Sunucuya yeni veri göndermek ve kaydetmek için kullanılır. Mesela bir kayıt formu gönderildiğinde bu işlem POST ile yapılır.

PUT: Var olan veriyi tamamen güncellemek için kullanılır. Örneğin, bir kullanıcının profil bilgilerini güncellerken PUT kullanılır.

DELETE: Belirli bir veriyi sunucudan silmek için kullanılır. Örneğin, bir kullanıcı hesabını silmek için.

✅Bu metodlar sayesinde frontend ve backend arasında düzenli ve anlaşılır bir iletişim olur. REST API’lerde de bu metodları kullanarak farklı işlemleri standart bir şekilde yapabiliyoruz.

<hr style="border: 50px solid #4CAF50; margin: 20px 0;">

## 🔍⭐POST ve PUT arasındaki fark nedir?
POST ve PUT, her ikisi de sunucuya veri göndermek için kullanılır ama amaçları ve kullanıldıkları senaryolar farklıdır.

POST, genellikle yeni bir veri oluşturmak için kullanılır. Örneğin bir kullanıcı kayıt formu gönderirken POST kullanırız. Sunucu yeni bir kullanıcı oluşturur.

PUT ise var olan bir veriyi güncellemek için kullanılır. Örneğin bir kullanıcının e-posta adresini değiştirmek istiyorsak PUT kullanırız.

Bir fark da şudur:

POST her çağrıldığında yeni bir kayıt oluşturabilir (id’si farklı olan yeni nesne gibi),

Ama PUT çağrıldığında belirli bir ID’ye sahip olan veriyi aynı tutarak içeriğini günceller.

✅Kısaca:
🚀→ POST = Oluştur.
🚀→ PUT = Güncelle.

<hr style="border: 50px solid #4CAF50; margin: 20px 0;">

## 🔍⭐Stateless mimari nedir?
Stateless, yani durumsuz mimari, her isteğin (request) birbirinden bağımsız olduğu anlamına gelir. Yani bir istemciden (örneğin bir tarayıcıdan) sunucuya yapılan her istek, sıfırdan yapılır gibi değerlendirilir.

Sunucu, daha önce gelen isteği hatırlamaz. Her istek kendi başına, gerekli tüm bilgileri içerir (örneğin: kimlik doğrulama bilgisi, veri vs.). Böylece sunucu, geçmişe bağlı kalmadan çalışır.
Örnek:
Bir REST API düşün. Her GET veya POST isteğinde sunucuya kim olduğunu ve ne istediğini tekrar tekrar bildirirsin. Sunucu önceki istekte sana cevap vermiş olsa bile, bir sonraki istekte bunu hatırlamaz.

✅ Avantajları:
🚀Sunucu ölçeklenebilir olur (çünkü hafızasında kullanıcı bilgisi tutmaz).

🚀Yük dengeleme (load balancing) kolaylaşır.

🚀Hızlı, basit ve bakımı kolay sistemler kurulur.

<hr style="border: 50px solid #4CAF50; margin: 20px 0;">

## 🔍⭐MVC (Model-View-Controller) Mimarisi Nedir ve Neden Kullanılır?
MVC, üç ana bileşene ayrılmış bir yazılım mimarisidir:

Model (Veri ve İş Mantığı)
Uygulamanın tüm verileri, kuralları ve iş mantığını içerir. Veritabanıyla iletişim, veri işleme ve kurallar bu katmanda yer alır.

View (Görünüm)
Kullanıcının etkileşime geçtiği arayüzdür. Görsel tasarımlar, butonlar, formlar gibi kullanıcıya gösterilen her şey bu katmandadır.

Controller (Kontrolcü)
Kullanıcıdan gelen istekleri işler, uygun Model ile iletişim kurar ve sonucu View’a gönderir. Aslında Model ile View arasındaki bir köprüdür.

----✅ NEDEN MVC KULLANILIR?----
1. Kodun Ayrıştırılması (Separation of Concerns)
Her bileşenin kendi sorumluluğu vardır. Böylece kod daha anlaşılır, düzenli ve bakımı kolay hale gelir. Örneğin; görünüm değişirse yalnızca View’ı güncellemek yeterlidir.

2. Test Edilebilirlik Artar
Model ve Controller ayrı olduğundan birimleri test etmek daha kolaydır. Bu, özellikle büyük projelerde otomatik testlerin etkinliği açısından büyük avantaj sağlar.

3. Yeniden Kullanılabilirlik (Reusability)
Aynı veri (Model), farklı görünümlerle (View) birden fazla kez kullanılabilir. Örneğin aynı kullanıcı bilgisi, farklı sayfalarda farklı şekillerde gösterilebilir.

4. Ekipte Paralel Geliştirme Kolaylaşır
Frontend geliştiricileri View üzerinde çalışırken, Backend geliştiricileri Model ve Controller üzerinde çalışabilir. Böylece ekip daha verimli çalışır.

5. Genişlemeye Açık Mimaridir
Uygulama büyüdükçe parçaları büyütmek veya yenilerini eklemek daha kolay hale gelir. Özellikle modüler tasarım isteyen projeler için idealdir.

<hr style="border: 50px solid #4CAF50; margin: 20px 0;">

## 🔍⭐Request ve Response ne demektir?
Request ve Response, web tabanlı sistemlerde istemci (client) ile sunucu (server) arasındaki iletişimi tanımlar. "Request", istemcinin sunucuya gönderdiği istektir. Bu istek, genellikle bir sayfa görüntüleme, veri gönderme veya bilgi alma talebini içerir. Örneğin bir web sitesine giriş yapıldığında, tarayıcı sunucuya bir "GET" isteği göndererek sayfanın içeriğini talep eder.

Sunucu, bu isteği aldıktan sonra işlemi gerçekleştirir ve buna karşılık bir "Response", yani yanıt gönderir. Bu yanıt HTML sayfası, bir JSON verisi, bir hata mesajı ya da işlem sonucunu bildiren başka türde bir içerik olabilir.

Kısaca: Request, istemcinin talebini, Response ise sunucunun bu talebe verdiği cevabı temsil eder. Bu ikili, modern web uygulamalarının temel taşıdır. İletişim genellikle HTTP ya da HTTPS protokolleri üzerinden sağlanır ve her adım belirli kurallarla işler.

Bu yapı sayesinde kullanıcıların tarayıcı üzerinden yaptıkları işlemler sunucu tarafından anlaşılır, işlenir ve karşılık verilir.

<hr style="border: 50px solid #4CAF50; margin: 20px 0;">

## 🔍⭐HTTP Durum Kodları (200, 201, 400, 401, 403, 404, 500)
HTTP durum kodları, istemciden (client) gelen isteğin sunucu (server) tarafından nasıl sonuçlandığını gösteren sayısal ifadelerdir.
Her kod, isteğin başarılı mı, hatalı mı yoksa başka bir işleme mi ihtiyaç duyduğunu belirtir.

200 – OK
İstek başarılı bir şekilde işlendi ve sunucu beklenen yanıtı gönderdi.
Örnek: Bir ürün listesi istendiğinde, sunucu listeyi JSON formatında döner.

201 – Created
İstek başarılı oldu ve sunucu yeni bir kaynak oluşturdu.
Örnek: Kayıt formu gönderildiğinde yeni kullanıcı oluşturulması.

400 – Bad Request
İstek hatalı, eksik veya sunucu tarafından anlaşılamıyor.
Örnek: Zorunlu alanları boş bırakarak form göndermek.

401 – Unauthorized
Kimlik doğrulama yapılmamış ya da geçersiz. Erişim için geçerli bir giriş bilgisi gerekir.
Örnek: Oturum açmadan yetkili bir API’ye istek göndermek.

403 – Forbidden
Kimlik doğrulama yapılmış olsa bile erişim izni yok.
Örnek: Normal bir kullanıcının yönetici paneline girmeye çalışması.

404 – Not Found
İstenen kaynak sunucuda bulunamadı.
Örnek: Var olmayan bir URL’ye gitmek.

500 – Internal Server Error
Sunucu, isteği işlerken beklenmeyen bir hata ile karşılaştı.
Örnek: Kod hatası veya veritabanı bağlantı sorunu.

 ✅Özet:

🚀2xx → Başarılı işlemler

🚀4xx → İstemci kaynaklı hatalar

🚀5xx → Sunucu kaynaklı hatalar

<hr style="border: 50px solid #4CAF50; margin: 20px 0;">

## 🔍⭐API versioning nedir? Neden önemlidir?

API Versioning, bir API’nin zaman içinde değişen sürümlerini yönetme yöntemidir.
API’ler geliştikçe yeni özellikler eklenir, mevcut yapılar değiştirilir veya kaldırılır.
Bu durum, API’yi kullanan uygulamaların bozulmasına sebep olabilir.
API versioning, bu değişiklikleri kontrollü bir şekilde yapmamızı ve eski kullanıcıların etkilenmeden çalışmaya devam etmesini sağlar.

Neden Önemlidir?

🚀Geriye dönük uyumluluğu korur (backward compatibility)

🚀Eski sürümü kullananlar etkilenmeden yeni sürüm yayınlanabilir

🚀Büyük değişiklikler adım adım devreye alınabilir

🚀API kullanıcılarının hangi sürümü kullanacağını seçmesine olanak tanır

🚀Geliştirme sürecini ve bakımını kolaylaştırır

🚀Hataları veya eksikleri yeni sürümlerde düzeltme imkanı sunar

✅Kısaca, API versioning hem geliştiriciler hem de kullanıcılar için API’nin güvenli, uyumlu ve sürdürülebilir olmasını sağlar.

<hr style="border: 50px solid #4CAF50; margin: 20px 0;">

## 🔍⭐Middleware nedir? Ne işe yarar?
⚙️ Middleware Nedir? Ne İşe Yarar?
Middleware, bir uygulama ile istemci (client) istekleri arasına giren ve bu istekleri belirli bir işlemden geçirerek sonraki aşamaya ileten ara katman yazılımlardır.
Genellikle, istemciden gelen request (istek) ile sunucudan dönen response (yanıt) arasında çalışır.

Middleware’in Amaçları:

🚀 İstekleri filtrelemek: Örneğin, kimlik doğrulaması yapılmamış kullanıcıları engellemek.

🛡️ Güvenlik sağlamak: Yetkilendirme, veri doğrulama ve saldırı önleme işlemleri.

📊 Loglama ve izleme: API’ye gelen isteklerin kaydını tutmak.

⚙️ Veri işleme: İstek veya yanıt üzerinde düzenleme yapmak (örn: JSON formatına dönüştürmek).

🌐 CORS yönetimi: Farklı alan adlarından gelen istekleri kontrol etmek.

✅ Kısaca: Middleware, uygulamanın farklı aşamalarında araya girerek isteğin güvenli, doğru ve verimli şekilde işlenmesini sağlayan kritik bir mekanizmadır.

<hr style="border: 50px solid #4CAF50; margin: 20px 0;">

## 🔍⭐Rate Limiting Nedir ve Neden Önemlidir?
Rate limiting, bir API’nin veya sistemin belirli bir zaman diliminde kabul edebileceği istek sayısını sınırlama yöntemidir.
Amacı, sistemin aşırı yüklenmesini önlemek, güvenliği artırmak ve kaynakların adil şekilde kullanılmasını sağlamaktır.

⚙️Neden önemlidir?

🚀 Sistemi aşırı yüklenmeye karşı korur.

🚀 Brute-force ve DDoS saldırılarını önler.

🚀 Kullanıcılar arasında adil kaynak paylaşımı sağlar.

🚀 Maliyet ve performans yönetimini kolaylaştırır.

⚙️Nasıl uygulanır?

Token Bucket / Leaky Bucket: Her istek bir token tüketir, token yoksa istek reddedilir.

Fixed Window: Belirli bir zaman aralığında sınırlı sayıda isteğe izin verir.

Sliding Window: Zaman penceresi kaydırılarak istekler daha adil bir şekilde dağıtılır.

Örnek kullanım senaryoları:

🚀 Giriş denemelerini sınırlamak (örneğin, 5 dakika içinde en fazla 5 deneme).

🚀 Ücretsiz ve premium kullanıcılar için farklı istek limitleri belirlemek.

🚀 Harici API servislerinin limitlerini aşmamak için istekleri kontrol etmek.

✅Özet: Rate limiting, bir backend geliştirici için sistem performansı, güvenliği ve istikrarı açısından kritik bir mekanizmadır.

<hr style="border: 50px solid #4CAF50; margin: 20px 0;">

## 🔍⭐Caching (Önbellekleme) Nedir?

⚡ Caching (Önbellekleme), veriyi daha hızlı erişebilmek için geçici bellekte saklama işlemidir. Amaç, aynı veriyi tekrar tekrar yavaş bir kaynaktan (örneğin veritabanı veya uzak bir API) çekmek yerine, bellekte tutarak milisaniyeler içinde erişmektir. Bu sayede performans artar 🚀, veritabanı yükü azalır 💾 ve kullanıcı deneyimi iyileşir .

Backend dünyasında caching genellikle şu şekilde çalışır: Bir istek geldiğinde önce cache’e bakılır. Eğer veri cache’te varsa doğrudan oradan döndürülür, yoksa veritabanından çekilir, cache’e yazılır ve istemciye iletilir. Bu süreçte verinin cache’te kalma süresi TTL (Time To Live) ile belirlenir, böylece eski veriler otomatik olarak silinir veya yenilenir.

En yaygın kullanılan cache sistemleri arasında Redis 🟥 ve Memcached 🟩 bulunur. Java projelerinde Spring Boot Cache desteği ile kolayca entegre edilebilir.

📌 Dikkat Edilmesi Gerekenler
Veri Güncelliği: Cache’teki veri zamanla eskir. TTL ayarını iyi yapmak gerekir ⏳.

Bellek Yönetimi: Cache bellekten yer kaplar, sınırsız büyümesine izin verme 💾.

Doğru Kullanım: Sık erişilen, nadiren değişen veriler için uygundur; sürekli değişen veriler için verimsiz olabilir ⚠️.

Senkranizasyon: Cache ile asıl veri kaynağının tutarlı kalması sağlanmalı 🔄.

Temizleme Stratejileri: LRU (Least Recently Used) gibi algoritmalarla kullanılmayan verileri silmek iyi bir pratiktir 🧹.

<hr style="border: 50px solid #4CAF50; margin: 20px 0;">

## 🔍⭐SQL ve NoSQL Arasındaki Temel Farklar 💡
SQL ve NoSQL, verileri depolamak için kullanılan iki farklı sistemdir. Her ikisi de veriyi saklar ama bunu farklı şekillerde yapar.

1. Veri Yapısı 🗂️
SQL: Veriler tablo (satır ve sütun) şeklinde düzenlenir. Tablolar arası net ilişkiler vardır. Şeması önceden belirlenir ve değiştirilemez.

NoSQL: Veriler daha esnek şekildedir; belge (JSON), anahtar-değer veya grafik gibi farklı formatlarda olabilir. Şema yoktur veya esnektir.

2. Sorgulama Dili 📝
SQL: Standart ve güçlü bir dil kullanılır (SQL). Karmaşık sorgular ve ilişkiler kolayca yapılabilir.

NoSQL: Her tür NoSQL veritabanının kendi sorgulama yöntemi vardır. JOIN gibi karmaşık ilişkiler genellikle yoktur.

3. Ölçeklenebilirlik 📈
SQL: Performansı artırmak için daha güçlü bir sunucuya geçersiniz (dikey ölçek). Büyük veri için yatay ölçek yapmak zordur.

NoSQL: Sunucu sayısını artırarak veri dağıtılır (yatay ölçek). Büyük ve hızlı büyüyen veriler için uygundur.

4. Veri Tutarlılığı 🔒
SQL: Veriler her zaman tutarlıdır ve kesin doğruluk sağlanır (ACID). Örneğin bankacılık sistemlerinde tercih edilir.

NoSQL: Performans için bazen veri tutarlılığı biraz esnetilir (Eventual consistency). Yani veriler hemen güncellenmeyebilir ama zamanla tutarlı hale gelir.

5. Kullanım Alanları 🛠️
SQL: Yapısal ve karmaşık ilişkilerin olduğu, veri bütünlüğünün kritik olduğu sistemler.

NoSQL: Hızlı büyüyen, esnek veri yapısı gereken uygulamalar; sosyal medya, büyük veri, gerçek zamanlı analiz gibi.
<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:0f2027,50:203a43,100:2c5364&height=200&section=footer&text=Thanks%20for%20visiting!%20🚀&fontSize=30&fontColor=ffffff" />
</p>

