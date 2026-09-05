# Komite — Yayın Kontrol Listesi

Bu belge bir tamamlanma beyanı değil, tekrar kullanılabilir yayın kapısıdır. Her yayın için gerçek kanıt, incelenen commit/değişiklik, inceleme türü ve sonuç ilgili PR veya değişiklik kaydında tutulur.

## A — Dokümantasyon yayını

- [ ] Değişiklik ayrı dalda hazırlandı; `main` üzerine doğrudan yazılmadı.
- [ ] README ve yönlendirdiği tüm public belgeler mevcut ve göreli bağlantılar çalışıyor.
- [ ] Proje adı her yerde **Komite** olarak tutarlı.
- [ ] Public belgelerde Türkçe bölümün hemen ardından İngilizce karşılığı bulunuyor veya açıkça belgelenmiş geçici istisna var.
- [ ] Apache-2.0 lisansı korunuyor; yeni kullanım kısıtı lisansa eklenmedi.
- [ ] Seçim, referandum ve bağlayıcı karar kapsam dışı sınırları korunuyor.
- [ ] Hedef, hipotez, açık problem ve kanıtlanmış bulgu birbirine karıştırılmıyor.
- [ ] Anonimlik, insan tekilliği, güvenlik, ölçek veya karar kalitesi kanıtlanmamışsa özellik gibi sunulmuyor.
- [ ] Metaforlar teknik garanti gibi sunulmuyor.
- [ ] Hassas veri, ham özel konuşma veya sömürülebilir güvenlik ayrıntısı yok.
- [ ] Değişiklik bütünüyle yeniden okundu; engelleyici/yüksek/orta/düşük bulgular kaydedildi ve düzeltmeler son sürümde doğrulandı.
- [ ] İnceleme türü doğru etiketlendi: öz-denetim, AI incelemesi veya bağımsız insan incelemesi.
- [ ] Birleştirme öncesi hedef dal ve PR başı yeniden doğrulandı.

### EN · Documentation release

- [ ] The change was prepared on a separate branch, not directly on `main`.
- [ ] README and all public documents it references exist and relative links work.
- [ ] The project name is consistently **Komite**.
- [ ] Public documents place the English counterpart immediately after each Turkish section, or a temporary exception is explicitly documented.
- [ ] Apache-2.0 is preserved and no new use restriction is added to the license.
- [ ] Election, referendum, and binding-decision exclusions remain intact.
- [ ] Targets, hypotheses, open problems, and proven findings are not conflated.
- [ ] Unproven anonymity, human uniqueness, security, scale, or decision-quality goals are not presented as capabilities.
- [ ] Metaphors are not presented as technical guarantees.
- [ ] No sensitive data, raw private conversations, or exploitable security details are published.
- [ ] The complete change was reread; blocker/high/medium/low findings were recorded and fixes were verified in the final revision.
- [ ] Review type is labeled correctly: self-review, AI review, or independent human review.
- [ ] The target branch and PR head were revalidated immediately before merge.

---

## B — Sentetik deneye geçmeden önce

- [ ] Deneyin bağlı olduğu açık problem ve yanlışlanabilir hipotez yazıldı.
- [ ] Başarı, başarısızlık ve kapsam dışı ölçütleri önceden tanımlandı.
- [ ] Kullanılacak veriler sentetik; gerçek kimlik, gerçek tercih veya üretim sırrı içermiyor.
- [ ] Saldırgan görünürlüğü ve ilgili tehditler tanımlandı.
- [ ] İlgili küçük grup, tekrar yayın, zamanlama, istemci, davet, bütünlük ve hata senaryoları test planında.
- [ ] Tekrar üretim yolu kaydedildi; olumsuz sonuçlar saklanıyor.
- [ ] Sentetik deney sonucu gerçek dünya anonimliği, insan tekilliği, güvenlik veya karar kalitesi kanıtı olarak sunulmuyor.

### EN · Before synthetic experiments

- [ ] The linked open problem and falsifiable hypothesis are written down.
- [ ] Success, failure, and out-of-scope criteria are predefined.
- [ ] Data is synthetic and contains no real identity, real preference, or production secret.
- [ ] Attacker visibility and relevant threats are defined.
- [ ] Relevant small-group, repeated-release, timing, client, invitation, integrity, and error scenarios are in the test plan.
- [ ] Reproduction steps are recorded and negative results are preserved.
- [ ] Synthetic results are not presented as proof of real-world anonymity, human uniqueness, security, or decision quality.

---

## C — Gerçek katılımcılı pilot veya üretimden önce

- [ ] Gerekçeli ifşa ve tekrar yayın politikası var; küçük grup saldırıları test edildi.
- [ ] Uygunluk, tekrar önleme, iptal/kurtarma, istemci, işletmeci işbirliği ve ağ gözlemci varsayımları yazıldı.
- [ ] Veri envanteri, erişim, saklama/silme, yedek, anahtar ve olay müdahale politikaları hazır.
- [ ] Gönüllülük, erişilebilirlik, baskı riski, etik ve uygulanabilir veri koruma yükümlülükleri yetkin kişilerce incelendi.
- [ ] Uygulamaya özgü testler ve bağımsız güvenlik/mahremiyet değerlendirmesi tamamlandı.
- [ ] Kritik/yüksek bulgular yetkili insan tarafından kapatıldı.
- [ ] Dağıtım ortamı, izleme, geri alma ve durdurma mekanizmaları doğrulandı.
- [ ] Proje sahibinin pilot/üretim için ayrı açık kararı var.

### EN · Before a real-participant pilot or production

- [ ] A justified disclosure/repeated-release policy exists and small-group attacks were tested.
- [ ] Eligibility, replay prevention, revocation/recovery, client, operator-collusion, and network-observer assumptions are documented.
- [ ] Data inventory, access, retention/deletion, backup, key, and incident-response policies exist.
- [ ] Voluntariness, accessibility, coercion risk, ethics, and applicable data-protection duties were reviewed by competent people.
- [ ] Application-specific tests and independent security/privacy review are complete.
- [ ] Critical/high findings were closed by an authorized human.
- [ ] Deployment, monitoring, rollback, and stop mechanisms were verified.
- [ ] The project owner made a separate explicit pilot/production decision.

Bir dokümantasyon PR’ının birleştirilmesi daha sonraki kapıların geçtiği anlamına gelmez.

Merging a documentation PR does not imply that later gates have been passed.