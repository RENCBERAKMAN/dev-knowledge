<p align="center">
  <img src="https://img.icons8.com/external-flaticons-lineal-color-flat-icons/64/000000/external-coding-web-development-flaticons-lineal-color-flat-icons.png" alt="Coding Icon" />
</p>

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

<hr style="border: 50px solid #4CAF50; margin: 20px 0;">

## 🔍⭐JOIN işlemi nedir? INNER JOIN ile LEFT JOIN farkı nedir?
JOIN, SQL’de birden fazla tablodaki verileri ortak bir sütun üzerinden birleştirmeye yarar. Bu sütun genelde id veya foreign key olur. Amaç, ilişkili verileri tek bir sonuç kümesinde göstermek.

📌 Örneğin, Müşteriler tablosu ve Siparişler tablosu olsun. Bir müşterinin sipariş bilgilerini almak için bu iki tabloyu JOIN ile birleştiririz.

INNER JOIN 🔍

Sadece iki tabloda da eşleşen kayıtları getirir.

Eşleşme yoksa o satır sonuçta yer almaz.

Mantık: Kesişim kümesi

Örnek: Sadece sipariş vermiş müşterilerin listesi.

LEFT JOIN ↔️

Sol tablodaki tüm kayıtları getirir. Sağ tabloda eşleşme yoksa o sütunlar NULL olur.

Mantık: Sol tablonun tamamı + sağ tablo varsa ek veriler

Örnek: Tüm müşterilerin listesi, siparişi olmayanlarda sipariş bilgisi boş.

✅ Fark:

INNER JOIN → Yalnızca eşleşenler ✅

LEFT JOIN → Solun tamamı, sağ varsa ekle, yoksa boş 🗒️

💡 Püf Nokta: Gereksiz LEFT JOIN performansı düşürür. Eşleşmeyen kayıtları bulmak için LEFT JOIN ... WHERE sağ_tablo.sütun IS NULL tekniği yaygındır. Büyük verilerde index kullanmak sorguyu hızlandırır.

<hr style="border: 50px solid #4CAF50; margin: 20px 0;">

## 🔍⭐Veritabanında Primary Key nedir, Foreign Key nedir?
Primary Key, bir tabloda her satırı benzersiz şekilde tanımlayan sütun (veya sütun grubu) demektir. Aynı değere sahip iki satır olamaz ve NULL değeri içeremez.

📌 Örnek: Müşteriler tablosunda customer_id primary key olabilir, çünkü her müşteri benzersiz bir ID’ye sahiptir.

Foreign Key, bir tabloda başka bir tablodaki primary key’e referans veren sütun (veya sütun grubu) demektir. Bu, tablolar arasında ilişki kurar ve referans bütünlüğünü sağlar.

📌 Örnek: Siparişler tablosunda customer_id foreign key olarak Müşteriler tablosundaki customer_id’yi gösterir. Böylece her sipariş doğru müşteriye bağlanır.

✅ Fark:

Primary Key → Kendi tablosunda satırları benzersiz şekilde tanımlar ✅

Foreign Key → Başka tablodaki primary key ile ilişki kurar 🗒️

💡 Püf Nokta:

Her tablonun bir primary key’i olmalı.

Foreign key’ler, verinin tutarlılığını sağlar ve “yetim” kayıt oluşmasını engeller.

JOIN işlemlerinde foreign key’lerde index kullanmak sorguları hızlandırır.

<hr style="border: 50px solid #4CAF50; margin: 20px 0;">

## 🔍⭐Veri normalizasyonu nedir?

Veri normalizasyonu, bir veritabanındaki bilgileri düzenli, tekrar etmeyen ve tutarlı şekilde saklama yöntemidir. Mantık çok basittir: aynı bilgiyi birden fazla yerde tutmak yerine, veriyi tek bir yerde saklayıp diğer tablolarla ilişkilendirmek. Böylece hem veri tutarlılığı sağlanır hem de gereksiz depolama önlenir.

