# BACKEND NOTLARI
<p align="center">
  <img src="https://img.icons8.com/external-flaticons-lineal-color-flat-icons/64/000000/external-coding-web-development-flaticons-lineal-color-flat-icons.png" alt="Coding Icon" />
</p>

<hr style="border: 50px solid #4CAF50; margin: 20px 0;">

# 1️⃣ Model (Entity) → "Veri Katmanı"
📘 Ne işe yarar?

Bu klasör, veri yapısını tanımlar.
Yani bir “not”, “kullanıcı” veya “ürün” nasıl görünüyorsa, o model burada tanımlanır.

📦 Örnek:

model/Note.java

![Java Code](https://raw.githubusercontent.com/RENCBERAKMAN/dev-knowledge/main/images/javacode.jpg)

## Açıklama:

Bu sınıf bir notun nasıl bir veri olduğunu anlatır.

İçinde veri tutar ama “iş mantığı” yoktur.

Bu dosyayı bir “veri kutusu” gibi düşün.

<hr style="border: 50px solid #4CAF50; margin: 20px 0;">

## 2️⃣ Service → "Mantık Katmanı"
📘 Ne işe yarar?

Service, “iş mantığını” içerir.
Yani sistemin ne yapması gerektiğine karar verir.

Controller sadece kullanıcıdan gelen isteği alır ve "Servis’e iletir".

Servis karar verir:

Ne yapılacak?

Hangi veriler kaydedilecek?

Hatalı giriş varsa ne olacak?

Başarılıysa hangi mesaj dönecek?

📦 Örnek:

service/NoteService.java

![Java Code 1](https://raw.githubusercontent.com/RENCBERAKMAN/dev-knowledge/main/images/javacode1.jpg)

Açıklama:

Burada not ekleme ve listeleme işlemini yapıyoruz.

Ama dış dünyayla (HTTP istekleriyle) bağlantısı yok.

Service sadece “mantığı” bilir.

<hr style="border: 50px solid #4CAF50; margin: 20px 0;">

## 3️⃣ Controller → "Yönlendirme Katmanı"
📘 Ne işe yarar?

Controller, dış dünyadan (örneğin Postman, frontend veya tarayıcı) gelen istekleri karşılar.

Yani kullanıcı /notes adresine istek atarsa bu sınıf devreye girer.
İsteği Service’e gönderir, cevabı alır, kullanıcıya döndürür.

📦 Örnek:

controller/NoteController.java

![Java Code 2](https://raw.githubusercontent.com/RENCBERAKMAN/dev-knowledge/main/images/javacode2.jpg)


Açıklama:

Controller, API kapısıdır.

Tarayıcı veya frontend’den istek gelir → Controller alır → Servis’e gönderir.

Service işi yapar → sonucu Controller’a döner → Controller kullanıcıya gönderir.
<hr style="border: 50px solid #4CAF50; margin: 20px 0;">

## 4️⃣ Repository → "Veri Tabanı Katmanı"
📘 Ne işe yarar?

Bizim şu anki projede veritabanı yok ama ileride olacak.
Repository, veritabanına erişimi yöneten katmandır.

Yani:

Veritabanına veri kaydetmek,

Veri silmek,

Veri bulmak,

Filtrelemek gibi işleri yapar.

Spring Boot’ta genellikle şöyle olur:

![Java Code 3](https://raw.githubusercontent.com/RENCBERAKMAN/dev-knowledge/main/images/javacode3.jpg)

Açıklama:

Şu anda bunu kullanmadık ama ileride veritabanı eklediğinde bu yapı aktif hale gelir.

“Service”, Repository ile konuşur.

“Controller”, Repository ile asla direkt konuşmaz!
<hr style="border: 50px solid #4CAF50; margin: 20px 0;">

# 🔹 Controller = “kapı”
# 🔹 Service = “beyin”
# 🔹 Repository = “veriyle konuşan kişi”
# 🔹 Model = “verinin şekli”

<hr style="border: 50px solid #4CAF50; margin: 20px 0;">


  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:0f2027,50:203a43,100:2c5364&height=200&section=footer&text=Thanks%20for%20visiting!%20🚀&fontSize=30&fontColor=ffffff" />
</p>