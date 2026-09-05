# Komite — Açık Problem Ağı

Komite tek bir özellik listesi değil, kök problemi çözmek için parçalanmış açık problemler ağı olarak geliştirilir.

> Kök problem: İnsanların gerçek düşüncelerini daha güvenli biçimde ortaya çıkararak daha iyi kararlar alınmasına nasıl yardımcı olabiliriz?

Her problem bağımsız olarak incelenebilir, başka problemlere bağlı olabilir, yeni alt problemler doğurabilir ve gerektiğinde yeniden açılabilir. Bir problemin kapanması "hakikat bulundu" anlamına gelmez; tanımlı kabul ölçütleri altında yeterli bir çözüm elde edildiği anlamına gelir.

## Çalışma ilkeleri

1. Her problem kaydı çözülecek bir problemi temsil eder. Kod, araştırma, manifesto, yönetişim, mahremiyet, istatistik, tasarım ve dokümantasyon problemleri aynı modelde yer alabilir.
2. Büyük problemler daha küçük alt problemlere ayrılır.
3. Bir problem başka bir problem çözülmeden ilerleyemiyorsa engelleyici ilişki açıkça kaydedilir.
4. Yeni kanıt mevcut çözümü zayıflatıyorsa kapanmış problem yeniden açılabilir.
5. Kişinin itibarı çözümü doğrulamaz. Gerekçe, kanıt, karşı örnek ve incelemeye dayanıklılık değerlendirilir.
6. Çözülmemiş veya güvenle açıklanamayan alanlar saklanmaz; proje sınırı olarak görünür tutulur.

## Problem yaşam döngüsü

**Ön İnceleme → Açık Problem → Üstlenildi → Araştırılıyor / Çalışılıyor → İncelemede → Çözüldü**

Gerektiğinde:

**Engelli · Reddedildi · Yinelenen**

- **Ön İnceleme:** Yeni problem önerisi değerlendiriliyor.
- **Açık Problem:** Geçerli ve kapsam içi problem; henüz aktif çalışması yok.
- **Üstlenildi:** Bir katkıcı problemi üstlenmiş.
- **Araştırılıyor / Çalışılıyor:** Araştırma, tasarım veya uygulama çalışması sürüyor.
- **Engelli:** Başka problem veya kanıt çözülmeden ilerleyemiyor.
- **İncelemede:** Bir çözüm önerilmiş; karşı örnek ve bağımsız inceleme bekleniyor.
- **Çözüldü:** Önceden tanımlanmış kapanma ölçütleri sağlanmış.
- **Reddedildi:** Problem veya öneri kapsam dışı ya da geçersiz bulunmuş.
- **Yinelenen:** Aynı problem başka bir kayıt altında zaten izleniyor.

## Bir problem kaydı ne zaman açılır?

Aşağıdakilerden en az biri doğruysa yeni problem kaydı açılması değerlendirilir:

- Kök problemi çözmemizi engelleyen yeni bir bilinmez ortaya çıktı.
- Mevcut çözümün önemli bir varsayımı sorgulanıyor.
- Yeni güvenlik, mahremiyet, insan, bilim, tasarım veya uygulama riski keşfedildi.
- Başka bir problemin çözülebilmesi için önce çözülmesi gereken alt problem oluştu.

Aynı problem zaten varsa yeni kayıt yerine mevcut kayda kanıt, karşı örnek veya bağlantı eklenir.

## Problem şablonu

Her problem mümkün olduğunca şu alanları içerir:

### Problem
Tam olarak neyi bilmiyoruz, ne çalışmıyor veya hangi iddia savunulamıyor?

### Kök problemle ilişkisi
Bu problem Komite'nin ana amacını neden etkiliyor?

### Mevcut bilgi
Şu ana kadar ne biliyoruz?

### Varsayımlar
Neyi geçici olarak doğru kabul ediyoruz?

### Engelleyiciler
Önce hangi problemlerin çözülmesi gerekiyor?

### Bağlı problemler
Bu problem hangi diğer problemlere bağlı veya onları etkiliyor?

### Beklenen çıktı
Araştırma, matematiksel model, prototip, deney, metin, test, politika veya başka hangi çıktı bekleniyor?

### Karşı örnek / kırma testi
Önerilen çözüm nasıl yanlışlanabilir veya hangi senaryoda başarısız olur?

### Sınırlar
Bu çözüm neyi çözmez?

### Kapanma ölçütü
Hangi somut koşullar oluşursa problem çözüldü kabul edilir?

## Kapanma sözleşmesi

Bir problem çalışma yapıldığı için değil, önceden yazılmış kapanma ölçütleri sağlandığı için kapanır.

Asgari beklenti:

- problem ve kapsam açık,
- varsayımlar görünür,
- ilgili kanıtlar kaydedilmiş,
- kritik karşı örnekler değerlendirilmiş,
- bilinen engelleyiciler çözülmüş veya açıkça kapsam dışı bırakılmış,
- çözümün sınırları yazılmış,
- gerekli inceleme tamamlanmış,
- yeni doğan problemler ayrı kayıt olarak açılmış veya bağlanmış.

**Çözüldü ≠ sonsuz doğruluk.** Yeni kanıt geldiğinde problem yeniden açılabilir.

## Katılım modeli

Komite katkıları konu uzmanlığına göre parçalanabilir. Bir katkıcı bütün projeyi anlamak zorunda değildir; ilgilendiği problem ve onun engelleyicileri için gerekli bağlamı anlaması yeterlidir.

Kamusal katkı ile proje içi yetki aynı şey değildir. Gelecekte kamusal problem gezgini ve anonim katkı yüzeyi ayrı tasarlanabilir; GitHub ve Linear doğrulanmış çalışma ve inceleme kayıtlarını taşır.

## İlk problem kümesi: Mahremiyet

### Mahremiyet
*İnsanların düşüncelerini açığa çıkarmadan nasıl birlikte düşünebiliriz?*

İlk alt problemler:

- **Kimlik** — Bir insanın kim olduğunu bilmeden katılmaya hakkı olduğunu nasıl doğrularız?
- **Bağ** — Bir görüşün kime ait olduğu sonradan bulunabilir mi?
- **İz** — Zaman, cihaz veya bağlantı bilgileri bir insanı ele verebilir mi?
- **Ölçü** — Bir sonucu ne kadar ayrıntıyla açıklamak güvenlidir?
- **Karşılaştırma** — Farklı sonuçlar bir araya getirilerek bir insanın görüşü bulunabilir mi?
- **Sessizlik** — Bir şeyi açıklamamak bile bilgi verebilir mi?
- **Katılım** — Bir insanın katılıp katılmadığı başlı başına hassas bilgi olabilir mi?
- **Hata** — Bir hata veya iptal mesajı istemeden bilgi açığa çıkarabilir mi?

Özellikle temel ilke:

> Sakladığın şeyin saklanmış olması bile bilgi olabilir.

Bu nedenle yalnız yayımlanan sonuç değil, sonuç açıklamama davranışı da mahremiyet modelinin parçasıdır.

## English summary

Komite is developed as an open problem network rather than a flat feature backlog. Each problem has explicit assumptions, dependencies, evidence, review requirements, limits, and closure criteria. Contributors may work on the problem closest to their expertise without needing full-project access. A solved problem means the defined criteria are currently satisfied, not that permanent truth has been established.
