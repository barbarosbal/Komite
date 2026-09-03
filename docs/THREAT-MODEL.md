# Komite — Tehdit modeli

Durum: başlangıç araştırma modeli. Aşağıdaki önlemler uygulanmış kontrol veya kalan risk kabulü değildir. Gerçek kullanım [yayın kapılarına](RELEASE-CHECKLIST.md) bağlıdır.

## Korunacak varlıklar ve saldırganlar

Varlıklar: kimlik/uygunluk bilgisi, katılım olgusu, bireysel tercih, anlama yanıtı, davet yetkisi, soru sürümü, sonuç bütünlüğü ve özgür katılım. Katılmış olmak bile hassas olabilir.

Saldırganlar: dış ağ gözlemcisi, kötü niyetli katılımcı, davet sahibi, karar sahibi/işveren, kötü niyetli veya ele geçirilmiş işletmeci, birlikte hareket eden servisler, saldırgan istemci ve tedarik zinciri. Yalnız dürüst işletmeci varsayımı yeterli değildir.

Güven sınırları: katılımcı cihazı → uygunluk/kimlik servisi; cihaz → tercih alım servisi; alım → toplulaştırma; işletmeciler → kayıt/yedek/izleme; toplu rapor → dış bilgiye sahip okuyucu. Ayrı servis veya veri tabanı kullanmak tek başına bağımsız güven alanı kurmaz.

## Tehdit kaydı

Öncelikler [SECURITY.md](../SECURITY.md) ölçeğindedir; bu tablo gelecekteki kullanım için doğal riski gösterir, mevcut bir uygulamada doğrulanmış açık listesi değildir. Her satırın durumu **open (açık)**tır.

