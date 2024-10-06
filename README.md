# FRC SLAPer
## Ön söz 
Lokalizasyon ve Patika Planlama, FRC takımları için baştan beri en ihtiyaç duyulan yapılardan biri. Uzun zamandır birçok takım ve bağımsız kuruluş, bu amaçta sayısız proje ve aplikasyon geliştirmiş olsa da, piyasanın son durumunda çoğu takımın belli başlı uygulamalara bağlı kaldığı gözlemleniyor. Bu durum; hazır program kullanımına teşvik ettiğinden sınırlı bir kod yazma, geliştirme ve öğrenme ortamı oluşturuyor. Bu alanda tekel olan bazı uygulamalar gün geçtikçe kendini ileri taşıdığından, yeni girişimlerle arasındaki fark açılıyor ve rekabet ortamı azalıyor.

Bir diğer sıkıntı ise, Türk FRC takımlarının çoğu dil ve konum bariyerinden dolayı bu amaç uğrundaki uygulamaları ya kullanamıyor, ya kullanmakta zorluk çekiyor ya da yetersiz kaynaktan dolayı SLAP uygulamalarının kullanımındaki rekabette geride kalıyorlar

İşte bu noktada FRC SLAPer devreye giriyor. Takımımız öğrencileri tarafından hazırlanan bu Sürekli Konumlandırma ve Patika Planlama aplikasyonu, hem takımımız öğrencilerinin kendilerini bu sınırlayıcı ortamdan kurtarmalarını sağlıyor, hem de yetersiz kaynak dolayısıyla kullanılamayan uygulamalara alternatif sağlıyor.

Metnin şu andaki konumu itibariyle kendiyle çeliştiği aşikar. Hem öğrenimin yetersiz olduğundan yakınırken bu sınırlayıcı faktörlere bir yenisini daha eklemek, ne uzaktan ne yakından bakılırsa bakılsın mantıksız gözüküyor. İşte bu yüzden bu öğreticiyi yazıyor ve açık kaynak kodlu olarak yayımlıyoruz. Bu sayede programımızı fikir edinme amaçlı kullanabilecek, inceleyebilecek ve kendiniz de takımınızla bu doğrultuda program yazabileceksiniz.

## Telif
Bu öğretici, aplikasyon ve aplikasyonun kaynak kodları; open-source (halk kullanımına açık) olarak paylaşılmıştır. Eğer öğretici, aplikasyon veya aplikasyonun kaynak kodlarından herhangi birinden herhangi bir yerde doğrudan alıntı yapılıyorsa, takımımızın ve öğretici linkinin kaynakça olarak eklenmesi rica olunur. Öğretici, aplikasyon veya aplikasyonun kaynak kodlarından herhangi birinin yüzde 80'inden fazlası ne doğrudan, ne de anlatımı değiştirilerek dolaylı yoldan başka bir yerde kullanılamaz.

# Lokalizasyon
Lokalizasyon, robotun encoder, kamera, mesafe sensörü gibi sensörlerinden elde ettiğimiz verilere göre odometri oluşturulmasıya ortaya çıkar. Odometri verisi, bize robotun hareketi hakkında bilgi verir ve bu bilgiler kullanılarak -genellikle- otonom sürüş kodları yazılır.

Bu öğreticide Tank (WCD) sürüş için odometriyi inceleyeceğiz.

Odometri hesaplamanın temel olarak iki yolu vardır
## Yay Teorisi (Theory Of Arc)
[(https://img.youtube.com/vi/watch?v=LXb3EKWsInQ/0.jpg)](https://www.youtube.com/watch?v=LXb3EKWsInQ)
