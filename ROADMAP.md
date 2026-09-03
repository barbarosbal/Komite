# Komite — Araştırmadan kullanıma yol

Bu belge takvim veya teslim sözü değil, kanıta bağlı aşama haritasıdır. Ayrıntılı yürütme işleri için mükerrer görev listesi oluşturmaz. Bir aşamanın belgelenmiş olması tamamlandığını göstermez.

| Aşama | Çıkış kanıtı | Bu yayın sırasındaki durum |
| --- | --- | --- |
| 0 — Açık kaynak temel | Tutarlı kapsam/karar/tehdit belgeleri, korunmuş lisans, incelenmiş PR | Bu değişikliğin kapsamı; kapanış kanıtı birleştirilen PR |
| 1 — Araştırma çerçevesi | Güncel kaynak incelemesi, saldırgan modeli, karşılaştırma ölçütleri ve test edilebilir iddialar | Açık; başlangıç belgeleri yeterli kanıt değil |
| 2 — Sentetik deney | Tekrar üretilebilir deneyler; log/üstveri, küçük grup, davet ve bütünlük karşı örnekleri | Başlamadı; gerçek kimlik/tercih verisi yok |
| 3 — Mimari değerlendirme | Adayların ölçümü, reddedilen alternatifler, uzman incelemesi ve açık insan kararı | Seçim yapılmadı |
| 4 — Sınırlı pilot hazırlığı | İfşa politikası, gönüllülük/etik/veri koruma incelemesi, destek ve durdurma planı, ayrı onay | Yetkilendirilmedi |
| 5 — Üretim değerlendirmesi | Uygulama testleri, bağımsız güvenlik değerlendirmesi, işletim/olay müdahale kanıtı ve ayrı yayın kararı | Hazır değil |

Küresel ölçek, tüm dünyada insan tekilliği veya baskıya dayanıklılık için teslim tarihi yoktur. Sonuç olumsuzsa kapsam daraltılabilir, mimari adayı reddedilebilir veya çalışma durabilir; bunlar araştırma başarısızlığını gizlemek için geçilmiş gösterilmez.

## Aşamalar arası değişmez sınırlar

- Oy sonucu kararın kendisi değildir; karar için bir girdidir.
- Yönetici/temsilci seçimi, kamu/devlet seçimi, referandum ve bağlayıcı karar üretimi kapsam dışıdır.
- Onaylı küçük grup ifşa politikası olmadan gerçek sonuç yayını yoktur.
- Sentetik deney sonucu gerçek dünyada mahremiyet, insan tekilliği veya güvenlik ispatı değildir.
- Belge birleştirme, gerçek veri veya üretim dağıtımı yetkisi değildir.

Geçiş ölçütlerinin ayrıntısı: [RELEASE-CHECKLIST.md](docs/RELEASE-CHECKLIST.md). Araştırma soruları: [RESEARCH.md](RESEARCH.md).

## English summary

Progress is evidence-gated, not date-driven. Documentation, synthetic experiments, architecture selection, pilot approval and production evaluation are separate stages. No runtime, pilot, global-scale claim or production readiness is implied by this publication.
