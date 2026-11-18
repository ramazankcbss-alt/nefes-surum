# Nefes – Gizlilik Politikası

Son güncelleme: 18 Kasım 2026

Nefes, sigarayı kademeli olarak azaltıp bırakmak isteyen kişiler için hazırlanmış kişisel bir takip uygulamasıdır. Bu politika, uygulamanın hangi bilgileri nasıl işlediğini açıklar. Uygulama 6698 sayılı Kişisel Verilerin Korunması Kanunu (KVKK) dikkate alınarak, mümkün olan en az veriyle çalışacak şekilde tasarlanmıştır.

## 1. Telefonda saklanan bilgiler

Aşağıdaki bilgiler **yalnızca kullanıcının telefonunda** saklanır; geliştiriciye veya herhangi bir sunucuya gönderilmez:

- Günlük sigara kayıtları (saat, kullanıcının seçtiği yer etiketi, isteğe bağlı tetikleyici), atlatılan istekler ve ikram edilen sigara sayısı
- Öğün, çay, kahve ve su kayıtları
- Haftalık kilo bilgisi ve başlangıç bilgileri (günlük tüketim, bırakma günü, paket fiyatı)
- Sigara alım ve stok kayıtları
- Kullanıcının eklediği sağlık raporları (fotoğraf veya belge) ve bu raporlardan telefonda okunan değerler
- Kullanıcının kaydettiği "Ev" ve "İş yeri" konumları
- Uygulama ayarları ve davet kodu

Bu bilgiler, uygulama içindeki **Ayarlar → Tüm verileri sil** ile veya uygulama kaldırılarak kalıcı olarak silinebilir.

## 2. İzinler ve kullanım amaçları

- **Konum:** Yalnızca kullanıcı "Sigara içildi" kaydı yaptığı anda bir kez alınır ve kayıtlı yerlere göre bir yer etiketi önermek için kullanılır. Her kayıtta koordinat değil, yalnızca etiket (Ev, İş yeri, Dışarıda) saklanır. Arka planda konum takibi yapılmaz.
- **Kamera, galeri ve dosyalar:** Yalnızca kullanıcı rapor eklemek istediğinde kullanılır; seçilen dosya uygulamanın kendi alanına kopyalanır.
- **Bildirimler:** Günlük değerlendirme, öğün ve su hatırlatmaları telefonda planlanır; sunucu kullanılmaz.
- **İnternet:** Yalnızca aşağıdaki 3, 4, 6a ve 6b maddelerinde belirtilen amaçlarla kullanılır.

## 3. İsimsiz kullanım istatistiği (isteğe bağlı)

Kullanıcı izin verirse uygulama, Google Firebase (Cloud Firestore, Avrupa bölgesi) üzerindeki **toplam sayaçları** birer artırır: yeni kurulum sayısı, haftalık kullanan telefon sayısı ve verilen memnuniyet puanı (1–5). Kişi başına kayıt tutulmaz; kimlik, isim, telefon numarası, e-posta, konum, davet kodu veya sigara ve sağlık bilgisi gönderilmez. Bu tercih ilk açılışta ve **Ayarlar** ekranında kapatılabilir. Teknik iletişim sırasında hizmet sağlayıcı (Google) IP adresini görebilir; geliştirici bu bilgiye erişmez ve saklamaz.

## 4. Güncelleme kontrolü

Google Play'den kurulan sürüm güncellemeleri yalnızca Google Play üzerinden alır ve kendi başına güncelleme kontrolü yapmaz. Doğrudan dağıtılan sürüm ise açıldığında yeni sürüm olup olmadığını GitHub üzerindeki herkese açık sürüm sayfasından kontrol eder. Bu sırada kullanıcıya ait hiçbir bilgi gönderilmez; teknik iletişim sırasında GitHub IP adresini görebilir.

## 5. Rapor okuma

Sağlık raporlarındaki yazılar Google ML Kit ile **telefonda** okunur; rapor görüntüsü ve metni sunucuya gönderilmez. ML Kit, Google'a yalnızca performans ve kullanım ölçümleri iletir.

## 6. Kullanıcının başlattığı paylaşımlar

Haftalık özet paylaşımı ve raporu "yorum için gönderme" yalnızca kullanıcı onayladığında, kullanıcının seçtiği uygulama aracılığıyla yapılır. Haftalık özete kilo bilgisi ve raporlar eklenmez.

## 6a. Aile takibi (isteğe bağlı, açık rızaya bağlı)

Kullanıcı açık rıza vererek Aile Takibi özelliğini başlatırsa, günlük özet (sigara sayısı ve hedef, son 7 günün sayıları, hedef serisi, atlatılan istek sayısı, kupon ve kumbara tutarı, stok sayımı sonucu) telefonda AES-256-GCM ile şifrelenerek Google Firebase (Firestore) sunucusuna gönderilir. Şifre anahtarı yalnızca kullanıcının ve aile kodunu girdiği yakınının telefonunda bulunur; sunucu ve uygulama geliştiricisi içeriği okuyamaz. Konum, sigara saatleri, kilo, sağlık raporları, karbonmonoksit ölçümleri, öğün ve içecek kayıtları paylaşılmaz. Yakının gönderdiği destek mesajları da aynı şekilde şifrelenir. Kullanıcı paylaşımı istediği an durdurabilir; durdurulduğunda sunucudaki şifreli veriler silinir. Aile üyesi modunda hesap açılmaz, kimlik bilgisi istenmez.

## 6b. Destek Ol kampanyası (isteğe bağlı)

Kullanıcı onay vererek kampanyayı başlatırsa, kendi seçtiği kişilere gönderdiği bağlantıda adı, içilmeyen sigara sayısı, programdaki gün sayısı ve davet kodu yer alır. Bu bilgiler bağlantının "#" işaretinden sonraki bölümünde bulunur; sayfayı barındıran sunucuya gönderilmez, yalnızca bağlantıyı açan kişinin tarayıcısında gösterilir. Bağlantıyı açan kişi "Bağışımı yaptım" dediğinde, kişinin kimliği alınmadan yalnızca hangi kuruma destek verildiği ve seçilen hazır mesaj sayaç olarak Firestore'a kaydedilir. Uygulama ve destek sayfası bağış toplamaz, ödeme bilgisi işlemez; bağış, kurumların kendi resmî sitelerinde yapılır.

## 7. Reklam ve veri satışı

Uygulamada reklam bulunmaz. Kişisel veriler satılmaz, kiralanmaz veya üçüncü kişilerle paylaşılmaz.

## 8. Yaş sınırı

Uygulama 18 yaş ve üzeri kullanıcılar içindir.

## 9. Sağlık bilgilendirmesi

Nefes bilgilendirme amaçlıdır; tıbbi tanı veya tedavi yerine geçmez. Ücretsiz destek için ALO 171 Sigara Bırakma Danışma Hattı aranabilir.

## 10. Haklarınız ve iletişim

KVKK'nın 11. maddesi kapsamındaki haklarınızla ilgili sorularınız için Google Play mağaza sayfasında yer alan geliştirici e-posta adresinden iletişime geçebilirsiniz. Uygulama verileri telefonunuzda tutulduğundan, verilerinize erişim ve silme işlemlerini uygulama içinden doğrudan yapabilirsiniz.

Bu politika değiştiğinde güncel hâli bu sayfada yayınlanır.
