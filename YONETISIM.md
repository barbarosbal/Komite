# Komite — Proje Yönetişimi

Bu belge açık kaynak projenin bakım, değişiklik ve karar kayıt sürecini tanımlar. Komite üzerinden yönetici/temsilci seçimi veya bağlayıcı karar üretimi tasarlamaz.

Mevcut kapsam [KAPSAM.md](KAPSAM.md) ile tanımlıdır. Kapsam değişikliği yalnız gerekçesi, etkileri, karşıt görüşleri ve proje sahibinin açık kararı kaydedilerek yapılabilir.

## Sorumluluk

Proje sahibi ve başlangıç bakım sorumlusu Barbaros Hayrettin Bal’dır; iletişim [README.md](README.md) içindedir. Seçilmiş kurul, bağımsız güvenlik ekibi, çoklu bakım sorumlusu veya kesintisiz destek varmış gibi iddiada bulunulmaz.

Katkıcı değişiklik önerir ve kanıt sağlar. İncelemeci bulguları ve inceleme sınırlarını kaydeder. Proje sahibi kapsam, yayın ve yetki kararlarını verir. Yeni bakım yetkileri açıkça kaydedilmeden varsayılmaz.

### EN · Responsibility

This document defines the maintenance, change, and decision-record process for the open-source project. It does not design leader/representative selection or binding decisions through Komite.

The current scope is defined in [KAPSAM.md](KAPSAM.md). A scope change requires recorded reasoning, effects, opposing views, and an explicit decision by the project owner.

Barbaros Hayrettin Bal is the initial project owner and maintainer; contact details are in [README.md](README.md). The project does not claim to have an elected board, independent security team, multiple maintainers, or continuous support unless those roles are explicitly established.

## Karar ve birleştirme akışı

1. Teklif, gerekçe, alternatifler, kabul ölçütleri ve kapsam dışı alanlar açıklanır.
2. Değişiklik ayrı dal ve PR üzerinden değerlendirilir. Yorum sayısı veya çoğunluk kabul kararı değildir.
3. Bulgular engelleyici/yüksek/orta/düşük olarak, dosya/sürüm ve kanıtla ilişkilendirilir.
4. Düzeltme sonrası son değişiklik bütünüyle yeniden doğrulanır.
5. Onay kapsamı ve birleştirilen sürüm PR’da kaydedilir.
6. Yanlış bir karar yeni kanıtla değiştirilebilir; önceki karar ve düzeltme gerekçesi history’de korunur.

### EN · Decision and merge flow

1. State the proposal, reasoning, alternatives, acceptance criteria, and out-of-scope areas.
2. Review changes through a separate branch and PR. Comment count or majority is not the acceptance decision.
3. Record findings as blocker/high/medium/low with file/version and evidence.
4. Revalidate the complete final change after fixes.
5. Record the approval scope and merged revision in the PR.
6. A wrong decision may be changed when new evidence appears; the earlier decision and the reason for correction remain in history.

## Ayrı insan onayı gereken alanlar

Rutin belge düzenleme, mevcut yetki kapsamında yapılabilir. Aşağıdakiler ayrı açık insan onayı gerektirir:

- yeni güvenlik veya mimari seçimi,
- kapsam genişlemesi,
- gerçek katılımcılı pilot,
- üretim dağıtımı,
- sır/yetki değişikliği,
- geri döndürülemez işlem veya açık güvenlik riskinin kabulü.

Kritik/yüksek AI bulguları yalnız AI tarafından kapatılmış sayılamaz.

### EN · Changes requiring separate human approval

Routine documentation changes may proceed under existing authority. Architecture/security selection, scope expansion, a real-participant pilot, production deployment, secret/permission changes, irreversible actions, or acceptance of an open security risk require separate explicit human approval.

Critical/high AI findings cannot be considered closed by AI alone.

## Bağımsızlık ve uygulanabilirlik sınırı

Öz denetim çalışma kalitesini artırabilir; bağımsız uzman veya insan incelemesi değildir. Gerçek kullanıma geçişte ilgili alanlarda bağımsız güvenlik/mahremiyet incelemesi gerekir. Tek bakım sorumlusu riski saklanmaz.

Bu metin GitHub dal koruması, zorunlu incelemeci veya CI kuralını kendiliğinden etkinleştirmez. Yazılı politika ile gerçekten etkin teknik kontrol birbirinden ayrı tutulur.

### EN · Independence and enforceability

Self-review can improve quality but is not independent expert or human review. Real-world use requires relevant independent security/privacy review. The single-maintainer risk is not hidden.

This document does not automatically enable GitHub branch protection, required reviewers, or CI. Written policy and actually enforced technical controls are separate things.

## Kayıt ve yetki ayrımı

GitHub kamuya açık değişiklik ve inceleme kanıtlarını taşır. Public katkı için özel şirket araçlarına erişim gerekmez. Ham özel konuşmalar, kişisel veriler ve yayınlanmaması gereken iç kayıtlar depoya kopyalanmaz.

Yetki veya kayıtlar arasında çelişki varsa sessizce yeniden yorumlanmaz; açıkça kaydedilir ve proje sahibinin kararına sunulur.

### EN · Separation of records and authority

GitHub carries public change and review evidence. Access to private company tools is not required for public contribution. Raw private conversations, personal data, and non-public internal records must not be copied into the repository.

Conflicts between authority or records are not silently reinterpreted; they are recorded and presented for an explicit project-owner decision.

## Özel bulgudan kamusal düzeltmeye sınır

[Güvenlik Politikası](GUVENLIK.md) özel bildirimin ilk temasını yönetir. Sömürü yolu, kişisel veri, gizli erişim bilgisi veya yeniden tanımlama verisi kamusal PR’a kopyalanmaz. Kamusal düzeltme yalnız sorunu anlamak ve yanlış iddiayı gidermek için gereken en az bağlamı taşır.

### EN · From private finding to public correction

[Security](GUVENLIK.md) governs the first contact for private reports. Exploit paths, personal data, secret access information, or re-identification data must not be copied into public PRs. A public correction should contain only the minimum context needed to understand and correct the issue.