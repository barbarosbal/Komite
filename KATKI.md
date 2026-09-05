# Komite — Katkı Rehberi

Komite açık bir problem ağı olarak geliştirilir. Bir katkıcı bütün projeyi bilmek zorunda değildir; uzmanlığına veya merakına en yakın problemi seçip onun bağlamını ve engelleyicilerini anlaması yeterlidir.

Public belgelerde Türkçe bölümün hemen ardından İngilizce karşılığı bulunur. Proje adı her dilde **Komite** yazılır.

## Başlamadan önce

[Kapsam](KAPSAM.md), [Açık Problem Ağı](ACIK-PROBLEMLER.md), [Karar Modeli](docs/KARAR-MODELI.md) ve [Güvenlik Politikası](GUVENLIK.md) okunmalıdır. Aynı problem veya değişiklik zaten varsa mükerrer kayıt açmak yerine mevcut kayda katkı verilir.

### EN · Before you start

Komite is developed as an open problem network. Contributors do not need to understand the entire project; it is enough to understand the problem closest to their expertise or curiosity, its context, and its blockers.

In public documents, each Turkish section is followed immediately by its English counterpart. The project name is always written **Komite**.

Read [Scope](KAPSAM.md), [Open Problems](ACIK-PROBLEMLER.md), [Decision Model](docs/KARAR-MODELI.md), and [Security](GUVENLIK.md). If the same problem or change already exists, contribute to the existing record instead of opening a duplicate.

## Yeni problem önermek

Yeni kayıt yalnız yapılacak işi değil, çözülecek problemi tanımlamalıdır. Mümkün olduğunda `.github/ISSUE_TEMPLATE/open-problem.md` şablonu kullanılır.

Yeni problem özellikle şu durumlarda anlamlıdır:

- kök problemi çözmemizi engelleyen yeni bir bilinmez ortaya çıktığında,
- önemli bir varsayım sorgulandığında,
- yeni güvenlik, mahremiyet, insan, bilim, tasarım veya uygulama riski keşfedildiğinde,
- başka bir problemin çözülmesi için önce çözülmesi gereken yeni alt problem bulunduğunda.

Bir problem çalışma yapıldığı için değil, önceden tanımlanan kapanma ölçütleri sağlandığında kapanır. Yeni kanıt gelirse yeniden açılabilir.

### EN · Proposing a new problem

A new record should describe the problem to solve, not merely the work to perform. Use `.github/ISSUE_TEMPLATE/open-problem.md` when possible.

A new problem is especially appropriate when a new unknown blocks the root problem, an important assumption is challenged, a new security/privacy/human/scientific/design/implementation risk appears, or a new prerequisite problem is discovered.

A problem closes because predefined closure criteria are satisfied, not because work was performed. New evidence can reopen it.

## Katkı akışı

1. Değişikliği ayrı dalda hazırlayın; doğrudan `main` üzerine yazmayın.
2. Gerekçe, kanıt, sınırlamalar, etkilenen problemler ve doğrulama sonucunu PR’da açıklayın.
3. Türkçe ve İngilizce karşılıkların anlam eşliğini kontrol edin.
4. Güvenlik, kapsam ve lisans sınırlarını yeniden okuyun.
5. Öz denetimi bağımsız insan incelemesi gibi göstermeyin.
6. AI yardımı kullanıldıysa kapsamını açıklayın; doğruluk ve güvenlik sorumluluğu katkıyı sunandadır.

### EN · Contribution flow

1. Prepare the change on a separate branch; do not write directly to `main`.
2. Explain the reasoning, evidence, limitations, affected problems, and validation results in the PR.
3. Check semantic equivalence between Turkish and English sections.
4. Recheck security, scope, and license boundaries.
5. Do not present self-review as independent human review.
6. Disclose the scope of AI assistance; the contributor remains responsible for accuracy and security.

## Güvenlik ve hassas bulgular

Hassas güvenlik açığı, yeniden tanımlama riski veya sömürülebilir ayrıntı herkese açık issue/PR içine konmamalıdır. [Güvenlik Politikası](GUVENLIK.md) içindeki özel bildirim yolu kullanılmalıdır.

### EN · Security and sensitive findings

Do not publish sensitive vulnerabilities, re-identification risks, or exploitable details in public issues or PRs. Use the private reporting path in [Security](GUVENLIK.md).

## Kayıtların yeri

GitHub kamuya açık katkı, değişiklik ve inceleme kayıtlarını taşır. Public katkı için herhangi bir özel şirket sistemine erişim gerekmez. Ham özel konuşmalar, kişisel veriler ve yayınlanmaması gereken iç kayıtlar depoya kopyalanmaz.

### EN · Where records live

GitHub carries public contribution, change, and review records. No access to private company systems is required to contribute publicly. Raw private conversations, personal data, and non-public internal records must not be copied into the repository.

## Lisans

Mevcut [Apache-2.0](LICENSE) lisansı korunur. Katkı sahibi eklediği içerik üzerinde gerekli haklara sahip olmalıdır; üçüncü taraf içerikleri izin veya uygun lisans olmadan kopyalanmamalıdır.

### EN · License

The existing [Apache-2.0](LICENSE) license is preserved. Contributors must have the necessary rights to what they submit and must not copy third-party content without permission or an appropriate license.