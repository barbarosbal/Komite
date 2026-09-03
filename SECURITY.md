# Komite — Güvenlik

## Desteklenen durum

Depo araştırma ve tasarım aşamasındadır. Desteklenen üretim sürümü, çalışan hizmet, doğrulanmış anonimlik veya güvenlik garantisi yoktur. Belgeler gerçek katılımcı verisiyle kullanıma izin veren bir sertifika değildir. Araştırma hedefleri için [tehdit modeli](docs/THREAT-MODEL.md) ve [yayın kapıları](docs/RELEASE-CHECKLIST.md) geçerlidir.

## Özel bildirim

Şüpheli güvenlik açığını, ifşa riskini veya yanlış güvenlik iddiasını **herkese açık issue (iş kaydı) veya pull request (değişiklik önerisi)** üzerinden yayımlamayın.

İlk temas: [barbaroshbal@gmail.com](mailto:barbaroshbal@gmail.com). Konu önerisi: `Komite security report`.

İlk mesajda yalnız hassas olmayan kısa açıklama, etkilenen belge/sürüm, olası etki ve güvenli biçimde iletişim kurulabilecek adres yer alsın. Gerçek kimlik, tercih, erişim anahtarı, token (belirteç) veya sömürülebilir ayrıntı göndermeyin. E-postanın uçtan uca şifreli olduğu varsayılmamalıdır; ayrıntıların güvenli aktarım yöntemi ayrıca kararlaştırılır. Yayınlanmış şifreleme anahtarı veya kesintisiz güvenlik ekibi vaat edilmez.

Şu anda taahhüt edilmiş bir yanıt süresi veya hizmet seviyesi yoktur. Yanıt gelmezse aynı adrese hassas veri eklemeden hatırlatma gönderilebilir. LinkedIn özel güvenlik kanıtı aktarım kanalı değildir.

## Değerlendirme ve açıklama

1. Proje sahibi bildirimi alır ve mümkünse güvenli iletişimi kurar.
2. Etki, etkilenen sürüm, yeniden üretim ve geçici sınırlandırma değerlendirilir. Gerçek veriyi kopyalamak yerine sentetik örnek tercih edilir.
3. Düzeltme ve kontrol kanıtları incelenir. Kritik/yüksek bulgu, yalnız AI (yapay zekâ) incelemesiyle kapatılamaz; yetkili insanın açık onayı gerekir.
4. Bildiriciyle koordineli olarak, kişisel veri ve saldırıyı kolaylaştıracak gereksiz ayrıntılar ayıklanmış açıklama hazırlanır. Otomatik açıklama tarihi veya ödül taahhüdü yoktur.

## İnceleme seviyeleri

| Seviye | Anlam | Yayın davranışı |
| --- | --- | --- |
| BLOCKER (engelleyici) | Kapsam ihlali, gizli veri ifşası, kanıtsız üretim/anonimlik garantisi gibi yayını doğrudan durduran sorun | Çözülmeden birleştirme yok |
| HIGH (yüksek) | Mahremiyeti, bütünlüğü veya katılımcı güvenliğini ciddi etkileyen açık/eksik güven sınırı | Düzeltme ve gereken insan onayı olmadan birleştirme yok |
| MEDIUM (orta) | Yanlış uygulamaya/yoruma yol açabilecek önemli belirsizlik veya eksik süreç | Bu temel yayınında düzeltilmeden birleştirme yok |
| LOW (düşük) | Anlamı temelden değiştirmeyen bağlantı, ifade veya sunum kusuru | Bu temel yayınında düzeltilmeden birleştirme yok |

Tasarımın açık araştırma tehditleri ile bu belgelerdeki yayın kusurları ayrı kayıtlardır. Bir belgenin temiz olması, tarif ettiği sistem risklerinin çözüldüğü anlamına gelmez.

## Güvenli araştırma sınırı

Yalnız kendi yerel/sentetik ortamınızda çalışın. Bu politika üçüncü taraflara saldırı, gerçek kişileri yeniden tanımlama, kimlik verisi toplama, sosyal mühendislik veya hizmet engelleme izni vermez. Gizli bilgiyi yanlışlıkla bulursanız yaymayın, incelemeyi genişletmeyin ve özel bildirim kanalını kullanın.

## English summary

There is no supported production release or proven anonymity guarantee. Report concerns privately to barbaroshbal@gmail.com; send only a non-sensitive summary initially. Email is not assumed end-to-end encrypted. Critical/high findings require explicit human approval for closure. Documentation publication is not approval for real-user deployment or security-risk acceptance.
