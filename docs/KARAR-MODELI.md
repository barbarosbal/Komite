# Komite — Karar Modeli

Durum: araştırma tasarımı; çalışan davranış veya seçilmiş protokol değildir. Kapsam: [Kapsam](../KAPSAM.md).

> **Oy veya tercih sonucu kararın kendisi değildir; karar için bir girdidir.**

> **Görüş istemek onay istemek değildir.** Amaç çoğunluğu takip etmek değil, karar sahibinin daha geniş bir görüş alanına sahip olmasını sağlamaktır.

### EN · Decision model

Status: research design; not an implemented behavior or selected protocol. Scope: [KAPSAM.md](../KAPSAM.md).

> **A vote or preference result is not the decision itself; it is an input to the decision.**

> **Asking for another view is not asking for approval.** The goal is not to follow the majority but to widen the decision-maker's field of view.

## Roller ve sorumluluk

- **Karar sahibi:** sorunu ve nihai karar yetkisini açıklar; sonuçtan farklı karar verirse gerekçesini kaydeder. Komite bu yetkiyi devralmaz.
- **Süreç kolaylaştırıcısı:** soru, kaynak, seçenek ve takvim taslağını hazırlar; çıkar çatışmasını açıklar.
- **Uygunluk sorumlusu:** bağlamsal katılım kuralını uygular. Tercihe erişmemesi bir tasarım hedefidir, mevcut garanti değildir.
- **Katılımcı:** bilgilendirilmiş ve gönüllü biçimde görüş bildirir; katılmama ve çekimserlik ayrı durumlardır.
- **İncelemeci:** çerçeveleme, dışlama ve ifşa riskini değerlendirir; karar sahibi adına bağlayıcı yorum yapmaz.

### EN · Roles and responsibility

- **Decision owner:** defines the problem and retains final decision authority; records reasoning when deciding differently from the aggregate signal.
- **Facilitator:** prepares the question, sources, options, and schedule; discloses conflicts of interest.
- **Eligibility operator:** applies contextual participation rules. Not learning the preference is a design target, not a current guarantee.
- **Participant:** provides a view voluntarily and with appropriate information; non-participation and abstention are different states.
- **Reviewer:** evaluates framing, exclusion, and disclosure risk; does not make a binding interpretation on behalf of the decision owner.

## Tasarlanan süreç

1. Problem, karar sahibi, kapsam ve sonucun nasıl kullanılacağı açıklanır.
2. Hedef topluluk, uygunluk kuralı, davet/örnekleme yöntemi ve çıkar çatışmaları belgelenir.
3. Soru, kaynaklar, seçenekler, anlama kontrolü, kapanış zamanı ve ifşa politikası katılım öncesinde sürümlenir. Maddi değişiklikte eski ve yeni yanıtlar sessizce birleştirilmez.
4. Anlama kontrolü bağlamı açıklar. Yanlış cevap katılım hakkını kaldırmaz, oy ağırlığını veya uygunluğu değiştirmez.
5. Katılımcı kabul, ret veya çekimser tercihini; isterse önceden tanımlı alternatif tavsiyesini bildirir. İlk model serbest metin içermez.
6. Tur kapanır. Bütünlük, eksik veri, ifşa ve tekrar sorgu denetimleri geçmeden sonuç yayımlanmaz.
7. Güvenli bulunursa yalnız izin verilen toplu sinyal ve sınırları açıklanır. Karar sahibi sistem dışında nihai kararı ve gerekçesini verir.
8. Sonuç ve süreç kalitesi sonradan incelenir; bireylerin tercihi geriye dönük profillenmez.

### EN · Designed process

1. State the problem, decision owner, scope, and intended use of the result.
2. Document the target population, eligibility rule, invitation/sampling method, and conflicts of interest.
3. Version the question, sources, options, understanding check, closing time, and disclosure policy before participation. Do not silently combine responses across material changes.
4. The understanding check provides context. A wrong answer must not remove participation rights or change vote weight/eligibility.
5. The participant may express accept/reject/abstain and optionally choose from predefined alternatives. The initial model contains no free text.
6. The round closes. Do not publish results until integrity, missing-data, disclosure, and repeated-query checks pass.
7. If safe, publish only the permitted aggregate signal and its limitations. The decision owner makes and explains the final decision outside the system.
8. Review outcomes and process quality later without retrospectively profiling individual preferences.

