# Komite — Araştırmadan Kullanıma Yol

Bu belge takvim veya teslim sözü değil, kanıta bağlı aşama haritasıdır. Bir aşamanın belgelenmiş olması tamamlandığını göstermez.

## Aşamalar

| Aşama | Çıkış kanıtı | Durum mantığı |
| --- | --- | --- |
| 0 — Açık kaynak temel | Tutarlı kapsam/karar/tehdit belgeleri, korunmuş lisans, incelenmiş değişiklikler | Belge temeli düzenli ve izlenebilir olmalı |
| 1 — Araştırma çerçevesi | Güncel kaynak incelemesi, saldırgan modeli, karşılaştırma ölçütleri ve test edilebilir iddialar | Başlangıç belgeleri tek başına yeterli kanıt değildir |
| 2 — Sentetik deney | Tekrar üretilebilir deneyler; üstveri, küçük grup, davet, bütünlük ve perspektif-faydası karşı örnekleri | Gerçek kimlik/tercih verisi kullanılmaz |
| 3 — Mimari değerlendirme | Adayların ölçümü, reddedilen alternatifler, uzman incelemesi ve açık insan kararı | Mimari belgeyle değil kanıtla seçilir |
| 4 — Sınırlı pilot hazırlığı | İfşa politikası, gönüllülük/etik/veri koruma incelemesi, destek ve durdurma planı, ayrı onay | Yetkilendirme ayrı karardır |
| 5 — Üretim değerlendirmesi | Uygulama testleri, bağımsız güvenlik/mahremiyet değerlendirmesi, işletim ve olay müdahale kanıtı | Üretim hazırlığı ayrıca kanıtlanır |

Küresel ölçek, tüm dünyada insan tekilliği, baskıya dayanıklılık veya karar kalitesinde iyileşme için teslim tarihi yoktur. Sonuç olumsuzsa kapsam daraltılabilir, mimari adayı reddedilebilir veya çalışma durabilir.

### EN · Stages

This document is not a delivery promise or calendar. It is an evidence-gated path. A stage being documented does not mean it is complete.

| Stage | Exit evidence | Status logic |
| --- | --- | --- |
| 0 — Open-source foundation | Consistent scope/decision/threat docs, preserved license, reviewed changes | Documentation must be coherent and traceable |
| 1 — Research framework | Current source review, attacker model, comparison criteria, testable claims | Initial documents alone are not sufficient evidence |
| 2 — Synthetic experiments | Reproducible experiments covering metadata, small groups, invitations, integrity, and perspective-value counterexamples | No real identity/preference data |
| 3 — Architecture evaluation | Measured candidates, rejected alternatives, expert review, explicit human decision | Architecture is selected by evidence, not wording |
| 4 — Limited-pilot preparation | Disclosure policy, voluntariness/ethics/data-protection review, support and stop plan, separate approval | Authorization is a separate decision |
| 5 — Production evaluation | Application tests, independent security/privacy review, operations and incident-response evidence | Production readiness must be separately demonstrated |

There is no delivery date for global scale, worldwide human uniqueness, coercion resistance, or improved decision quality. Negative results may narrow scope, reject an architecture candidate, or stop the work.

## Aşamalar arası değişmez sınırlar

- Oy/tercih sonucu kararın kendisi değildir; karar için bir girdidir.
- Yönetici/temsilci seçimi, kamu/devlet seçimi, referandum ve bağlayıcı karar üretimi kapsam dışıdır.
- Onaylı küçük grup ifşa politikası olmadan gerçek sonuç yayını yoktur.
- Sentetik deney sonucu gerçek dünyada mahremiyet, insan tekilliği, güvenlik veya karar kalitesi ispatı değildir.
- Belge birleştirme, gerçek veri veya üretim dağıtımı yetkisi değildir.
- Yanlış karar veya başarısız deney silinmez; gerekçesiyle düzeltilir ve öğrenme kaydı korunur.

### EN · Invariants across stages

- A vote/preference result is an input to a decision, not the decision itself.
- Leader/representative selection, public/state elections, referendums, and binding decisions are out of scope.
- No real result publication without an approved small-group disclosure policy.
- Synthetic experiments do not prove real-world privacy, human uniqueness, security, or decision quality.
- Merging documents does not authorize real data or production deployment.
- Wrong decisions and failed experiments are not erased; they are corrected with reasons and preserved as learning records.

Geçiş ölçütleri: [Yayın Kontrol Listesi](docs/YAYIN-KONTROL-LISTESI.md)  
Araştırma soruları: [Araştırma](ARASTIRMA.md)

Transition criteria: [Release Checklist](docs/YAYIN-KONTROL-LISTESI.md)  
Research questions: [Research](ARASTIRMA.md)