📌 Örnek: Diyelim ki bir Siparişler tablosunda müşteri adı, adresi ve telefon numarası her siparişte tekrar ediyorsa, bu normalizasyon yapılmamış bir tablodur. Normalizasyon uygulayarak müşteri bilgilerini ayrı bir Müşteriler tablosuna taşıyoruz. Artık her müşteri bilgisi sadece bir kez saklanır, siparişler tablosu ise sadece müşteri ID’si üzerinden bu tabloya bağlanır.

✅ Böylece:

Verinin tutarlılığı artar: güncelleme gerektiğinde tek noktadan yapılır ✅

Depolama alanı tasarrufu sağlanır ✅

Sorgular daha hızlı ve yönetim daha kolay olur ✅

💡 Mantığın özü:

“Her veri, sadece bir kez saklanmalı; tekrar eden veriler ayrı tablolarla ilişkilendirilmelidir.”

📌 Ek ipucu: Normalizasyon genellikle 1NF, 2NF, 3NF gibi adımlarla yapılır. Ama bazı durumlarda performans için kontrollü denormalizasyon da tercih edilebilir.

<hr style="border: 50px solid #4CAF50; margin: 20px 0;">

## 🔍⭐CRUD işlemleri nelerdir? (Create, Read, Update, Delete)

CRUD, veritabanı ya da bir uygulama üzerinde yapılabilen en temel dört işlemi ifade eder: Create, Read, Update, Delete. Bu işlemler, neredeyse tüm yazılımların ve veri yönetim sistemlerinin temelini oluşturur.

Create (Oluştur) ✨
Yeni bir veri eklemek için kullanılır.
📌 Örnek: Bir kullanıcı kayıt formu doldurup gönderildiğinde, bu işlem veritabanına yeni bir kullanıcı ekler.

Read (Oku) 📖
Var olan veriyi okumak veya görüntülemek için kullanılır.
📌 Örnek: Kullanıcıların listesini görmek için yapılan sorgu, Read işlemidir.

Update (Güncelle) 🔄
Mevcut veriyi değiştirmek için kullanılır.
📌 Örnek: Bir kullanıcının e-posta adresini değiştirmek Update işlemidir.

Delete (Sil) 🗑️
Var olan veriyi sistemden silmek için kullanılır.
📌 Örnek: Kullanıcı hesabının kalıcı olarak kaldırılması Delete işlemidir.

✅ Kısaca:

Create → Yeni veri ekle

Read → Veri oku/görüntüle

Update → Var olan veriyi değiştir

Delete → Veriyi sil

💡 Püf Nokta: CRUD işlemleri genellikle HTTP metodları ile de eşleştirilir:

Create → POST

Read → GET

Update → PUT/PATCH

Delete → DELETE

Bu sayede hem veritabanı hem de REST API mantığı aynı temel prensipler üzerine kurulur.

<hr style="border: 50px solid #4CAF50; margin: 20px 0;">

## 🔍⭐ Veritabanı tasarımında dikkat edilmesi gereken temel noktalar

1️⃣ Doğru Veri Yapısı Seçimi 🏗️

Tablolar, alanlar (sütunlar) ve veri tipleri doğru tanımlanmalı.

Fazladan sütun veya gereksiz tekrar eden veri olmamalı.

2️⃣ Normalizasyon 📚

Veriler tekrar etmeyecek şekilde düzenlenmeli.

Her bilgi yalnızca bir yerde tutulmalı, ilişkiler foreign key ile sağlanmalı.

3️⃣ İlişkilerin Doğru Kurulması 🔗

One-to-One, One-to-Many, Many-to-Many ilişkiler net belirlenmeli.

Doğru yerde Primary Key ve Foreign Key kullanılmalı.

4️⃣ Veri Tutarlılığı ve Bütünlüğü ✅

Constraint’ler (NOT NULL, UNIQUE, CHECK) ile yanlış veri girişi engellenmeli.

Foreign key ile tablolar arası bütünlük korunmalı.

5️⃣ Performans ve İndeksleme ⚡

Sorgularda sık kullanılan sütunlara index eklenmeli.

Ama gereksiz indexlerden kaçınılmalı (fazla index → yavaş yazma işlemi).

6️⃣ Güvenlik 🔒

Hassas veriler (şifre, kart bilgisi) şifrelenmeli.

Yetkilendirme ve erişim kontrolü uygulanmalı.

