# Komite — Claude bağımsız inceleme brifi

## Amaç

Bu brif, hazırlık değişikliği birleştirilmeden önce yapılacak bağımsız ve karşıt incelemeyi tarif eder. İnceleme henüz yapılmamıştır. Amaç metni onaylamak değil; yanlış, çelişkili, kanıtsız veya gereğinden güçlü iddiaları kırmaya çalışmaktır.

Komite, tamamlanacak bir ürün ya da özellik listesi olarak değil, çözülecek bir **problem ağı** olarak ele alınmalıdır. Bir problem üzerinde çalışılmış olması kapanma ölçütünün sağlandığını göstermez.

## İncelenecek kaynaklar

- [README](../README.md)
- [Açık Problem Ağı](../ACIK-PROBLEMLER.md)
- [Kapsam](../KAPSAM.md)
- [Araştırma](../ARASTIRMA.md)
- [Karar Modeli](KARAR-MODELI.md)
- [Mimari Yönler](MIMARI-YONLER.md)
- [Tehdit Modeli](TEHDIT-MODELI.md)
- [Güvenlik](../GUVENLIK.md)
- [Yönetişim](../YONETISIM.md)
- [Yol Haritası](../YOL-HARITASI.md)
- [Katkı Rehberi](../KATKI.md)
- [Yayın Kontrol Listesi](YAYIN-KONTROL-LISTESI.md)

Depodaki `Komite-Open-Project-Deck-v0.1-ESKI.pdf` arşiv niteliğindedir. Güncel manifesto ve sunum yerine değerlendirilmemeli; belge tutarlılığı kontrolünde yalnız eski anlatımla oluşabilecek çelişkileri göstermek için kullanılmalıdır.

## İnceleme görevleri

1. **Problem-ağı modeli:** Kök problem, alt problemler, bağımlılıklar, engelleyiciler ve yeniden açma kuralı belgeler arasında aynı anlamı taşıyor mu? Ürün tamamlanmışlığı ima eden dil var mı?
2. **Manifesto ve teknik belgeler:** Güncel manifesto dışa aktarımı sağlandığında manifesto ile kapsam, karar modeli, mimari yönler ve tehdit modeli arasında çelişki ara. Manifesto sağlanmamışsa bu denetimi `yetersiz kanıt` olarak işaretle; varsayım üretme.
3. **İnsan dili:** Görünen problem ve alt problem adları kısa, doğal bir kavram ile herkesin anlayabileceği bir sorudan oluşuyor mu? Gereksiz İngilizce veya yalnız uzmanların anlayacağı etiketleri listele.
4. **Mahremiyet ve anonimlik:** Anonimlik, kimlik bağlantısızlığı, tekil insan, uygunluk, Sybil direnci, istemci güvenliği, üstveri ve işletmeci ayrılığı iddialarını kırmaya çalış. Araştırma hedefi ile kanıtlanmış özellik birbirine karışıyor mu?
5. **Kapanma ölçütleri:** Her problemin yanlışlanabilir ve doğrulanabilir kapanma ölçütü var mı? Çalışma yapılmasını çözüm sayan veya öz incelemeyi bağımsız inceleme gibi sunan yerleri bul.
6. **Tehdit modeli:** Saldırganlar, güven sınırları, birleşik tehditler, küçük grup ifşası, baskı, istemci ele geçirilmesi, tekrar yayınlar ve ihlal sonrası bağlantı yeterince ele alınmış mı? Eksik tehdit ve karşı örnek öner.
7. **Çapraz bağlantılar:** Tüm göreli bağlantıları, dosya adlarını ve başlık hedeflerini doğrula. Eski İngilizce dosya adına veya bulunmayan belgeye işaret eden her referansı bul.
8. **Kanıtlanmamış iddialar:** Üretim hazırlığı, güvenlik, anonimlik, ölçek, doğrulanabilirlik, temsil ve karar kalitesi hakkında kanıt düzeyini aşan her cümleyi alıntıla ve neden savunulamadığını açıkla.
9. **Epistemik statü:** İlke, Hedef, Hipotez, Açık Problem ve Kanıtlanmış Bulgu ayrımını README ile tüm teknik belgelerde karşılaştır. Özellikle uygunluk, mahremiyet, anonimlik ve “daha dürüst/daha nitelikli sinyal” dilinin statüsüz veya aşırı güçlü kaldığı yerleri bul.
10. **Bağımlılık haritası:** İnsan dili problem haritasındaki her engelleyici ilişkiyi tehdit, karar, araştırma ve yayın kapılarıyla karşılaştır. Bağımsız inceleme olmadan kapanamayacak problemlerin eksik veya gereksiz olanlarını belirt.
11. **Özel/kamusal sınır:** Güvenlik bildirimindeki hassas ayrıntıların kamusal düzeltmeye taşınma sınırını saldırgan ve iyi niyetli bildirici açısından kırmaya çalış.
12. **Eski sunum:** Eski PDF’deki “Anonim Seçim”, Kapı/Oda ve “daha dürüst/daha nitelikli sinyal sağlar” ifadelerinin güncel belgelerde garanti gibi devam edip etmediğini kontrol et. PDF’yi güncel kaynak veya manifesto sayma.
13. **Küme kapsamı:** README'deki Mahremiyet, Karar ve Öğrenme kümelerinin Açık Problem Ağı'nda karşılığı ve doğru açık/kapanmış statüsü var mı?
14. **İnceleme kapsamı:** Bağımsız inceleme örneklerinin tüketici bir muafiyet listesi gibi okunabildiği yer var mı? T01-T12 ve gerçek-kullanım iddiaları için genel kural belgeler arasında tutarlı mı?

## Beklenen çıktı

- Sonuç: `GEÇER`, `DEĞİŞİKLİK GEREKİYOR` veya `YETERSİZ KANIT`.
- Bulgular: `Engelleyici`, `Yüksek`, `Orta`, `Düşük` öncelikleriyle; dosya ve bölüm referansı, kırılma senaryosu, gereken düzeltme ve doğrulama yöntemi.
- Tutarlılık tablosu: iddia, kaynak belge, karşı belge, kanıt durumu ve çelişki.
- Eksik kanıt listesi: doğrulanamayan her iddia için gereken kaynak veya deney.
- Açıkça ayrılmış bölüm: bağımsız bulgular ile yalnız dil/biçim önerileri.
- Her bulgu için etiket: `öz-denetim`, `bağımsız insan incelemesi` veya `AI incelemesi`; bu Claude çıktısı `AI incelemesi`dir ve bağımsız insan güvenlik onayı değildir.

İncelemeci, depo sahibinin niyetini tamamlamaya veya metni savunmaya çalışmamalıdır. `Bilmiyorum`, `kanıtlanmadı` ve `yetersiz kanıt` geçerli sonuçlardır.
