# Komite — Araştırma

Amaç, çözüldüğü varsayılan iddiaları çoğaltmak değil, açık soruları sınanabilir hale getirmektir. Henüz Komite’ye özgü güvenlik ispatı, bağımsız kriptografik denetim veya gerçek katılımcı deneyi yoktur.

## Birincil kaynaklar

Aşağıdaki kaynaklar 2026-09-03 tarihinde başlangıç taraması için incelendi. Kapsamlı veya güncel güvenlik durumunu tüketen bir literatür taraması değildir. Protokol seçimi öncesi güncel analizler, düzeltmeler ve uygulama denetimleri ayrıca kontrol edilmelidir.

| Ref | Kaynak | Bu araştırmaya katkısı / sınırı |
| --- | --- | --- |
| R1 | Denis, Jacobs, Wood, [RFC 9474: RSA Blind Signatures](https://www.rfc-editor.org/rfc/rfc9474.html), 2023 | Kör imza protokolü ve güvenlik hususları; bilgilendirici CFRG yayınıdır, Komite sistem güvenliği veya insan tekilliği kanıtı değildir |
| R2 | Sonnino ve diğerleri, [Coconut: Threshold Issuance Selective Disclosure Credentials](https://arxiv.org/abs/1802.07344), 2018 ön baskı / NDSS 2019 | Eşikli belge üretimi, seçici açıklama ve bağlantısız sunum araştırması; seçilmiş uygulama veya güncel güvenlik onayı değildir |
| R3 | Piotrowska ve diğerleri, [The Loopix Anonymity System](https://www.usenix.org/conference/usenixsecurity17/technical-sessions/presentation/piotrowska), USENIX Security 2017 | Karıştırma ve örtü trafiğiyle ağ mahremiyeti araştırması; uygunluk ve gerçek insan tekilliği çözümü değildir |
| R4 | NIST, [SP 800-188: De-Identifying Government Datasets: Techniques and Governance](https://csrc.nist.gov/pubs/sp/800/188/final), 2023 | Veri ifşa riskini teknik ve yönetişim birlikte ele alır; anonimlik sertifikası değildir |

[Mimari karşılaştırma](docs/ARCHITECTURE-DIRECTIONS.md) bu kaynaklardan hareketle proje için yapılmış değerlendirmedir; kaynak yazarlarının Komite hakkındaki görüşü değildir.

## Araştırma soruları ve deney kapıları

| Soru | İlk güvenli çalışma | Başarı için gereken kanıt |
| --- | --- | --- |
| Uygunluk ile insan tekilliği nasıl ayrılır? | Sentetik kimlik/davet, devir, iptal ve kurtarma senaryoları | Tanımlı bağlamda yanlış kabul/ret ve tekrar katılım ölçümü; küresel tekillik iddiası olmadan sınır açıklaması |
| Verme ile tercih ne ölçüde bağlanabilir? | Birleşik log, zaman, öznitelik ve kötü niyetli işletmeci modeli | Saldırgan yeteneklerine göre analiz; başarısız ve başarılı saldırıların raporu |
| Küçük grupta hangi sonuç güvenle açıklanabilir? | Oybirliği, tek hücre, kesişim, dış bilgi, tamamlayıcı toplam ve ardışık sorgu verileri | Gerekçeli yayın/bastırma politikası; yararlılık kaybı ve kalan risk; sihirli eşik yok |
| Anlama kontrolü görüşü yönlendirir mi? | Karşıt çerçeveli soru ve kaynak incelemesi | Tarafsızlık iddiasının sınırları; katılımı/tercih ağırlığını değiştirmeyen akış |
| Örneklem kimi dışarıda bırakır? | Davet ve yanıt vermeme senaryoları | Temsil iddiasının desteklenmesi veya çıkarılması; kapsanmayan grupların açıklanması |
| Bütünlük ile mahremiyet birlikte nasıl denetlenir? | Sahte, silinmiş, tekrar ve geç bildirimlerle sentetik tur | Yeniden üretilebilir tespit kanıtı; bireysel tercihi açmayan denetim sınırı |
| Baskı ve ele geçirilmiş cihaz karşısında ne korunamaz? | Masa başı saldırı analizi | Açık korunmama sınırları; yüksek riskli bağlamların dışlanması |

İlk çalışmalar sentetik veriyle sınırlıdır. Gerçek insan araştırması ayrıca etik, gönüllülük, veri koruma ve güvenlik incelemesine tabidir; bu belge deney katılımcısı toplama izni değildir.

## Kanıt sınıfları

- `source_verified`: belirtilen kaynak gerçekten incelendi; sistem iddiasını otomatik doğrulamaz.
- `knowledge_base_verified`: kayıt ve sürüm tutarlılığı doğrulandı; deney veya ispat yerine geçmez.
- `attestation_only`: yazarın/incelemecinin beyanı var, bağımsız yeniden üretim yok.
- `insufficient_evidence`: iddia için yeterli kanıt yok; açık soru olarak kalır.

Mevcut teknik hedeflerin uygulama düzeyindeki durumu `insufficient_evidence`dır. Kaynak taraması sonuçları ile protokol garantileri ayrı tutulur.

## Katkı biçimi

Araştırma önerisi şu bilgileri içermelidir: soru; kaynak ve sürüm; saldırgan/güven varsayımı; yöntem; sentetik veri üretimi; başarı ve başarısızlık ölçütü; bulgular; sınırlamalar; tekrar üretim yolu; ilgili tehdit ID’leri. Olumsuz sonuçlar da değerlidir. Yalnız “anonim”, “güvenli” veya “merkeziyetsiz” etiketi kanıt sayılmaz.

Kamusal araştırma, kimlik/tercih eşleştirmeleri veya sömürülebilir açık ayrıntıları içermemelidir. Güvenlik bildirimi için [GUVENLIK.md](GUVENLIK.md); katkı için [KATKI.md](KATKI.md).

## English summary

The cited primary sources guide research; they do not validate Komite. Initial work uses synthetic data. Each claim needs explicit assumptions, reproducible evidence and limitations. No protocol, anonymity guarantee or joint global-uniqueness/privacy/Sybil-resistance solution has been established.