| ID / öncelik | Tehdit ve örnek saldırı | Araştırılacak kontrol ve doğrulama | Kalan risk / durdurma koşulu |
| --- | --- | --- | --- |
| T01 / HIGH | Understanding Gate üzerinden framing/priming: yalnız bir görüşü doğru gösteren soru ve kaynaklar | Karşı görüş incelemesi; soru sürümleme; yanlış yanıtın katılımı/ağırlığı değiştirmediğini test | Tarafsızlık salt test puanıyla kanıtlanamaz; yönlendirme bulgusunda tur durur |
| T02 / HIGH | Küçük kohortlarda deanonymization (kimliği yeniden ortaya çıkarma): tek kişi, oybirliği, bilinen diğer tercihler | Minimum kohort; küçük hücre ve tamamlayıcı toplam bastırma; dış bilgi, kesişim ve tekrar yayın saldırıları | Eşik tek başına garanti değil; risk değerlendirmesi yoksa sonuç yayımlanmaz |
| T03 / HIGH | Metadata/timing correlation (üstveri/zamanlama ilişkilendirmesi): IP, oturum, cihaz, istek boyutu, log ve zaman eşleştirme | Veri envanteri; kayıt minimizasyonu; gecikme/toplu iletim/örtü trafiği deneyleri; ağ ve log birleştirme testi | Küresel gözlemci ve düşük trafik korunmuş varsayılmaz; tanımlanamayan gözlem kapsamı gerçek kullanımı durdurur |
| T04 / HIGH | Operator collusion (işletmeci işbirliği): uygunluk, alım ve analitik verilerinin birleştirilmesi | Yetki ayrımı; bağımsız yönetim; eşikli güven modelleri; birleşik veri erişimiyle saldırı deneyi | Aynı yönetici, bulut hesabı veya yedek tüm sınırları aşabilir; güven eşiği belirsizse ilerlenmez |
| T05 / HIGH | Coercion/vote buying (baskı/oy satın alma): ekran gösterme, cihaz gözetimi, hesap/kanıt devri | Tehdit senaryosu ve gönüllülük incelemesi; tercih kanıtı üretmeyen akışların araştırılması | Anonimlik baskıyı çözmez; denetlenen cihazdaki kullanıcı güvence altında değildir; ilk pilotta yüksek baskı bağlamı hariç |
| T06 / HIGH | Client compromise (istemcinin ele geçirilmesi): değiştirilmiş arayüz, eklenti, kötü bağımlılık tercihi çalar/değiştirir | Bağımlılık/kaynak bütünlüğü; asgari istemci; hedefli içerik değiştirme testleri; doğrulanabilir dağıtım araştırması | Sunucu kriptografisi ele geçirilmiş cihazı iyileştirmez; istemci kanıtı olmadan güvenli kullanım iddiası yok |
| T07 / HIGH | Invitation abuse (davet suistimali): devredilen davet, yeniden kullanım, sahte insan ve seçici dışlama | Bağlam/süre sınırı; atomik tek kullanım; eşzamanlı tekrar deneyi; itiraz ve iptal tasarımı | Davet veya hesap tekil insan kanıtı değildir; kurtarma/yeniden verme çoklu katılım yaratabilir |
| T08 / HIGH | Sampling bias: karar sahibinin yalnız destekçileri davet etmesi; dijital dışlanma ve yanıt vermeme | Önceden yöntem açıklaması; kapsam/yanıt vermeme raporu; çelişen örneklem senaryoları | Kriptografi temsiliyet sağlamaz; temsil iddiası desteklenmiyorsa rapordan çıkarılır |
| T09 / HIGH | Sonuç manipülasyonu: silme, sahte bildirim, replay (yeniden oynatma), çift sayım, geç yanıt | Tur/sürüm bağlama; atomik kabul; bütünlük ve bağımsız yeniden hesaplama araştırması; hata/enjeksiyon testleri | Geçerli imza dürüst sayımı veya gerçek insanı kanıtlamaz; bütünlük belirsizse sonuç yok |
| T10 / HIGH | İhlal sonrası bağlantı: anahtar, yedek ve eski logların ele geçirilmesi | Veri yaşam döngüsü; silme/yedek süresi; anahtar döndürme; geçmiş verilerle korelasyon deneyi | Silme beyanı veya at-rest encryption (diskte şifreleme) geçmiş bağlantısızlık kanıtı değildir |
| T11 / MEDIUM | Availability (erişilebilirlik) saldırısı: seçici engelleme, kapasite tüketimi, hizmet kesintisi | Kapasite sınırları; kesinti/yeniden deneme testleri; önceden tanımlı uzatma/iptal kuralı | Eksik katılım sonucu çarpıtabilir; gizli biçimde kayıp yanıtları geçerli sonuç sayma |
| T12 / HIGH | Öznitelik/sunum bağlantısı: nadir rol, sabit takma ad veya tur-ötesi tanımlayıcı | Asgari öznitelik açıklama; turla sınırlı bağlantı; farklı tur ve küçük grup eşleştirme testi | Kriptografik sunum bağlantısız olsa bile açıklanan bilgi kişiyi ayırt edebilir |

## Küçük grup ifşa politikası

Küçük gruplar uç durum değildir. Minimum kohort eşiği, alt hücre bastırma, tamamlayıcı bastırma, kesişen gruplar, tekrar sorgular ve farklı zamanlarda raporlanan toplamlar birlikte tasarlanmalıdır. Oybirliği ve dış bilgi riski de incelenir. Anlama kontrolü ve katılım sayıları muaf değildir.

Kesin eşik, sorgu bütçesi ve zaman penceresi henüz onaylanmadı. Güvenli varsayılan **fail-closed (güvenli kapanma)**: onaylı politika yoksa veya risk ölçülemiyorsa sonuç yok. Sabit bir “en az 5/10 kişi” kuralı burada güvenlik kanıtı olarak sunulmaz.

## Test kanıtının sınırı

Her deney saldırgan görünürlüğünü, veri boyutunu, kohort yapısını, başarı ölçütünü, başarısız örnekleri, sürümü ve yeniden çalıştırma yolunu kaydetmelidir. Sentetik veride başarısız saldırı denemesi gerçek dünyada anonimliği kanıtlamaz. Her aday mimari bu tabloya kontrol sahibi, test bağlantısı ve kabul edilmemiş kalan riskleri eklemeden değerlendirmeden çıkamaz.

## English summary

All threats remain open design risks, not accepted production risks. Threats include framing/priming, small-cohort re-identification, metadata and timing correlation, colluding operators, coercion, compromised clients, invitation abuse, sampling bias and result tampering. Cryptography does not eliminate social or endpoint threats. No approved disclosure policy means no result publication.
