🌧️ RainClinic - Randevu Yönetim Sistemi
RainClinic, kullanıcıların online randevu almasını ve takip etmesini sağlayan bir randevu yönetim sistemidir. Kullanıcılar randevu oluşturup takibini yapabilir, admin paneli üzerinden yönetim işlemleri gerçekleştirilebilir.

🚀	Veritabanı VPS sunucusunda çalışmaktadır. ConnectionStrings dosyasında VPS sunucusu IP ve veritabanı bağlantı bilgileri bulunmaktadır. Bu bilgilerin kesinlikle paylaşılmaması gerekmektedir.

🚀	Proje Yayını: Mevcut proje, VPS sunucusu üzerinden Docker ile yayınlanmaktadır. Projeye ulaşmak için aşağıdaki bağlantıyı kullanabilirsiniz: rainclinic.blog. Projeyi Visual Studio'da çalıştırmadan, 
canlı olarak belirtilen bağlantı üzerinden kullanmak VPS sunucusunun sağlığı için önemlidir.

🚀	Hatırlatma: Visual Studio'daki connectionStrings dosyası production ortamına bağlıdır.

🚀 Özellikler

✅ Kullanıcılar:
Kullanıcılar randevu oluştururken isim, e-posta, telefon, doktor seçimi ve muayene tipini (yüz yüze / online) belirler.
E-posta onayı gereklidir. Kullanıcı, e-posta onayı yapmadan giriş yapamaz.
Tek aktif randevu kuralı: Kullanıcı, mevcut randevusu kapatılmadan yeni randevu oluşturamaz.
Kendi randevularını listeleyebilir ancak değiştiremez veya silemez.

✅ Admin Paneli:
Tüm randevuları yönetir: Randevuları listeleyebilir, düzenleyebilir, silebilir.
Kullanıcının e-posta onay durumunu görüntüleyebilir.
Randevu durumlarını yönetir: "Bekliyor", "İşleme Alındı", "Tamamlandı", "İptal Edildi" gibi statüler atanabilir.

✅ Diğer Özellikler:
Kimlik doğrulama: ASP.NET Core Identity ile güvenli giriş/çıkış işlemleri.
E-posta doğrulama: Kullanıcıya doğrulama bağlantısı gönderilir.
Mobil ve masaüstü uyumlu: Tüm cihazlarda responsive tasarım.
Docker ve Reverse Proxy Desteği: Çoklu site yayını için Docker-Compose + Nginx Proxy yapılandırıldı.

🔑 Kullanıcı Rolleri ve Yetkiler
Rol	Yetkiler
Admin	Tüm randevuları yönetebilir, kullanıcıları düzenleyebilir
User Sadece kendi randevularını görüntüleyebilir, değiştiremez
   
✅ Güvenlik Önlemleri
JWT ve Cookie Authentication kullanıldı.
HTTPS zorunlu yapıldı (SSL/TLS ile).
Rate Limiting ve Brute-Force Protection eklendi.
SQL Injection ve XSS önlenmesi için veri giriş doğrulama (Data Annotation) kullanıldı.

🎨 UI/UX Mobil Uyumluluk
Bootstrap 5 ile responsive tasarım.
Admin Paneli & Kullanıcı Arayüzü Ayrı.
Mobil, Tablet ve Masaüstü için optimize edildi.