7️⃣ Ölçeklenebilirlik ve Esneklik 📈

İleride verinin büyüyeceği düşünülmeli.

Gerektiğinde yeni tablolar veya alanlar kolayca eklenebilmeli.

8️⃣ Yedekleme ve Kurtarma Planı 🗄️

Veri kaybına karşı düzenli yedekleme stratejisi olmalı.

💡 Özet Mantık:
İyi bir veritabanı tasarımı = tekrarsız veri + doğru ilişkiler + tutarlılık + performans + güvenlik.

<hr style="border: 50px solid #4CAF50; margin: 20px 0;">

## 🔍⭐🔐 SQL Injection Nedir?

SQL Injection, bir web uygulamasının en tehlikeli ve en sık karşılaşılan güvenlik açıklarından biridir.

Kısaca tanımlamak gerekirse: SQL injection, kullanıcıdan alınan verilerin (örneğin giriş formu, arama kutusu, URL parametresi) doğrudan SQL sorgusuna eklenmesi ve gerekli kontroller yapılmadan veritabanına gönderilmesi sonucu saldırganın kendi SQL kodlarını çalıştırabilmesidir.

💡 Bunu basit düşün: Uygulaman veritabanına “sadece belirli bir veriyi sorgula” diye emir veriyor, ama saldırgan araya kendi cümlesini ekleyerek “hem istediğin sorguyu yap, hem de şunu da çalıştır” diyebiliyor.

⚠️ Neden Tehlikelidir?

🔓 Veri sızdırılabilir: Saldırgan tüm tablo verilerini (kullanıcı adı, şifre, e-posta) görebilir.

✏️ Veri değiştirilebilir: Tabloya sahte kayıt eklenebilir, mevcut veriler güncellenebilir veya tamamen silinebilir.

🚪 Yetkisiz erişim sağlanabilir: Normalde erişim hakkı olmayan bilgileri görebilir veya admin yetkisi elde edebilir.

💥 Sistem tamamen çökebilir: Kritik tablolar silinirse uygulama kullanılmaz hale gelir.

🔍 En Hassas Noktalar

🚫 Kullanıcı girdisi asla güvenilir değildir.
→ Basit bir OR '1'='1' ifadesi bile tüm kullanıcıların listelenmesine sebep olabilir.

❌ Doğrudan string birleştirme en büyük hatadır.
Örneğin:

"SELECT * FROM users WHERE username = '" + input + "';"


Eğer input doğrudan sorguya eklenirse → tamamen savunmasızsın.

🌐 Sadece giriş formları değil: URL parametreleri, cookie değerleri, hatta HTTP header’ları bile risklidir.

🕵️ Hatalı hata mesajları ipucu verir.
→ Veritabanı hatalarını kullanıcıya göstermek, saldırganın yapıyı öğrenmesini kolaylaştırır.

🛡️ Nasıl Önlenir?

✅ Hazır parametreli sorgular (Prepared Statements) kullan:
Değerler SQL’den ayrı tutulur → saldırgan sorgu yapısını değiştiremez.

🏗️ ORM veya frameworklerin güvenli sorgu metodlarını tercih et:
Örn: Hibernate, Django ORM, Entity Framework.

🔍 Input doğrulama yap:
Beklenen format dışında veri kabul etme. Örn: ID → sadece sayı.

🔑 Minimum yetki prensibi uygula:
Veritabanı kullanıcısına gereksiz yetkiler (DROP, ALTER, vb.) verme.

🚫 Hata mesajlarını gizle:
Kullanıcıya özel SQL hataları gösterme → genel hata mesajı döndür.

🧪 Güvenlik testleri yap:
Araçlar (örn: SQLMap) veya manuel testlerle uygulamayı kontrol et.

🧩 Özet Mantık

👉 SQL Injection’un özü şu:
“Kullanıcının girdiği veri asla sorgunun bir parçası olmamalı, sadece sorgunun parametresi olmalı.”

Bunu sağladığında en kritik güvenlik açığını kapatmış olursun. ✅
<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:0f2027,50:203a43,100:2c5364&height=200&section=footer&text=Thanks%20for%20visiting!%20🚀&fontSize=30&fontColor=ffffff" />
</p>

