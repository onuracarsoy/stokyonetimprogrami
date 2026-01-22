# Stok Yönetim Programı

Basit ve öğretici amaçlarla hazırlanmış masaüstü stok takip uygulaması.

## Özet
Stok Yönetim Programı, ürünlerin (cep telefonu, aksesuar vb.) stoklarını takip etmek, eklemek, güncellemek, silmek ve faturalarını yönetmek için hazırlanmış bir Windows Forms uygulamasıdır. Küçük işletmeler veya öğrenme amaçlı projeler için uygundur.

## Öne çıkan özellikler
- Ürün ekleme, düzenleme ve silme (isim, miktar, fiyat vb.)
- Ürün listesi görüntüleme ve arama
- Fatura ekleme ve yönetimi
- Basit SQL Server / LocalDB bağlantısı ile veri saklama

## Kullanılan teknolojiler
- C#
- Windows Forms
- ADO.NET
- SQL Server LocalDB
- Visual Studio (çalıştırmak için)

## Kurulum ve çalıştırma
1. Bu repoyu klonlayın:
   git clone https://github.com/onuracarsoy/stokyonetimprogrami.git

2. Visual Studio ile projeyi açın.

3. NuGet paketlerini geri yükleyin (Visual Studio otomatik yapmazsa `Tools > NuGet Package Manager > Restore`).

4. Projeyi derleyip çalıştırın (F5).

Not: Uygulama SQL Server LocalDB kullanacak şekilde yapılandırılmıştır. LocalDB yüklü değilse [SQL Server Express LocalDB](https://learn.microsoft.com/tr-tr/sql/database-engine/configure-windows/sql-server-express-localdb) kurmanız gerekebilir.

## Veritabanı yapılandırması
- Bağlantı dizesi genelde `app.config` veya `Properties/Settings.settings` içinde bulunur. Örnek LocalDB bağlantı dizesi:
  ```
  Data Source=(LocalDB)\MSSQLLocalDB;AttachDbFilename=|DataDirectory|\StokDB.mdf;Integrated Security=True
  ```
- Repoda hazır bir `.mdf` veya SQL script'i varsa proje kökünde/`Database` klasöründe bulunur; yoksa yeni bir LocalDB veritabanı oluşturup tabloları elle eklemeniz gerekebilir.
- Eğer tablolarla ilgili bir SQL scripti görmüyorsanız, bana bildirirseniz mevcut schema için örnek script hazırlayabilirim.

## Ekran Görüntüleri
(Görseller repoda bulunan bağlantılar üzerinden korunmuştur.)

Giriş Ekranı  
![GirişYap](https://user-images.githubusercontent.com/115365153/224332614-318fa5f9-d3f8-4657-8445-22728e9602a3.png)

Ürün Ekleme (Mobil)  
![MobileEkle](https://user-images.githubusercontent.com/115365153/224332712-f26151f6-6acc-42ea-a659-fc37da5387e1.png)

Ürün Ekleme (Aksesuar)  
![AksesuarEkle](https://user-images.githubusercontent.com/115365153/224332735-ca3d1288-68c0-4592-a7fb-d498c28cb56c.png)

Fatura Ekleme  
![FaturaEkle](https://user-images.githubusercontent.com/115365153/224332755-b6b98550-34a7-4016-a710-5c529b2224c3.png)

## Hızlı kullanım rehberi
- Yeni ürün eklemek için "Yeni Ekle" formunu doldurun ve kaydedin.
- Ürünleri listeleyip arama çubuğundan filtreleyebilirsiniz.
- Fatura oluştururken ilgili ürünleri seçip miktar ve fiyat bilgilerini girin.

## Sorun giderme
- Uygulama veritabanına bağlanamıyorsa: LocalDB kurulumunu ve connection string'i kontrol edin.
- Eksik NuGet paketleri hatası alırsanız: Visual Studio'da paketleri geri yükleyin veya `dotnet restore` çalıştırın (project türüne göre).

## Katkıda bulunma
- Hatalar, iyileştirme önerileri veya yeni özellik talepleri için Issues açabilirsiniz.
- Kod katkısı yapmak isterseniz fork -> branch -> pull request akışını kullanın.

## Lisans
Bu proje açık kaynaklıdır. (Varsa spesifik bir lisans ekleyin; yoksa belirtin veya bir lisans dosyası ekleyin.)

## İletişim
Geliştirici: onuracarsoy  
E-posta veya GitHub üzerinden iletişime geçebilirsiniz.

---
Not: İstediğiniz takdirde bu dosyayı doğrudan repoya commit edebilirim ve/veya içerikte değişiklik yapabilirim (ör. detaylı veritabanı scriptleri, lisans türü, geliştirme notları). Fotoğraflar repoda olduğu gibi korunmuştur.