# Komite — Mimari Araştırma Yönleri

Durum: alternatif değerlendirmesi. Seçilmiş mimari, uygulanmış protokol veya güvenlik garantisi yoktur. Metaforlar teknik garanti değildir.

### EN · Architecture research directions

Status: alternative evaluation. No architecture has been selected, no protocol has been implemented, and no security guarantee exists. Metaphors are not technical guarantees.

## Ayrılması gereken problemler

İnsan olma, küresel tekillik, bağlamsal uygunluk, tur başına tek katılım, kimlik-tercih bağlantısızlığı, ağ mahremiyeti, sayım bütünlüğü ve güvenli sonuç ifşası ayrı problemlerdir. Birinin çözümü diğerini otomatik çözmez.

**Küresel tekil insan doğrulaması + mahremiyet + sahte/çoklu kimlikle katılıma dayanıklılık birlikte çözülmüş kabul edilmez.**

### EN · Problems that must remain separate

Human verification, global uniqueness, contextual eligibility, one participation per round, identity-preference unlinkability, network privacy, counting integrity, and safe result disclosure are separate problems. Solving one does not automatically solve the others.

**Global unique-human verification + privacy + Sybil resistance are not considered jointly solved.**

## Karşılaştırma

Bu tablo Komite için araştırma değerlendirmesidir; kaynakların Komite’yi doğruladığı anlamına gelmez. Kaynak künyeleri [Araştırma](../ARASTIRMA.md) belgesindedir.

| Yön | Araştırılan katkı | Güven varsayımı / maliyet | Tek başına çözmediği alan | Sonraki deney |
| --- | --- | --- | --- | --- |
| Kör imzalar, R1 | Yetkilendirme ile kullanım arasındaki bağlantıyı azaltma | Doğru uygulama, anahtar dağıtımı, güvenilir uygunluk/verme politikası | Küresel tekillik, token devri, ağ korelasyonu, küçük grup ifşası | Sahte/tekrar/eşzamanlı kullanım ve birleşik log saldırıları |
| Anonim yetki belgeleri, R2 | Seçici açıklama ve bağlantısız sunum | İhraççı modeli, ispat uygulaması, iptal/kurtarma, öznitelik mahremiyeti | Gerçek insan kaydı, nadir öznitelik, baskı, turda tek yanıt | Turla sınırlı tekrar önleme + turlar arası bağlantısızlık |
| Karıştırma ağları, R3 | İleti giriş/çıkış eşleştirmesini zorlaştırma | Dürüst düğüm varsayımı, gecikme, bant genişliği, örtü trafiği | Uygunluk, tekillik, ele geçirilmiş uç cihaz, rapor çıkarımı | Küçük/düşük trafikli gruplarda korelasyon deneyi |
| Uygulanabilir mahremiyet, R4 | Asgari veri, erişim ayrımı, kısa saklama, toplulaştırma ve ifşa kontrolü | İşletmeci disiplini, veri envanteri, yararlılık/mahremiyet ödünleşimi | Kriptografik bağlantısızlık ve güçlü gözlemciye genel güvence | Log/yedek envanteri ve tekrar yayın saldırıları |

Bu yönler aynı katmandaki rakip ürünler değildir. Bazıları birlikte değerlendirilebilir; birleşmeleri güvenlik özelliklerini otomatik olarak toplamaz.

### EN · Comparison

This table is Komite's own research assessment and does not imply endorsement by the cited sources. Bibliographic details are in [Research](../ARASTIRMA.md).

- **Blind signatures (R1):** may reduce linkage between authorization and use; do not solve global uniqueness, token transfer, network correlation, or small-group disclosure.
- **Anonymous credentials (R2):** may support selective disclosure and unlinkable presentation; do not solve real-human enrollment, rare-attribute identification, coercion, or one-response-per-round by themselves.
- **Mixnets (R3):** may make input/output correlation harder; do not solve eligibility, uniqueness, compromised endpoints, or inference from published results.
- **Practical privacy (R4):** focuses on data minimization, access separation, short retention, aggregation, and disclosure control; does not itself provide cryptographic unlinkability or protection from powerful colluding observers.

These are not interchangeable products at the same layer. Combining them does not automatically compose their guarantees.

## Aday sistem sınırları

- Uygunluk/verme alanı kime hangi bağlamda katılım hakkı verildiğini ele alır; tercihi öğrenmemesi hedeflenir.
- Tercih alım alanı bağlam geçerliliği ve tekrar kullanımı denetlemeyi araştırır; gerçek kimliği öğrenmemesi hedeflenir.
- Toplulaştırma/yayın alanı bütünlük ve ifşa politikasını uygular; ham tercihler kamusal denetim adına açılmaz.
- Bağımsız inceleme alanı kimlik-tercih bağı yaratmadan yeterli kanıtı doğrulamayı araştırır.

Ayrı servisler aynı işletmeci, analitik, log, IP kaydı veya yedek altyapısını paylaşıyorsa bu ayrım mahremiyet sağlamayabilir.

### EN · Candidate system boundaries

- The eligibility/issuance domain decides who may participate in a context and should aim not to learn preferences.
- The preference-receipt domain explores context validity and replay prevention and should aim not to learn real identity.
- The aggregation/publication domain applies integrity and disclosure policy; raw preferences are not exposed for public audit.
- The independent-review domain explores how to verify sufficient evidence without recreating identity-preference links.

Separate services do not create privacy by themselves if they share operators, analytics, logs, IP records, or backups.

## Seçim öncesi zorunlu değerlendirme

1. Saldırganların birleşimi ve her bileşenin görebildiği veriler yazılır; [Tehdit Modeli](TEHDIT-MODELI.md) eşleştirilir.
2. Verme/kullanma, iptal, kurtarma, tekrar önleme, eşzamanlılık ve tur sınırı tanımlanır.
3. Küçük grup politikası, veri saklama/silme ve ihlal sonrası geçmiş bilgi riski gösterilir.
4. Seçilen kitaplık/sürüm için bakım, güvenlik incelemesi, güncel saldırılar ve yeniden üretilebilir testler değerlendirilir.
5. Gecikme, maliyet, erişilebilirlik, operasyon yükü ve başarısızlık yolları ölçülür.
6. Seçim gerekçesi ve reddedilen alternatifler kaydedilir; bağımsız uzman incelemesi ve proje sahibinin açık onayı olmadan kabul edilmiş sayılmaz.

Diferansiyel mahremiyet toplu çıktı katmanı için ayrıca araştırılabilir; kimlik doğrulama veya ağ anonimliği yerine geçmez.

### EN · Required evaluation before selection

1. Write down combined attacker capabilities and the data visible to each component; map them to the [Threat Model](TEHDIT-MODELI.md).
2. Define issuance/use, revocation, recovery, replay prevention, concurrency, and round boundaries.
3. Show the small-group policy, retention/deletion rules, and post-breach historical-information risk.
4. Evaluate maintenance status, security review, current attacks, and reproducible tests for the selected library/version.
5. Measure latency, cost, accessibility, operational burden, and failure modes.
6. Record the selection reasoning and rejected alternatives; do not treat the choice as accepted without independent expert review and explicit project-owner approval.

Differential privacy may be researched for aggregate outputs, but it does not replace identity verification or network anonymity.