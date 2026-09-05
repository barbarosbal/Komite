# Komite — Proje yönetişimi

Bu belge açık kaynak projenin bakım sürecini tanımlar. Komite üzerinden yönetici/temsilci seçimi veya bağlayıcı karar üretimi tasarlamaz. [Ürün kapsamı](KAPSAM.md) değişmez.

## Başlangıç sorumluluğu

Proje sahibi ve başlangıç bakım sorumlusu Barbaros Hayrettin Bal’dır; iletişim [README.md](README.md) içindedir. Seçilmiş kurul, bağımsız güvenlik ekibi, çoklu bakım sorumlusu veya kesintisiz destek varmış gibi iddiada bulunulmaz.

Katkıcı değişiklik önerir ve kanıt sağlar. İncelemeci bulguları ve inceleme sınırlarını kaydeder. Proje sahibi kapsam, yayın ve yetki kararlarını verir; yeni bakım yetkileri açıkça kaydedilmeden varsayılmaz. Çıkar çatışması olan kişi bunu açıklar; anlaşmazlıkta gerekçe ve karşıt görüş PR’da korunur.

## Karar ve birleştirme akışı

1. Teklif, kaynaklar, alternatifler, kabul ölçütleri ve kapsam dışı alanlar açıklanır.
2. Değişiklik ayrı dal ve PR üzerinden değerlendirilir. Yorum sayısı veya çoğunluk, kabul kararı değildir.
3. İncelemeci engelleyici/yüksek/orta/düşük bulgularını, dosya/sürüm ve kanıtla ilişkilendirir. Öz denetim açıkça öz denetim olarak etiketlenir.
4. Düzeltme sonrası son değişiklik kaydı yeniden doğrulanır. Bu temel yayını için açık belge bulgusu kalmadan birleştirme yapılmaz.
5. Onay kapsamı ve birleştirilen sürüm PR’da kaydedilir. Kullanıcının bu belge temelini yayımlama yetkisi, yalnız temiz belge değişikliğinin birleştirilmesini kapsar; ürün dağıtımı veya açık güvenlik riskinin kabulü değildir.

Rutin belge düzenleme, önceden açıkça verilmiş yayın yetkisi kapsamında yapılabilir. Yeni güvenlik/mimari seçimi, kapsam genişlemesi, gerçek katılımcılı pilot, üretim dağıtımı, sır/yetki değişikliği veya geri döndürülemez işlem ayrı insan onayı gerektirir. Kritik/yüksek AI bulguları yalnız AI tarafından kapatılmış sayılamaz.

## Bağımsızlık ve uygulanabilirlik sınırı

Bu temel yayınındaki ikinci okuma aynı yazarın öz denetimi olabilir; bağımsız uzman veya insan denetimi değildir. Gerçek kullanıma geçişte bağımsız güvenlik/mahremiyet incelemesi gereklidir. Tek bakım sorumlusu riski saklanmaz; uzman incelemesi bulunamıyorsa üretim hazırlığı kapısı geçilmez.

Bu metin GitHub branch protection (dal koruması), zorunlu incelemeci veya CI (sürekli entegrasyon) kuralını kendiliğinden etkinleştirmez. Kuralların gerçekten zorunlu uygulanması ayrı ayar ve doğrulama gerektirir. Mevcut temel yayın, elle yürütülen ve PR’da kanıtlanan kontroldür; otomatik koruma varmış gibi rozet kullanılmaz.

## Kayıt ve yetki ayrımı

Depodaki belgeler projenin kamuya açık tasarım/kapsam referansıdır. GitHub değişiklik ve inceleme kanıtlarını taşır; özel şirket karar kayıtlarının yerine geçmez. Kamusal PR’a yalnız yayımlanması uygun bağlam taşınır. İnceleme için gerekli gerekçe özel sistem erişimine bağımlı bırakılmaz. Yetki veya kayıtlar arasında çelişki varsa sessizce yeniden yorumlanmaz; proje sahibine sunulur.

## Özel bulgudan kamusal düzeltmeye sınır

[Güvenlik Politikası](GUVENLIK.md) özel bildirimin ilk temasını yönetir; bu belge ise neyin kamusal belge değişikliğine dönüşebileceğini yönetir. Sömürü yolu, kişisel veri, gizli erişim bilgisi veya yeniden tanımlama verisi kamusal PR’a kopyalanmaz. Kamusal düzeltme yalnız sorunu anlamak ve yanlış iddiayı gidermek için gereken, saldırıyı kolaylaştırmayan en az bağlamı taşır. Bildiricinin adı ve atıf biçimi açık rızası olmadan yayımlanmaz. Düzeltmenin kamusal olması güvenlik riskinin kabul edildiği, gerçek kullanıma izin verildiği veya özel ayrıntıların açıklanacağı anlamına gelmez.

## English summary

The project owner is the initial maintainer. Changes use branches, documented review and explicit authority. This documentation launch can use disclosed self-review under the owner's existing authorization; it is not independent security approval. Production, security-risk acceptance and expanded scope require separate human decisions. Written policy does not itself enable repository protections.
