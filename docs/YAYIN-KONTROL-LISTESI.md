# Komite — Yayın kapıları

Bu kontrol listesi bir tamamlanma beyanı değildir. Her yayın için gerçek sonuçlar, kontrol edilen değişiklik kaydı, inceleme ve birleştirme kanıtı değişiklik önerisinde tutulur. Gelecekteki uygulama kapıları bu belge yayınıyla geçilmiş sayılmaz.

## A — Bu belge temelinin yayımlanması

- [ ] README ve mevcut LICENSE başlangıç sürümünde incelendi; mükerrer PR/iş kontrolü yapıldı.
- [ ] Ayrı dal kullanıldı; `main` üzerine doğrudan yazılmadı.
- [ ] README'nin yönlendirdiği güncel belge seti mevcut: `ACIK-PROBLEMLER.md`, `KAPSAM.md`, `ARASTIRMA.md`, `KATKI.md`, `GUVENLIK.md`, `YONETISIM.md`, `YOL-HARITASI.md`, `docs/KARAR-MODELI.md`, `docs/TEHDIT-MODELI.md`, `docs/MIMARI-YONLER.md`, `docs/YAYIN-KONTROL-LISTESI.md` ve bu PR için `docs/CLAUDE-INCELEME-BRIFI.md`; göreli bağlantılar çalışıyor ve proje adı tutarlı.
- [ ] Apache-2.0 LICENSE değişmedi; yeni kullanım kısıtı lisansa eklenmedi.
- [ ] Kapsam dışı seçim/referandum/bağlayıcılık sınırları ve çekirdek ilke tutarlı.
- [ ] Metafor mimari diye sunulmuyor; dört araştırma yönü ve birleşik tekillik/mahremiyet açığı açık.
- [ ] `Komite-Open-Project-Deck-v0.1-ESKI.pdf` arşiv olarak etiketli; güncel sunum diye bağlantılanmıyor veya dağıtılmıyor. İç uyarı/filigran yoksa dosyanın tek başına paylaşılmasının kalan yanlış-anlaşılma riski açıkça kabul ediliyor.
- [ ] İstenen tehditler, anlama kontrolü ve küçük grup güvenli kapanma kuralı mevcut.
- [ ] Hassas veri, ham konuşma veya kanıtsız güvenlik/üretim iddiası yok.
- [ ] PR farkı bütünüyle okundu; bulgular seviyelendirildi; düzeltmeler son sürümde doğrulandı.
- [ ] İnceleme etiketi doğru: `öz-denetim`, `bağımsız insan incelemesi` veya `AI incelemesi`. Öz-denetim ve AI incelemesi bağımsız insan incelemesi diye sunulmadı.
- [ ] Açık belge bulgusu yok; gereken insan onayları var; varsa otomatik kontroller başarılı. Otomatik kontrol yoksa açıkça belirtildi.
- [ ] Birleştirme öncesi hedef dalın değişmediği ve beklenen PR başı doğrulandı; değiştiyse inceleme yenilendi.

### Yerel tekrar kontrolü

Hedef dalın son durumunu alın ve aşağıdaki salt-okunur kontrolleri depo kökünde çalıştırın. Dal ilerlediyse farkı yeniden inceleyin:

```sh
git diff --check origin/main...HEAD
git diff --name-status origin/main...HEAD
git diff origin/main...HEAD -- LICENSE
git hash-object LICENSE
```

Bu temelin LICENSE nesnesi `261eeb9e9f8b2b4b0d119366dda99c6fd7d35c64` değerindedir. Lisans farkı boş kalmalıdır. README belge tablosundaki dosyaları ve tüm göreli bağlantıları tek tek açın; ad yazımını, İngilizce özetleri ve tüm farkın anlamını kontrol edin. Bu komutlar anlamsal/güvenlik incelemesinin yerine geçmez; uzak bağlantılarda oturum gereksinimini erişim hatasından ayırın. Sonuçları incelenen sürümle birlikte PR’a yazın.

## B — Komite sentetik deneyine geçmeden önce

- [ ] Deneyin bağlı olduğu açık problem, yanlışlanabilir hipotez, başarı/başarısızlık ölçütü ve kapsam dışı alanlar yazıldı.
- [ ] Aynı problemi çözen mevcut deney, dal veya değişiklik önerisi tarandı; mükerrer çalışma açılmadı.
- [ ] Kullanılacak sentetik katılımcı, uygunluk, davet, anlama, tercih, üstveri ve sonuç verileri envanterlendi; hiçbir gerçek kimlik, gerçek tercih veya üretim sırrı yok.
- [ ] Saldırgan görünürlüğü ve ilgili insan dili problem başlıkları tanımlandı; T kodları yalnız geri izleme için eklendi.
- [ ] Küçük grup, tekrar yayın, zamanlama, istemci, davet devri, eşzamanlı tekrar ve sonuç bütünlüğü kırma senaryolarından ilgili olanlar test planında.
- [ ] Deney izole dalda, sabit veri üretimi ve tekrar çalıştırma talimatıyla yürütülecek; başarısız/olumsuz sonuçlar da saklanacak.
- [ ] Çıktının yalnız sentetik kanıt olduğu; anonimlik, insan tekilliği, karar kalitesi, pilot veya üretim hazırlığını kanıtlamadığı rapor şablonunda görünür.
- [ ] Gerekli inceleme türü önceden seçildi ve `öz-denetim`, `bağımsız insan incelemesi` veya `AI incelemesi` diye doğru etiketlendi.

## C — Gerçek katılımcılı pilot veya üretimden önce

- Gerekçeli ifşa eşiği ve tamamlayıcı/tekrarlı yayın politikası; anlama ve katılım verisi dahil saldırı testleri.
- Uygunluk, tekrar önleme, iptal/kurtarma, istemci, işletmeci işbirliği ve ağ gözlemci varsayımları.
- Veri envanteri, erişim, saklama/silme, yedek, anahtar ve olay müdahale politikaları.
- Gönüllülük, erişilebilirlik, baskı riski, etik ve uygulanabilir veri koruma yükümlülüklerinin yetkin incelemesi; gönderim sonrası geri çekme/düzeltme sınırlarının açıklanması.
- Uygulamaya özgü testler, bağımlılık incelemesi, bağımsız güvenlik değerlendirmesi ve kritik/yüksek bulguların yetkili insan tarafından kapatılması.
- Doğrulanmış dağıtım ortamı, çalışan sürümün kaynak kaydıyla eşleşmesi, izleme, geri alma ve durdurma denemeleri.
- Dal koruması ve gereken kalite kontrollerinin gerçekten etkin olduğuna dair kanıt; sır/yetki ayarları için ayrı yetki.
- Proje sahibinin pilot/üretim için ayrı açık kararı. Araştırma belgesinin kabulü güvenlik riskinin kabulü değildir.

## English summary

Documentation release, synthetic implementation and real-participant deployment have distinct gates. An unchecked future gate cannot be inferred from a merged documentation PR. Record the reviewed revision and actual evidence; do not claim automated checks or independent review that did not occur.
