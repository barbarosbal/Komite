# Komite — Mimari araştırma yönleri

Durum: alternatif değerlendirmesi. Seçilmiş mimari, uygulanmış protokol veya güvenlik garantisi yoktur. “Tek kapı, tek anahtar” yalnız metafordur; aşağıdaki sorulara cevap vermez.

## Ayrılması gereken problemler

İnsan olma, küresel tekillik, bağlamsal uygunluk, tur başına tek katılım, kimlik-tercih bağlantısızlığı, ağ mahremiyeti, sayım bütünlüğü ve güvenli sonuç ifşası ayrı problemlerdir. Birinin çözümü diğerine devredilemez. **Global unique-human verification (küresel tekil insan doğrulaması) + privacy (mahremiyet) + sybil resistance (sahte/çoklu kimlikle katılıma dayanıklılık) birlikte çözülmüş kabul edilmez.**

## Karşılaştırma

Bu tablo Komite için araştırma değerlendirmesidir; kaynakların Komite’yi doğruladığı anlamına gelmez. Kaynak künyeleri [RESEARCH.md](../RESEARCH.md) içindedir.

| Yön | Araştırılan katkı | Güven varsayımı / maliyet | Tek başına çözmediği alan | Sonraki deney |
| --- | --- | --- | --- | --- |
| Blind signatures (kör imzalar), R1 | İmzalayanın açık belirteci görmeden yetkilendirmesi; verme/kullanma bağlantısını azaltma | Doğru kriptografik uygulama, anahtar dağıtımı ve güvenilir uygunluk/verme politikası; ek tekrar-kullanım kaydı | Küresel insan tekilliği, token devri, ağ korelasyonu, küçük grup ifşası | Sahte/tekrar/eşzamanlı kullanım; anahtar/bağlam ayrımı; verme ve kullanım loglarını birleştiren saldırgan |
| Anonymous credentials (anonim yetki belgeleri), R2 | Gerekli öznitelikleri seçici açıklama ve bağlantısız sunum araştırması | İhraççı modeli, ispat uygulaması, iptal/kurtarma, kullanıcı anahtarı ve öznitelik mahremiyeti; daha karmaşık yaşam döngüsü | Gerçek insan kaydı, nadir öznitelikle tanınma, baskı; anonim sunum tek başına turda tek yanıt sağlamaz | Turla sınırlı tekrar önleme ve turlar arası bağlantısızlığı birlikte test; kayıp belge ve iptal senaryosu |
| Mixnets (karıştırma ağları), R3 | İleti giriş/çıkış eşleştirmesini zorlaştırma; trafik analizini inceleme | Seçilen protokolün dürüst düğüm/işbirliği varsayımı; gecikme, bant genişliği, örtü trafiği ve kullanılabilirlik maliyeti | Uygunluk, tekillik, ele geçirilmiş uç cihaz, nihai rapordan çıkarım | Küçük/düşük trafikli grup ve gözlemci modeliyle gecikme/ilişkilendirme deneyi |
| Practical privacy (uygulanabilir mahremiyet), R4 | Asgari veri, erişim ayrımı, kısa saklama, toplulaştırma ve ifşa kontrolünden oluşan işletim yaklaşımı | İşletmeci disiplinine bağımlılık; denetlenebilir veri envanteri; yararlılık/mahremiyet ödünleşimi | Kriptografik bağlantısızlık, işbirlikçi işletmecilere veya güçlü gözlemciye genel güvence | Log/yedek envanteri; küçük hücre, tamamlayıcı toplam ve tekrar yayın saldırıları |

Bu yönler aynı katmandaki rakip ürünler değildir; bazıları birlikte değerlendirilebilir. Birleştirme güvenlik özelliklerini otomatik olarak toplamaz. Ortak tanımlayıcılar, hata mesajları, öznitelikler ve zamanlama bütün kompozisyonu bozabilir.

## Aday sistem sınırları — çözüm değil inceleme çerçevesi

- Uygunluk/verme alanı hangi bağlamda kime katılım hakkı verildiğini ele alır; tercih öğrenmemesi hedeflenir.
- Tercih alım alanı bağlam geçerliliği ve tekrar kullanımı denetlemeyi araştırır; gerçek kimliği öğrenmemesi hedeflenir.
- Toplulaştırma/yayın alanı bütünlük ve ifşa politikasını uygular; ham tercihler kamusal denetim adına açılmaz.
- Bağımsız inceleme alanı kimlik-tercih bağı yaratmadan yeterli kanıtı doğrulamayı araştırır.

Ayrı servisler aynı işletmeci ve gözlem altyapısını paylaşıyorsa bu ayrım mahremiyet sağlamayabilir. Analitik, hata izleme, IP kayıtları ve yedekler de mimarinin parçasıdır.

## Seçim öncesi zorunlu değerlendirme

1. Saldırganların birleşimi ve her bileşenin görebildiği veriler yazılır; [tehdit kaydı](THREAT-MODEL.md) eşleştirilir.
2. Verme/kullanma, iptal, kurtarma, tekrar önleme, eşzamanlılık ve tur sınırı tanımlanır.
3. Küçük grup politikası, veri saklama/silme ve ihlal sonrası geçmiş bilgi riski gösterilir.
4. Seçilen kitaplık/sürüm için bakım, güvenlik incelemesi, güncel saldırılar ve yeniden üretilebilir testler değerlendirilir. Bu belgedeki kaynak listesi kitaplık onayı değildir.
5. Gecikme, maliyet, erişilebilirlik, operasyon yükü ve başarısızlık yolları ölçülür.
6. Seçim gerekçesi ve reddedilen alternatifler Architecture Decision Record (mimari karar kaydı) taslağına yazılır; bağımsız uzman incelemesi ve proje sahibinin açık onayı olmadan kabul edilmiş sayılmaz.

**Differential privacy (diferansiyel mahremiyet)** yalnız toplu çıktı katmanı için ayrıca araştırılabilir. Bütçe, tekrar yayınların birleşik etkisi ve yararlılık kaybı belirtilmeden “gürültü ekledik” güvence değildir; kimlik doğrulama veya ağ anonimliği yerine geçmez.

## English summary

No architecture has been selected. Blind signatures, anonymous credentials, mixnets and practical privacy address different layers and assumptions; combining them does not automatically compose their guarantees. Global human uniqueness, privacy and Sybil resistance remain an unresolved joint problem. A metaphor is not a protocol specification.
