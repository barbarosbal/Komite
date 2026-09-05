# Komite — Araştırma

Amaç, çözüldüğü varsayılan iddiaları çoğaltmak değil, açık soruları sınanabilir hale getirmektir. Henüz Komite’ye özgü güvenlik ispatı, bağımsız kriptografik denetim veya gerçek katılımcı deneyi yoktur.

### EN · Research

The goal is not to multiply claims that are assumed to be solved, but to turn open questions into testable ones. There is currently no Komite-specific security proof, independent cryptographic audit, or real-participant experiment.

## Birincil kaynaklar

Aşağıdaki kaynaklar 2026-09-03 tarihinde başlangıç taraması için incelendi. Bu kapsamlı veya güncel güvenlik durumunu tüketen bir literatür taraması değildir. Protokol seçimi öncesi güncel analizler, düzeltmeler ve uygulama denetimleri ayrıca kontrol edilmelidir.

| Kaynak | İz | Bu araştırmaya katkısı / sınırı |
| --- | --- | --- |
| Denis, Jacobs, Wood, [RFC 9474: RSA Blind Signatures](https://www.rfc-editor.org/rfc/rfc9474.html), 2023 | R1 | Kör imza protokolü ve güvenlik hususları; Komite sistem güvenliği veya insan tekilliği kanıtı değildir |
| Sonnino ve diğerleri, [Coconut: Threshold Issuance Selective Disclosure Credentials](https://arxiv.org/abs/1802.07344), 2018 ön baskı / NDSS 2019 | R2 | Eşikli belge üretimi, seçici açıklama ve bağlantısız sunum araştırması; seçilmiş uygulama veya güncel güvenlik onayı değildir |
| Piotrowska ve diğerleri, [The Loopix Anonymity System](https://www.usenix.org/conference/usenixsecurity17/technical-sessions/presentation/piotrowska), USENIX Security 2017 | R3 | Karıştırma ve örtü trafiğiyle ağ mahremiyeti araştırması; uygunluk ve insan tekilliği çözümü değildir |
| NIST, [SP 800-188: De-Identifying Government Datasets: Techniques and Governance](https://csrc.nist.gov/pubs/sp/800/188/final), 2023 | R4 | Veri ifşa riskini teknik ve yönetişim birlikte ele alır; anonimlik sertifikası değildir |

[Mimari karşılaştırma](docs/MIMARI-YONLER.md) bu kaynaklardan hareketle proje için yapılmış değerlendirmedir; kaynak yazarlarının Komite hakkındaki görüşü değildir.

### EN · Primary sources

The sources above were reviewed as an initial scan on 2026-09-03. This is not a comprehensive or continuously current literature review. Current analyses, corrections, implementation details, and audits must be checked before any protocol choice. The [architecture comparison](docs/MIMARI-YONLER.md) is Komite's own research assessment; it is not an endorsement by the cited authors.

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
| Farklı perspektifler karar sahibinin görüş alanını gerçekten genişletiyor mu? | Önceden kaydedilmiş yöntemlerle karşılaştırmalı sentetik çalışma; gerçek insan çalışması ancak ayrı etik/gönüllülük incelemesiyle | “Daha iyi görme”, “sinyal kalitesi” ve “karar faydası” için önceden tanımlı ölçüler; alternatif açıklamalar ve olumsuz sonuçlar dahil rapor |

İlk çalışmalar sentetik veriyle sınırlıdır. Gerçek insan araştırması ayrıca etik, gönüllülük, veri koruma ve güvenlik incelemesine tabidir.

### EN · Research questions and experiment gates

Core research questions include separating eligibility from human uniqueness; testing linkage between issuance and preference; safe disclosure in small groups; framing effects of understanding checks; sampling bias; joint integrity/privacy verification; limits under coercion or compromised devices; and whether additional perspectives actually widen the decision-maker's field of view. Initial work is limited to synthetic data. Any real-human research requires separate ethics, voluntariness, data-protection, and security review.

## Kanıt sınıfları

- `source_verified`: belirtilen kaynak gerçekten incelendi; sistem iddiasını otomatik doğrulamaz.
- `knowledge_base_verified`: kayıt ve sürüm tutarlılığı doğrulandı; deney veya ispat yerine geçmez.
- `attestation_only`: yazarın/incelemecinin beyanı var, bağımsız yeniden üretim yok.
- `insufficient_evidence`: iddia için yeterli kanıt yok; açık soru olarak kalır.

Mevcut teknik hedeflerin uygulama düzeyindeki durumu `insufficient_evidence`dır.

“İnsanlar daha güvenli hissederse daha dürüst konuşur”, “daha fazla perspektif daha iyi görmeyi sağlar” ve “bu sinyal daha iyi karara yardım eder” ifadeleri **hipotezdir**. Bunlar güvenlik veya kriptografik garanti değildir.

### EN · Evidence classes

- `source_verified`: the cited source was actually reviewed; this does not validate a system claim.
- `knowledge_base_verified`: record/version consistency was checked; this is not an experiment or proof.
- `attestation_only`: there is an author/reviewer assertion without independent reproduction.
- `insufficient_evidence`: evidence is insufficient and the claim remains open.

Current implementation-level technical targets are `insufficient_evidence`. Statements such as “safer conditions make people more honest,” “more perspectives improve visibility,” or “this signal improves decisions” are **hypotheses**, not security or cryptographic guarantees.

## Katkı biçimi

Araştırma önerisi şu bilgileri içermelidir: soru; kaynak ve sürüm; saldırgan/güven varsayımı; yöntem; sentetik veri üretimi; başarı ve başarısızlık ölçütü; bulgular; sınırlamalar; tekrar üretim yolu; ilgili tehdit ID’leri. Olumsuz sonuçlar da değerlidir.

Kamusal araştırma, kimlik/tercih eşleştirmeleri veya sömürülebilir açık ayrıntıları içermemelidir. Güvenlik bildirimi için [GUVENLIK.md](GUVENLIK.md); katkı için [KATKI.md](KATKI.md).

### EN · Contribution format

A research proposal should include the question; source and version; attacker/trust assumptions; method; synthetic-data generation; success and failure criteria; findings; limitations; reproduction path; and relevant threat IDs. Negative results are valuable.

Public research must not contain identity/preference mappings or exploitable vulnerability details. Use [Security](GUVENLIK.md) for sensitive reports and [Contributing](KATKI.md) for general contributions.