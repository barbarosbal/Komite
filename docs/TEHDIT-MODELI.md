# Komite — Tehdit Modeli

Durum: başlangıç araştırma modeli. Aşağıdaki önlemler uygulanmış kontrol veya kabul edilmiş kalan risk değildir. Gerçek kullanım [Yayın Kontrol Listesi](YAYIN-KONTROL-LISTESI.md) kapılarına bağlıdır.

### EN · Threat model

Status: initial research model. The controls below are not implemented safeguards and the remaining risks are not accepted production risks. Real-world use is gated by the [Release Checklist](YAYIN-KONTROL-LISTESI.md).

## Korunacak varlıklar ve saldırganlar

Korunacak varlıklar: kimlik/uygunluk bilgisi, katılım olgusu, bireysel tercih, anlama yanıtı, davet yetkisi, soru sürümü, sonuç bütünlüğü ve özgür katılım. Katılmış olmak bile hassas olabilir.

Anlama yanıtı yalnız içerik kalitesi verisi değildir. Nadir cevap örüntüsü, zamanlama, tekrar deneme sayısı veya küçük bir rolle birleştiğinde kimlik ya da tercih çıkarımına yardım edebilir.

Saldırganlar: dış ağ gözlemcisi, kötü niyetli katılımcı, davet sahibi, karar sahibi/işveren, kötü niyetli veya ele geçirilmiş işletmeci, birlikte hareket eden servisler, saldırgan istemci ve tedarik zinciri.

Ayrı servis veya veri tabanı kullanmak tek başına bağımsız güven alanı kurmaz.

### EN · Assets and attackers

Protected assets include identity/eligibility information, the fact of participation, individual preferences, understanding-check responses, invitation authority, question version, result integrity, and free participation. Participation itself can be sensitive.

Understanding-check data is not merely content-quality data. Rare response patterns, timing, retry counts, or role information can contribute to identity or preference inference.

Attackers include external network observers, malicious participants, invitation holders, decision owners/employers, malicious or compromised operators, colluding services, compromised clients, and supply-chain attackers.

Separate services or databases do not automatically create independent trust domains.

## Tehdit kaydı

Öncelikler [Güvenlik](../GUVENLIK.md) ölçeğindedir. Bu tablo gelecekteki kullanım için doğal riski gösterir; mevcut bir uygulamada doğrulanmış açık listesi değildir. Her satırın durumu **açık**tır.

| İz / öncelik | Tehdit | Araştırılacak kontrol | Kalan risk / durdurma koşulu |
| --- | --- | --- | --- |
| T01 · Yüksek | Anlama üzerinden yönlendirme | Karşı görüş incelemesi, soru sürümleme, yanlış yanıtın katılımı/ağırlığı değiştirmediğini test | Tarafsızlık salt test puanıyla kanıtlanamaz; yönlendirme bulgusunda tur durur |
| T02 · Yüksek | Küçük grupta kimliği çıkarma | Küçük hücre/tamamlayıcı toplam bastırma, dış bilgi, kesişim ve tekrar yayın saldırıları | Sabit eşik tek başına garanti değildir; risk değerlendirmesi yoksa sonuç yok |
| T03 · Yüksek | Üstveri ve zamanlama ilişkilendirmesi | Veri minimizasyonu, gecikme/toplu iletim/örtü trafiği deneyleri, log birleştirme testi | Küresel gözlemci ve düşük trafik korunmuş varsayılmaz |
| T04 · Yüksek | İşletmecilerin birlikte hareket etmesi | Yetki ayrımı, eşikli güven modelleri, birleşik veri erişimiyle saldırı deneyi | Aynı yönetici/bulut/yedek ayrımı aşabilir |
| T05 · Yüksek | Baskı ve oy satın alma | Gönüllülük analizi, tercih kanıtı üretmeyen akış araştırması | Anonimlik baskıyı çözmez; denetlenen cihaz güvenli değildir |
| T06 · Yüksek | İstemcinin ele geçirilmesi | Kaynak/bağımlılık bütünlüğü, asgari istemci, doğrulanabilir dağıtım araştırması | Sunucu kriptografisi ele geçirilmiş cihazı düzeltmez |
| T07 · Yüksek | Davet suistimali ve çoklu katılım | Bağlam/süre sınırı, atomik tek kullanım, tekrar/eşzamanlılık testi | Davet veya hesap tekil insan kanıtı değildir |
| T08 · Yüksek | Örnekleme yanlılığı ve seçici dışlama | Yöntemi önceden açıklama, kapsam/yanıt vermeme raporu | Kriptografi temsiliyet sağlamaz |
| T09 · Yüksek | Sonuç manipülasyonu | Tur/sürüm bağlama, atomik kabul, bağımsız yeniden hesaplama, hata enjeksiyonu | Bütünlük belirsizse sonuç yayımlanmaz |
| T10 · Yüksek | İhlal sonrası bağlantı | Veri yaşam döngüsü, silme/yedek süresi, anahtar döndürme, geçmiş korelasyon deneyi | Silme beyanı veya diskte şifreleme geçmiş bağlantısızlık kanıtı değildir |
| T11 · Orta | Erişilebilirlik saldırısı ve seçici engelleme | Kapasite, kesinti/yeniden deneme, uzatma/iptal kuralları | Eksik katılım sonucu çarpıtabilir |
| T12 · Yüksek | Öznitelik ve sunum bağlantısı | Asgari öznitelik, turla sınırlı bağlantı, turlar arası eşleştirme testi | Kriptografik bağlantısızlık açıklanan bilginin ayırt ediciliğini çözmez |

