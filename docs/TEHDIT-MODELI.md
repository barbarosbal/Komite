# Komite — Tehdit modeli

Durum: başlangıç araştırma modeli. Aşağıdaki önlemler uygulanmış kontrol veya kalan risk kabulü değildir. Gerçek kullanım [yayın kapılarına](YAYIN-KONTROL-LISTESI.md) bağlıdır.

## Korunacak varlıklar ve saldırganlar

Varlıklar: kimlik/uygunluk bilgisi, katılım olgusu, bireysel tercih, anlama yanıtı, davet yetkisi, soru sürümü, sonuç bütünlüğü ve özgür katılım. Katılmış olmak bile hassas olabilir.

Anlama yanıtı yalnız içerik kalitesi verisi değildir: nadir cevap örüntüsü, zamanlama, tekrar deneme sayısı veya küçük bir rolle birleştiğinde kimlik ya da tercih çıkarımına yardım edebilir. [Karar modelindeki anlama kontrolü ve sonuç sözleşmesi](KARAR-MODELI.md#anlama-kontrolü-anlama-ile-yönlendirme-arasındaki-sınır) bu nedenle aynı ifşa sınırlarına tabidir.

Saldırganlar: dış ağ gözlemcisi, kötü niyetli katılımcı, davet sahibi, karar sahibi/işveren, kötü niyetli veya ele geçirilmiş işletmeci, birlikte hareket eden servisler, saldırgan istemci ve tedarik zinciri. Yalnız dürüst işletmeci varsayımı yeterli değildir.

Güven sınırları: katılımcı cihazı → uygunluk/kimlik servisi; cihaz → tercih alım servisi; alım → toplulaştırma; işletmeciler → kayıt/yedek/izleme; toplu rapor → dış bilgiye sahip okuyucu. Ayrı servis veya veri tabanı kullanmak tek başına bağımsız güven alanı kurmaz.

## Tehdit kaydı

Öncelikler [Güvenlik](../GUVENLIK.md) ölçeğindedir; bu tablo gelecekteki kullanım için doğal riski gösterir, mevcut bir uygulamada doğrulanmış açık listesi değildir. Her satırın durumu **açık**tır.

| Tehdit ve örnek saldırı | İz / öncelik | Araştırılacak kontrol ve doğrulama | Kalan risk / durdurma koşulu |
| --- | --- | --- | --- |
| **Anlama üzerinden yönlendirme:** yalnız bir görüşü doğru gösteren soru ve kaynaklar | T01 · Yüksek | Karşı görüş incelemesi; soru sürümleme; yanlış yanıtın katılımı/ağırlığı değiştirmediğini test | Tarafsızlık salt test puanıyla kanıtlanamaz; yönlendirme bulgusunda tur durur |
| **Küçük grupta kimliği çıkarma:** tek kişi, oybirliği, bilinen diğer tercihler | T02 · Yüksek | Minimum kohort; küçük hücre ve tamamlayıcı toplam bastırma; dış bilgi, kesişim ve tekrar yayın saldırıları | Eşik tek başına garanti değil; risk değerlendirmesi yoksa sonuç yayımlanmaz |
| **Üstveri ve zamanlama ilişkilendirmesi:** IP, oturum, cihaz, istek boyutu, log ve zaman eşleştirme | T03 · Yüksek | Veri envanteri; kayıt minimizasyonu; gecikme/toplu iletim/örtü trafiği deneyleri; ağ ve log birleştirme testi | Küresel gözlemci ve düşük trafik korunmuş varsayılmaz; tanımlanamayan gözlem kapsamı gerçek kullanımı durdurur |
| **İşletmecilerin birlikte hareket etmesi:** uygunluk, alım ve analitik verilerinin birleştirilmesi | T04 · Yüksek | Yetki ayrımı; bağımsız yönetim; eşikli güven modelleri; birleşik veri erişimiyle saldırı deneyi | Aynı yönetici, bulut hesabı veya yedek tüm sınırları aşabilir; güven eşiği belirsizse ilerlenmez |
| **Baskı ve oy satın alma:** ekran gösterme, cihaz gözetimi, hesap/kanıt devri | T05 · Yüksek | Tehdit senaryosu ve gönüllülük incelemesi; tercih kanıtı üretmeyen akışların araştırılması | Anonimlik baskıyı çözmez; denetlenen cihazdaki kullanıcı güvence altında değildir; ilk pilotta yüksek baskı bağlamı hariç |
| **İstemcinin ele geçirilmesi:** değiştirilmiş arayüz, eklenti veya kötü bağımlılık tercihi çalar/değiştirir | T06 · Yüksek | Bağımlılık/kaynak bütünlüğü; asgari istemci; hedefli içerik değiştirme testleri; doğrulanabilir dağıtım araştırması | Sunucu kriptografisi ele geçirilmiş cihazı iyileştirmez; istemci kanıtı olmadan güvenli kullanım iddiası yok |
| **Davet suistimali:** devredilen davet, yeniden kullanım, sahte insan ve seçici dışlama | T07 · Yüksek | Bağlam/süre sınırı; atomik tek kullanım; eşzamanlı tekrar deneyi; itiraz ve iptal tasarımı | Davet veya hesap tekil insan kanıtı değildir; kurtarma/yeniden verme çoklu katılım yaratabilir |
| **Örnekleme yanlılığı:** karar sahibinin yalnız destekçileri davet etmesi; dijital dışlanma ve yanıt vermeme | T08 · Yüksek | Önceden yöntem açıklaması; kapsam/yanıt vermeme raporu; çelişen örneklem senaryoları | Kriptografi temsiliyet sağlamaz; temsil iddiası desteklenmiyorsa rapordan çıkarılır |
| **Sonuç manipülasyonu:** silme, sahte bildirim, yeniden oynatma, çift sayım, geç yanıt | T09 · Yüksek | Tur/sürüm bağlama; atomik kabul; bütünlük ve bağımsız yeniden hesaplama araştırması; hata/enjeksiyon testleri | Geçerli imza dürüst sayımı veya gerçek insanı kanıtlamaz; bütünlük belirsizse sonuç yok |
| **İhlal sonrası bağlantı:** anahtar, yedek ve eski logların ele geçirilmesi | T10 · Yüksek | Veri yaşam döngüsü; silme/yedek süresi; anahtar döndürme; geçmiş verilerle korelasyon deneyi | Silme beyanı veya diskte şifreleme geçmiş bağlantısızlık kanıtı değildir |
| **Erişilebilirlik saldırısı:** seçici engelleme, kapasite tüketimi, hizmet kesintisi | T11 · Orta | Kapasite sınırları; kesinti/yeniden deneme testleri; önceden tanımlı uzatma/iptal kuralı | Eksik katılım sonucu çarpıtabilir; gizli biçimde kayıp yanıtları geçerli sonuç sayma |
| **Öznitelik ve sunum bağlantısı:** nadir rol, sabit takma ad veya tur-ötesi tanımlayıcı | T12 · Yüksek | Asgari öznitelik açıklama; turla sınırlı bağlantı; farklı tur ve küçük grup eşleştirme testi | Kriptografik sunum bağlantısız olsa bile açıklanan bilgi kişiyi ayırt edebilir |

## Küçük grup ifşa politikası

Küçük gruplar uç durum değildir. Minimum kohort eşiği, alt hücre bastırma, tamamlayıcı bastırma, kesişen gruplar, tekrar sorgular ve farklı zamanlarda raporlanan toplamlar birlikte tasarlanmalıdır. Oybirliği ve dış bilgi riski de incelenir. Anlama kontrolü ve katılım sayıları muaf değildir.

Kesin eşik, sorgu bütçesi ve zaman penceresi henüz onaylanmadı. Güvenli varsayılan **güvenli kapanma**: onaylı politika yoksa veya risk ölçülemiyorsa sonuç yok. Sabit bir “en az 5/10 kişi” kuralı burada güvenlik kanıtı olarak sunulmaz.

Çapraz bağ kuralı: tercih toplamları, anlama yanıtları/puanları, katılım ve yanıt vermeme sayıları, hata/iptal bilgisi, alt grup kırılımları ve farklı zamanlardaki raporlar tek bir birleşik yayın yüzeyi olarak değerlendirilir. Alanları ayrı tabloda göstermek bağımsızlaştırmaz; bir rapor diğerinde bastırılmış değeri çıkarabiliyorsa ikisi birlikte yayımlanmaz. Uygulama ayrıntıları [Karar Modeli — Sonuç sözleşmesi](KARAR-MODELI.md#sonuç-sözleşmesi) ile aynı sürümde tutulur.

## Test kanıtının sınırı

Her deney saldırgan görünürlüğünü, veri boyutunu, kohort yapısını, başarı ölçütünü, başarısız örnekleri, sürümü ve yeniden çalıştırma yolunu kaydetmelidir. Sentetik veride başarısız saldırı denemesi gerçek dünyada anonimliği kanıtlamaz. Her aday mimari bu tabloya kontrol sahibi, test bağlantısı ve kabul edilmemiş kalan riskleri eklemeden değerlendirmeden çıkamaz.

## English summary

All threats remain open design risks, not accepted production risks. Threats include framing/priming, small-cohort re-identification, metadata and timing correlation, colluding operators, coercion, compromised clients, invitation abuse, sampling bias and result tampering. Cryptography does not eliminate social or endpoint threats. No approved disclosure policy means no result publication.
