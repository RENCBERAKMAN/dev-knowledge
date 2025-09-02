<p align="center">
  <img src="https://img.icons8.com/external-flaticons-lineal-color-flat-icons/64/000000/external-coding-web-development-flaticons-lineal-color-flat-icons.png" alt="Coding Icon" />
</p>
<hr style="border: 50px solid #4CAF50; margin: 20px 0;">

## 🔍⭐JWT (JSON Web Token) Nedir? Ne İşe Yarar?

JWT (JSON Web Token), istemci (client) ile sunucu (server) arasında güvenli ve doğrulanabilir bilgi alışverişi yapmak için kullanılan JSON formatında dijital bir kimlik kartıdır.
Genellikle kullanıcı kimlik doğrulama (authentication) ve yetkilendirme (authorization) için kullanılır.

Kullanıcı giriş yaptığında sunucu, kullanıcı için bir JWT üretir ve istemciye verir. Kullanıcı, sonraki her isteğinde bu token’ı sunucuya gönderir. Sunucu, token’ı doğrulayarak kullanıcının kim olduğunu ve hangi yetkilere sahip olduğunu anlar.

📌 Özet: JWT → “Beni tanıyabilmen için sana geçici ve güvenli bir kimlik veriyorum.”

1️⃣ JWT’nin Yapısı

JWT üç temel bölümden oluşur:

header.payload.signature


Header (Başlık)

Token türü ve kullanılan imzalama algoritması (HS256, RS256) burada belirtilir.

Payload (Yük)

Kullanıcı bilgileri ve izinler burada tutulur (id, email, role vb.).
⚠️ Önemli: Payload şifrelenmez, sadece Base64 ile encode edilir. Bu yüzden gizli bilgiler buraya yazılmaz.

Signature (İmza)

Header ve Payload, gizli bir anahtar veya private key ile imzalanır.

Token değişirse imza geçersiz olur → sunucu fark eder.

2️⃣ JWT’nin Kullanım Alanları
✅ Authentication (Kimlik Doğrulama)

Kullanıcı giriş yaptığında sunucu JWT üretir.

Kullanıcı her istekte token’ı gönderir → “Ben buyum” der.

✅ Authorization (Yetkilendirme)

Token içinde kullanıcı rolü veya izinler saklanabilir.

Sunucu, bu bilgilerle kullanıcının hangi işlemleri yapabileceğini belirler.

✅ Stateless (Durumsuz) Oturum Yönetimi

Normal oturumlarda bilgiler sunucuda tutulur.

JWT ile kullanıcı bilgisi token’da saklanır → sunucuya yük binmez.

Bu özellik microservices ve dağıtık sistemler için kritik bir avantajdır.

3️⃣ Junior Seviyesi İçin Kritik Noktalar

JWT payload’ı okunabilir → gizli bilgiler asla yazılmaz.

Token genellikle Authorization: Bearer <token> header’ında gönderilir.

JWT’nin mutlaka süresi (exp) olmalıdır. Sonsuz ömürlü token güvenlik açığıdır.

Kullanıcı giriş yaptıktan sonra token ile tüm kimlik doğrulama işlemleri yapılır.

4️⃣ İleriye Taşıyan Püf Noktalar

Expire + Refresh Token

Access Token: kısa süreli (örn. 15 dk).

Refresh Token: uzun süreli (örn. 7 gün).

Token çalınsa bile kullanım süresi sınırlıdır.

Algoritma Seçimi

HS256 → simetrik, secret sızarsa güvenlik riski vardır.

RS256 → asimetrik, private key sunucuda, public key doğrulamada kullanılır → daha güvenli.

Blacklist / Token İptali

JWT stateless olduğundan sunucu token’ı otomatik iptal edemez.

Bu nedenle blacklist veya kısa ömürlü token + refresh token stratejisi uygulanır.

Performans ve Payload

Token içine gereksiz veri koyma → network performansını düşürür.

Minimum bilgi ile kimlik doğrulama sağla.

Güvenlik Önerileri

Token’ı HttpOnly cookie ile saklamak XSS saldırılarına karşı güvenli bir yöntemdir.

Kritik işlemlerde, token var diye her şeye izin verme → ek doğrulama yap.

5️⃣ Özet Mantık

JWT = JSON formatında dijital kimlik kartı.

Kullanım alanları: Authentication, Authorization, Stateless session management.

Junior için kritik:

Payload gizli değil → hassas bilgi koyma.

Expire time kullan.

İleri seviye:

Refresh token + access token kombinasyonu.

Algoritma seçimi (HS256 vs RS256).

Blacklist ve token iptali.

Vizyon: JWT her zaman çözüm değildir; doğru stratejiyle, doğru yerde kullanıldığında hem güvenlik hem performans avantajı sağlar.

<hr style="border: 50px solid #4CAF50; margin: 20px 0;">

  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:0f2027,50:203a43,100:2c5364&height=200&section=footer&text=Thanks%20for%20visiting!%20🚀&fontSize=30&fontColor=ffffff" />
</p>