### EN · Threat register

The priorities use the [Security](../GUVENLIK.md) scale. These are open design risks, not a verified vulnerability list in an implemented product.

| ID / priority | Threat | Research direction | Remaining risk / stop condition |
| --- | --- | --- | --- |
| T01 · High | Framing/priming through understanding checks | Opposing-view review, question versioning, test that wrong answers do not affect participation/weight | Neutrality cannot be proven by a score alone; stop on steering evidence |
| T02 · High | Small-group re-identification | Small-cell/complementary suppression, external-information, intersection, repeated-release attacks | A fixed threshold is not a guarantee; no risk assessment means no result |
| T03 · High | Metadata/timing correlation | Data minimization, batching/delay/cover-traffic experiments, combined-log tests | Global observers and low-traffic settings are not assumed protected |
| T04 · High | Operator collusion | Separation of authority, threshold trust, attacks using combined access | Shared admin/cloud/backup can defeat separation |
| T05 · High | Coercion and vote buying | Voluntariness analysis, research into non-receipt-like flows | Anonymity does not solve coercion; monitored devices remain unsafe |
| T06 · High | Compromised client | Source/dependency integrity, minimal client, verifiable-distribution research | Server cryptography does not repair a compromised endpoint |
| T07 · High | Invitation abuse / multiple participation | Context/time limits, atomic single use, replay/concurrency testing | Invitation/account is not proof of unique humanity |
| T08 · High | Sampling bias / selective exclusion | Predeclared method, coverage and non-response reporting | Cryptography does not create representativeness |
| T09 · High | Result manipulation | Round/version binding, atomic acceptance, independent recomputation, fault injection | No result if integrity is uncertain |
| T10 · High | Post-breach linkage | Data lifecycle, backup/deletion periods, key rotation, historical-correlation tests | Deletion claims or encryption at rest do not prove historical unlinkability |
| T11 · Medium | Availability/selective blocking | Capacity, outage/retry tests, extension/cancellation rules | Missing participation can distort results |
| T12 · High | Attribute/presentation linkage | Minimal attributes, round-limited links, cross-round matching tests | Cryptographic unlinkability does not remove identifying attributes |

## Küçük grup ifşa politikası

Küçük gruplar uç durum değildir. Minimum kohort, küçük hücre bastırma, tamamlayıcı bastırma, kesişen gruplar, tekrar sorgular ve farklı zamanlarda raporlanan toplamlar birlikte tasarlanmalıdır. Oybirliği ve dış bilgi riski de incelenir. Anlama kontrolü ve katılım sayıları muaf değildir.

Kesin eşik, sorgu bütçesi ve zaman penceresi henüz onaylanmadı. Güvenli varsayılan **güvenli kapanma**dır: onaylı politika yoksa veya risk ölçülemiyorsa sonuç yok.

Tercih toplamları, anlama yanıtları/puanları, katılım ve yanıt vermeme sayıları, hata/iptal bilgisi, alt grup kırılımları ve farklı zamanlardaki raporlar tek bir birleşik yayın yüzeyi olarak değerlendirilir.

### EN · Small-group disclosure policy

Small groups are not edge cases. Minimum cohort size, small-cell suppression, complementary suppression, overlapping groups, repeated queries, and totals published at different times must be designed together. Unanimity and external-information risks also matter. Understanding-check and participation counts are not exempt.

No exact threshold, query budget, or time window has been approved. The safe default is **fail closed**: if there is no approved policy or the risk cannot be measured, publish no result.

Preference totals, understanding responses/scores, participation/non-response counts, error/cancellation information, subgroup breakdowns, and reports across time are treated as one combined disclosure surface.

## Test kanıtının sınırı

Her deney saldırgan görünürlüğünü, veri boyutunu, kohort yapısını, başarı ölçütünü, başarısız örnekleri, sürümü ve yeniden çalıştırma yolunu kaydetmelidir. Sentetik veride başarısız saldırı denemesi gerçek dünyada anonimliği kanıtlamaz.

Her aday mimari, ilgili kontrol sahibini, test bağlantısını ve kabul edilmemiş kalan riskleri açıkça göstermeden değerlendirmeden çıkamaz.

### EN · Limits of test evidence

Every experiment must record attacker visibility, data size, cohort structure, success criteria, failed examples, version, and reproduction path. A failed attack against synthetic data does not prove real-world anonymity.

No architecture candidate should leave evaluation without explicit control ownership, linked tests, and unaccepted remaining risks.