# Komite — Açık Problem Ağı

Komite tek bir özellik listesi değil, kök problemi çözmek için parçalanmış açık problemler ağı olarak geliştirilir.

> Kök problem: İnsanların gerçek düşüncelerini daha güvenli biçimde ortaya çıkararak daha iyi kararlar alınmasına nasıl yardımcı olabiliriz?

Her problem bağımsız olarak incelenebilir, başka problemlere bağlı olabilir, yeni alt problemler doğurabilir ve gerektiğinde yeniden açılabilir. Bir problemin kapanması "hakikat bulundu" anlamına gelmez; tanımlı kabul ölçütleri altında yeterli bir çözüm elde edildiği anlamına gelir.

## Çalışma ilkeleri

1. Her issue çözülecek bir problemi temsil eder. Kod, araştırma, manifesto, yönetişim, mahremiyet, istatistik, tasarım ve dokümantasyon problemleri aynı modelde yer alabilir.
2. Büyük problemler daha küçük alt problemlere ayrılır.
3. Bir problem başka bir problem çözülmeden ilerleyemiyorsa blocker ilişkisi açıkça kaydedilir.
4. Yeni kanıt mevcut çözümü zayıflatıyorsa kapanmış problem yeniden açılabilir.
5. Kişinin itibarı çözümü doğrulamaz. Gerekçe, kanıt, karşı örnek ve incelemeye dayanıklılık değerlendirilir.
6. Çözülmemiş veya güvenle açıklanamayan alanlar saklanmaz; proje sınırı olarak görünür tutulur.

## Issue yaşam döngüsü

**Triage → Open Problem → Claimed → Research / Work → Review → Accepted**

Gerektiğinde:

**Blocked · Rejected · Duplicate**

- **Triage:** Yeni problem önerisi değerlendiriliyor.
- **Open Problem:** Geçerli ve kapsam içi problem; henüz aktif çalışması yok.
- **Claimed:** Bir katkıcı problemi üstlenmiş.
- **Research / Work:** Araştırma, tasarım veya uygulama çalışması sürüyor.
- **Blocked:** Başka problem veya kanıt çözülmeden ilerleyemiyor.
- **Review:** Bir çözüm önerilmiş; karşı örnek ve bağımsız inceleme bekleniyor.
- **Accepted:** Önceden tanımlanmış kapanma kriterleri sağlanmış.
- **Rejected:** Problem veya öneri kapsam dışı ya da geçersiz bulunmuş.
- **Duplicate:** Aynı problem başka issue altında zaten izleniyor.

## Bir issue ne zaman açılır?

Aşağıdakilerden en az biri doğruysa yeni issue açılması değerlendirilir:

- Kök problemi çözmemizi engelleyen yeni bir bilinmez ortaya çıktı.
- Mevcut çözümün önemli bir varsayımı sorgulanıyor.
- Yeni güvenlik, mahremiyet, insan, bilim, tasarım veya uygulama riski keşfedildi.
- Başka bir issue'nun çözülebilmesi için önce çözülmesi gereken alt problem oluştu.

Aynı problem zaten varsa yeni issue yerine mevcut issue'ya kanıt, karşı örnek veya bağlantı eklenir.

## Problem issue şablonu

Her problem mümkün olduğunca şu alanları içerir:

### Problem
Tam olarak neyi bilmiyoruz, ne çalışmıyor veya hangi iddia savunulamıyor?

### Kök problemle ilişkisi
Bu problem Komite'nin ana amacını neden etkiliyor?

### Mevcut bilgi
Şu ana kadar ne biliyoruz?

### Varsayımlar
Neyi geçici olarak doğru kabul ediyoruz?

### Blocker'lar
Önce hangi problemlerin çözülmesi gerekiyor?

### Bağlı problemler
Bu problem hangi diğer problemlere bağlı veya onları etkiliyor?

### Beklenen çıktı
Araştırma, matematiksel model, prototip, deney, metin, test, politika veya başka hangi çıktı bekleniyor?

### Karşı örnek / kırma testi
Önerilen çözüm nasıl yanlışlanabilir veya hangi senaryoda başarısız olur?

### Sınırlar
Bu çözüm neyi çözmez?

### Kapanma kriteri
Hangi somut koşullar oluşursa issue çözüldü kabul edilir?

## Kapanma sözleşmesi

Bir issue çalışma yapıldığı için değil, önceden yazılmış kapanma kriterleri sağlandığı için kapanır.

Asgari beklenti:

- problem ve kapsam açık,
- varsayımlar görünür,
- ilgili kanıtlar kaydedilmiş,
- kritik karşı örnekler değerlendirilmiş,
- bilinen blocker'lar çözülmüş veya açıkça kapsam dışı bırakılmış,
- çözümün sınırları yazılmış,
- gerekli inceleme tamamlanmış,
- yeni doğan problemler ayrı issue olarak açılmış veya bağlanmış.

**Closed ≠ eternal truth.** Yeni kanıt geldiğinde issue yeniden açılabilir.

## Katılım modeli

Komite katkıları konu uzmanlığına göre parçalanabilir. Bir katkıcı bütün projeyi anlamak zorunda değildir; ilgilendiği problem ve onun blocker'ları için gerekli bağlamı anlaması yeterlidir.

Kamusal katkı ile proje içi yetki aynı şey değildir. Gelecekte kamusal problem gezgini ve anonim katkı yüzeyi ayrı tasarlanabilir; GitHub ve Linear canonical çalışma ve inceleme kayıtlarını taşır.

## R01 — ilk problem kümesi

**R01 — Anonimlik Kümesi ve Sonuç Açıklama Politikası**

İlk alt problemler:

- **R01.1 — Saldırgan modelini tanımla**
- **R01.2 — Asgari güvenli açıklama kümesini modelle**
- **R01.3 — Katılım bilgisinin sızıntı yüzeyini incele**
- **R01.4 — Eksik veri ve yarıda bırakma davranışını tanımla**
- **R01.5 — Birleşik gizlilik bütçesi ve kesişim riskini modelle**
- **R01.6 — İptal, bastırma ve hata mesajlarının bilgi sızıntısını incele**

Özellikle R01 için temel ilke:

> Sakladığın şeyin saklanmış olması bile bilgi olabilir.

Bu nedenle yalnız yayımlanan sonuç değil, sonuç açıklamama davranışı da mahremiyet modelinin parçasıdır.

## English summary

Komite is developed as an open problem network rather than a flat feature backlog. Each issue represents an unresolved problem with explicit assumptions, blockers, evidence, review requirements, limits and closure criteria. Contributors may work on the problem closest to their expertise without needing full-project access. A closed issue means the defined criteria are currently satisfied, not that permanent truth has been established.
