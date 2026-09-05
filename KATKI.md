# Komite — Katkı rehberi

Araştırma, karşı örnek, yöntem eleştirisi, tehdit analizi, erişilebilirlik ve belge katkıları beklenir. Türkçe ana dildir; kritik kapsam ve güvenlik değişikliklerinin İngilizce özeti de güncellenir. Proje adı her dilde **Komite** yazılır.

Komite düz bir özellik listesi olarak değil, birbirine engelleyici ilişkilerle bağlı **açık problemler ağı** olarak geliştirilir. Yeni katkıya başlamadan önce [Açık Problem Ağı](ACIK-PROBLEMLER.md) belgesini okuyun. Bir katkıcı bütün projeyi üstlenmek zorunda değildir; uzmanlığına en yakın problemi ve onu engelleyen alt problemleri çözmeye odaklanabilir.

## Başlamadan önce

[Kapsamı](KAPSAM.md), [Açık Problem Ağı'nı](ACIK-PROBLEMLER.md), [karar modelini](docs/KARAR-MODELI.md), [güvenlik politikasını](GUVENLIK.md) ve ilgili mevcut PR’ları okuyun. Aynı çalışmanın veya kararın zaten bulunup bulunmadığını kontrol edin. Güvenlik açığı ayrıntılarını kamusal kanala koymayın.

## Yeni problem önermek

Yeni bir problem kaydı, yalnızca yapılacak işi değil çözülecek problemi tanımlamalıdır. Mümkün olduğunda `.github/ISSUE_TEMPLATE/open-problem.md` şablonunu kullanın.

Yeni problem kaydı açılması özellikle şu durumlarda uygundur:

- kök problemi çözmemizi engelleyen yeni bir bilinmez ortaya çıktığında,
- mevcut çözümün önemli bir varsayımı sorgulandığında,
- yeni güvenlik, mahremiyet, insan, bilim, tasarım veya uygulama riski keşfedildiğinde,
- başka bir problem kaydının çözülmesi için önce çözülmesi gereken yeni bir alt problem bulunduğunda.

Aynı problem zaten varsa yinelenen kayıt açmak yerine mevcut kayda kanıt, karşı örnek veya bağlantı ekleyin. Bir problem kaydı çalışma yapıldığı için değil, önceden tanımlanan kapanma ölçütleri sağlandığında kapanır; yeni kanıt gelirse yeniden açılabilir.

## Katkı akışı

1. Küçük belge düzeltmesini doğrudan ayrı dalda hazırlayın. Büyük değişiklikte önce amaç, kapsam dışı alanlar, kaynaklar, etkilenen tehditler ve kabul ölçütlerini açıklayan teklif hazırlayın.
2. Kendi fork (depo kopyası) veya yetkili dalınızda çalışın; doğrudan `main` üzerine yazmayın. Hassas veri veya gizli konuşma metni eklemeyin.
3. PR’da gerekçe, değişen dosyalar, kanıtlar, sınırlamalar ve doğrulama sonucunu belirtin. [PR şablonunu](.github/pull_request_template.md) kullanın.
4. Değişiklik farkını bütün olarak inceleyin; kapsam, lisans, kaynak doğruluğu, Türkçe/İngilizce anlam eşliği ve göreli bağlantıları kontrol edin. Belge değişikliği güvenlik ispatı değildir.
5. Bulguları [seviyelere](GUVENLIK.md) göre kaydedin, düzeltmeleri aynı dala ekleyin ve son sürümü yeniden inceleyin. [Yönetişim](YONETISIM.md) onay sınırları geçerlidir.

## Uygulama katkısından önce

Şu an uygulama kodu veya test altyapısı yoktur. Sentetik uygulama hazırlığının ayrıntılı ve güncel koşulları [Yayın Kontrol Listesi — Gate B](docs/YAYIN-KONTROL-LISTESI.md#b--komite-sentetik-deneyine-geçmeden-önce) içindedir. Gelecekte kod yazmadan önce mevcut mimari, ilgili iş kaydı/önceki PR ve mükerrer iş riski de kontrol edilmelidir. Mimari seçimi, gerçek veri, kimlik doğrulama veya dağıtım kararları belge yayını yetkisinden türetilemez. Yeni bağımlılığın lisansı, bakımı ve güvenlik durumu ayrıca değerlendirilir.

Kod katkıları için test ve kalite kapıları o uygulamanın ortamına göre tanımlanmadan “testler geçti” denemez. Mevcut depo için çalıştırılabilir ürün komutu uydurmayın.

## İçerik ve davranış

- İddiaları kaynak, varsayım ve kanıt düzeyiyle ayırın. Karşı örnek ve olumsuz araştırma sonuçlarını gizlemeyin.
- İnsanları değil argümanları eleştirin; taciz, ayrımcılık, kimlik ifşası ve baskı kabul edilmez. Davranış sorunlarını proje iletişim adresine özel iletin; proje sahibi moderasyon gerekçesini mahremiyeti koruyarak açıklar.
- Katkı üzerinde gerekli haklara sahip olun; üçüncü taraf içeriklerini izin/lisansı olmadan kopyalamayın. Mevcut [Apache-2.0](LICENSE) korunur; kasıtlı katkılar için lisansın katkı hükümleri geçerlidir. Ayrı bir katkı sözleşmesi varmış gibi davranmayın.
- AI destekli katkıda kullanılan yardımın kapsamını PR’da açıklayın; doğruluk, kaynak ve güvenlik sorumluluğu katkıyı sunandadır. AI öz denetimini bağımsız insan incelemesi diye sunmayın.

## Kayıtların yeri

GitHub katkı farkları, PR görüşmeleri ve mühendislik kanıtlarını taşır. Katkıcının özel şirket sistemlerine erişmesi gerekmez; inceleme için gereken kamuya açık ve güvenli bağlam PR’da sağlanır. Özel karar kayıtları, araştırma notları ve ham konuşmalar depoya kopyalanmaz. İç yürütme takibi varsa aynı iş için mükerrer kayıt açmak yerine proje sahibiyle ilişkilendirilir.

## English summary

Komite is developed as an open problem network. Start with `ACIK-PROBLEMLER.md`, choose a problem close to your expertise, follow its blockers, and use the open-problem issue template for new problem proposals. Use a branch and a focused PR, never direct writes to main. Keep Turkish primary and critical English summaries consistent. Disclose AI assistance, cite evidence, protect private data and preserve Apache-2.0. Self-review is not independent human review. No private company-tool access is required to contribute.
