# Komite — Katkı rehberi

Araştırma, karşı örnek, yöntem eleştirisi, tehdit analizi, erişilebilirlik ve belge katkıları beklenir. Türkçe ana dildir; kritik kapsam ve güvenlik değişikliklerinin İngilizce özeti de güncellenir. Proje adı her dilde **Komite** yazılır.

Komite düz bir özellik listesi olarak değil, birbirine blocker ilişkileriyle bağlı **açık problemler ağı** olarak geliştirilir. Yeni katkıya başlamadan önce [Açık Problem Ağı](OPEN-PROBLEMS.md) belgesini okuyun. Bir katkıcı bütün projeyi üstlenmek zorunda değildir; uzmanlığına en yakın problemi ve onu engelleyen alt problemleri çözmeye odaklanabilir.

## Başlamadan önce

[Kapsamı](SCOPE.md), [Açık Problem Ağı'nı](OPEN-PROBLEMS.md), [karar modelini](docs/DECISION-MODEL.md), [güvenlik politikasını](SECURITY.md) ve ilgili mevcut PR’ları okuyun. Aynı çalışmanın veya kararın zaten bulunup bulunmadığını kontrol edin. Güvenlik açığı ayrıntılarını kamusal kanala koymayın.

## Yeni problem önermek

Yeni bir issue, yalnızca yapılacak işi değil çözülecek problemi tanımlamalıdır. Mümkün olduğunda `.github/ISSUE_TEMPLATE/open-problem.md` şablonunu kullanın.

Yeni issue açılması özellikle şu durumlarda uygundur:

- kök problemi çözmemizi engelleyen yeni bir bilinmez ortaya çıktığında,
- mevcut çözümün önemli bir varsayımı sorgulandığında,
- yeni güvenlik, mahremiyet, insan, bilim, tasarım veya uygulama riski keşfedildiğinde,
- başka bir issue'nun çözülmesi için önce çözülmesi gereken yeni bir alt problem bulunduğunda.

Aynı problem zaten varsa mükerrer issue açmak yerine mevcut issue'ya kanıt, karşı örnek veya bağlantı ekleyin. Bir issue çalışma yapıldığı için değil, önceden tanımlanan kapanma kriterleri sağlandığında kapanır; yeni kanıt gelirse yeniden açılabilir.

## Katkı akışı

1. Küçük belge düzeltmesini doğrudan ayrı dalda hazırlayın. Büyük değişiklikte önce amaç, kapsam dışı alanlar, kaynaklar, etkilenen tehditler ve kabul ölçütlerini açıklayan teklif hazırlayın.
2. Kendi fork (depo kopyası) veya yetkili dalınızda çalışın; doğrudan `main` üzerine yazmayın. Hassas veri veya gizli konuşma metni eklemeyin.
3. PR’da gerekçe, değişen dosyalar, kanıtlar, sınırlamalar ve doğrulama sonucunu belirtin. [PR şablonunu](.github/pull_request_template.md) kullanın.
4. Değişiklik farkını bütün olarak inceleyin; kapsam, lisans, kaynak doğruluğu, Türkçe/İngilizce anlam eşliği ve göreli bağlantıları kontrol edin. Belge değişikliği güvenlik ispatı değildir.
5. Bulguları [seviyelere](SECURITY.md) göre kaydedin, düzeltmeleri aynı dala ekleyin ve son sürümü yeniden inceleyin. [Yönetişim](GOVERNANCE.md) onay sınırları geçerlidir.

## Uygulama katkısından önce

Şu an uygulama kodu veya test altyapısı yoktur. Gelecekte kod yazmadan önce mevcut mimari, ilgili iş kaydı/önceki PR, mükerrer iş riski, kabul ölçütleri, kapsam dışı alanlar, veri/aktör sınırları ve test planı hazırlanmalıdır. Mimari seçimi, gerçek veri, kimlik doğrulama veya dağıtım kararları belge yayını yetkisinden türetilemez. Yeni bağımlılığın lisansı, bakımı ve güvenlik durumu ayrıca değerlendirilir.

Kod katkıları için test ve kalite kapıları o uygulamanın ortamına göre tanımlanmadan “testler geçti” denemez. Mevcut depo için çalıştırılabilir ürün komutu uydurmayın.

## İçerik ve davranış

- İddiaları kaynak, varsayım ve kanıt düzeyiyle ayırın. Karşı örnek ve olumsuz araştırma sonuçlarını gizlemeyin.
- İnsanları değil argümanları eleştirin; taciz, ayrımcılık, kimlik ifşası ve baskı kabul edilmez. Davranış sorunlarını proje iletişim adresine özel iletin; proje sahibi moderasyon gerekçesini mahremiyeti koruyarak açıklar.
- Katkı üzerinde gerekli haklara sahip olun; üçüncü taraf içeriklerini izin/lisansı olmadan kopyalamayın. Mevcut [Apache-2.0](LICENSE) korunur; kasıtlı katkılar için lisansın katkı hükümleri geçerlidir. Ayrı bir katkı sözleşmesi varmış gibi davranmayın.
- AI destekli katkıda kullanılan yardımın kapsamını PR’da açıklayın; doğruluk, kaynak ve güvenlik sorumluluğu katkıyı sunandadır. AI öz denetimini bağımsız insan incelemesi diye sunmayın.

## Kayıtların yeri

GitHub katkı farkları, PR görüşmeleri ve mühendislik kanıtlarını taşır. Katkıcının özel şirket sistemlerine erişmesi gerekmez; inceleme için gereken kamuya açık ve güvenli bağlam PR’da sağlanır. Özel karar kayıtları, araştırma notları ve ham konuşmalar depoya kopyalanmaz. İç yürütme takibi varsa aynı iş için mükerrer kayıt açmak yerine proje sahibiyle ilişkilendirilir.

## English summary

Komite is developed as an open problem network. Start with `OPEN-PROBLEMS.md`, choose a problem close to your expertise, follow its blockers, and use the open-problem issue template for new problem proposals. Use a branch and a focused PR, never direct writes to main. Keep Turkish primary and critical English summaries consistent. Disclose AI assistance, cite evidence, protect private data and preserve Apache-2.0. Self-review is not independent human review. No private company-tool access is required to contribute.