## Geri çekme ve düzeltme sınırı

Gönderim öncesinde katılımdan vazgeçilebilir. Gönderim sonrasında belirli bir tercihi bulup silme veya değiştirme ile kimlik-tercih bağlantısızlığı arasında tasarım gerilimi vardır. Bu akış henüz seçilmedi; anonim gönderimin sonradan kişi adına geri alınabileceği vaat edilmez.

Gerçek kullanım öncesinde düzeltme, geri çekme, saklama ve silme sınırları katılımcıya açıkça anlatılmalı ve uygulanabilir veri koruma gereklilikleriyle birlikte incelenmelidir.

### EN · Withdrawal and correction boundary

A participant may stop before submission. After submission, locating and changing/deleting a specific preference can conflict with identity-preference unlinkability. No post-submission withdrawal mechanism has been selected, and it must not be promised.

Before real-world use, correction, withdrawal, retention, and deletion limits must be clearly explained and reviewed against applicable data-protection requirements.

## Anlama kontrolü ve yönlendirme riski

Çerçeveleme ve önceden yönlendirme, “doğru cevap” üzerinden tercih telkinine dönüşebilir. Kontrol soruları görüş onayı arayamaz. Kaynak seçimi, kelime tonu, seçenek sırası ve karşı görüşün eksikliği incelenir.

Anlama puanı bireysel tercihle eşleştirilmez. Anlama yanıtı, zamanlama ve tekrar deneme sayısı da hassas üstveri olabilir. Bu nedenle anlama verisi de [Tehdit Modeli](TEHDIT-MODELI.md) içindeki küçük grup ve tekrar yayın politikalarına tabidir.

### EN · Understanding check and steering risk

Framing and priming can turn a “correct answer” into preference steering. Understanding checks must not seek approval of a viewpoint. Source selection, wording tone, option order, and omission of opposing views require review.

Understanding scores must not be linked to individual preferences. Understanding responses, timing, and retry counts can themselves be sensitive metadata, so they are subject to the same small-group and repeated-release rules in the [Threat Model](TEHDIT-MODELI.md).

## Sonuç sözleşmesi

Bir sonuç raporu, ifşa politikasının izin verdiği ayrıntıda şunları taşır:

- tur ve soru sürümü, tarih aralığı, karar sahibi, yöntem ve önceden açıklanan değişiklikler,
- davet/örnekleme yöntemi, uygunluk kapsamı, kapsanmayan gruplar ve bilinen seçilim etkileri,
- kabul/ret/çekimser paydası; yanıt vermeme çekimser sayılmaz,
- katılım, eksik/başarısız bildirim ve veri kalitesi belirsizliği,
- bastırılan alanlar ve güvenli düzeyde gerekçesi,
- temsiliyet sınırı, bütünlük kontrolünün kapsamı ve karar sahibinin ayrı nihai gerekçesi.

Anlık bireysel bildirim akışı, kişi bazlı anlama puanı ve indirilebilir ham tercihler yayımlanmaz. Minimum güvenli ifşa eşiği henüz belirlenmemiştir: onaylı politika yoksa sonuç yayını da yoktur.

### EN · Result contract

A result report, to the extent allowed by the disclosure policy, should include the round/question version, date range, decision owner, method, declared changes, sampling/invitation method, eligibility scope, excluded groups, known selection effects, denominators for accept/reject/abstain, participation and missing-data uncertainty, suppressed fields and safe rationale, representativeness limits, integrity-check scope, and the decision owner's separate final reasoning.

Do not publish real-time individual submissions, per-person understanding scores, or downloadable raw preferences. No minimum safe disclosure threshold has been approved; without an approved policy, no result is published.

## Durdurma koşulları

Uygunluk ihlali, manipüle içerik, bütünlük belirsizliği veya güvenli ifşa politikasının yokluğu turu veya sonuç yayınını durdurur. “Güvensiz ama yararlı” gerekçesiyle ham veriler açılmaz.

### EN · Stop conditions

Eligibility violations, manipulated content, integrity uncertainty, or absence of a safe disclosure policy stop the round or result publication. Raw data is not released on the basis that it is “unsafe but useful.”