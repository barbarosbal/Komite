# Komite — Güvenlik

## Desteklenen durum

Depo araştırma ve tasarım aşamasındadır. Desteklenen üretim sürümü, çalışan hizmet, doğrulanmış anonimlik veya güvenlik garantisi yoktur. Belgeler gerçek katılımcı verisiyle kullanıma izin veren bir sertifika değildir.

Araştırma hedefleri için [Tehdit Modeli](docs/TEHDIT-MODELI.md) ve [Yayın Kontrol Listesi](docs/YAYIN-KONTROL-LISTESI.md) geçerlidir.

### EN · Supported status

The repository is in research and design. There is no supported production release, running service, proven anonymity, or security guarantee. The documents are not certification for use with real participant data.

See the [Threat Model](docs/TEHDIT-MODELI.md) and [Release Checklist](docs/YAYIN-KONTROL-LISTESI.md) for research boundaries.

## Özel bildirim

Şüpheli güvenlik açığını, ifşa riskini veya sömürülebilir güvenlik/mahremiyet ayrıntısını herkese açık issue veya PR içinde yayımlamayın.

İlk temas: [barbaroshbal@gmail.com](mailto:barbaroshbal@gmail.com)  
Konu önerisi: `Komite security report`

İlk mesajda yalnız hassas olmayan kısa açıklama, etkilenen belge/sürüm, olası etki ve güvenli iletişim adresi yer alsın. Gerçek kimlik, tercih, erişim anahtarı, token veya sömürülebilir ayrıntı göndermeyin. E-postanın uçtan uca şifreli olduğu varsayılmamalıdır.

Şu anda taahhüt edilmiş yanıt süresi veya hizmet seviyesi yoktur. LinkedIn hassas güvenlik kanıtı aktarım kanalı değildir.

Yazım hatası, kırık bağlantı veya sömürü ayrıntısı içermeyen kamusal belge tutarsızlıkları [Katkı Rehberi](KATKI.md) üzerinden normal PR ile düzeltilebilir. Emin değilseniz önce özel kanalda hassas olmayan özet gönderin.

### EN · Private reporting

Do not publish suspected vulnerabilities, disclosure risks, or exploitable security/privacy details in a public issue or PR.

First contact: [barbaroshbal@gmail.com](mailto:barbaroshbal@gmail.com)  
Suggested subject: `Komite security report`

The first message should contain only a non-sensitive summary, affected document/version, possible impact, and a safe contact address. Do not send real identity data, preferences, access keys, tokens, or exploitable details. Email is not assumed to be end-to-end encrypted.

There is currently no committed response time or service level. LinkedIn is not a channel for transmitting sensitive security evidence.

Typos, broken links, and public documentation inconsistencies that do not include exploit details may be fixed through the normal [Contributing](KATKI.md) process. If uncertain, send a non-sensitive summary privately first.

## Değerlendirme ve açıklama

1. Proje sahibi bildirimi alır ve mümkünse güvenli iletişimi kurar.
2. Etki, etkilenen sürüm, yeniden üretim ve geçici sınırlandırma değerlendirilir; gerçek veri yerine sentetik örnek tercih edilir.
3. Düzeltme ve kontrol kanıtları incelenir. Kritik/yüksek bulgu yalnız AI incelemesiyle kapatılamaz; yetkili insanın açık onayı gerekir.
4. Kamusal açıklama hazırlanacaksa kişisel veri ve saldırıyı kolaylaştıracak gereksiz ayrıntı ayıklanır.

### EN · Assessment and disclosure

1. The project owner receives the report and establishes safer communication where possible.
2. Impact, affected version, reproduction, and temporary mitigation are assessed; synthetic examples are preferred over real data.
3. Fixes and control evidence are reviewed. Critical/high findings cannot be closed by AI review alone; explicit authorized human approval is required.
4. If a public disclosure is prepared, personal data and unnecessary attack-enabling detail are removed.

## İnceleme seviyeleri

| Seviye | Anlam | Yayın davranışı |
| --- | --- | --- |
| Engelleyici | Kapsam ihlali, gizli veri ifşası, kanıtsız üretim/anonimlik garantisi gibi yayını durduran sorun | Çözülmeden birleştirme yok |
| Yüksek | Mahremiyet, bütünlük veya katılımcı güvenliğini ciddi etkileyen açık/eksik güven sınırı | Düzeltme ve gereken insan onayı olmadan birleştirme yok |
| Orta | Yanlış uygulama veya yoruma yol açabilecek önemli belirsizlik | Düzeltilmeden birleştirilmemeli |
| Düşük | Anlamı temelden değiştirmeyen bağlantı, ifade veya sunum kusuru | Birleştirme öncesi düzeltilmeli |

### EN · Review severity

| Level | Meaning | Publication behavior |
| --- | --- | --- |
| Blocker | Scope violation, secret-data disclosure, or unsupported production/anonymity guarantee | Do not merge until resolved |
| High | Serious privacy, integrity, or participant-safety boundary problem | Do not merge without a fix and required human approval |
| Medium | Important ambiguity that may cause misuse or misinterpretation | Should be fixed before merge |
| Low | Link, wording, or presentation defect that does not fundamentally change meaning | Should be fixed before merge |

Bir belgenin temiz olması tarif ettiği sistem risklerinin çözüldüğü anlamına gelmez.

A clean document does not mean the system risks it describes are solved.

## Güvenli araştırma sınırı

Yalnız kendi yerel veya sentetik ortamınızda çalışın. Bu politika üçüncü taraflara saldırı, gerçek kişileri yeniden tanımlama, kimlik verisi toplama, sosyal mühendislik veya hizmet engelleme izni vermez. Gizli bilgiyi yanlışlıkla bulursanız yaymayın, incelemeyi genişletmeyin ve özel bildirim kanalını kullanın.

### EN · Safe research boundary

Work only in your own local or synthetic environment. This policy does not authorize attacks on third parties, re-identification of real people, identity-data collection, social engineering, or denial of service. If you accidentally discover secret information, do not publish it or expand the investigation; use the private reporting channel.