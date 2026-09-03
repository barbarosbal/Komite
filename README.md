# Komite

Daha iyi kararlar. Daha iyi gelecek.

Komite, insanların görüşlerinden mahremiyeti gözeterek kolektif sinyal üretmeyi araştıran açık kaynak **decision support (karar destek) altyapısı** projesidir. Hedef; karar sahibinin farklı görüşleri, belirsizlikleri ve alternatifleri karar öncesinde değerlendirebilmesidir. Daha iyi sonuç elde edilmesi bir araştırma hipotezidir, garanti değildir.

> Oy sonucu kararın kendisi değildir; karar için bir girdidir.

## Durum ve sınırlar

Bu depo şu anda araştırma ve tasarım belgeleri içerir. Çalışan uygulama, kurulabilir paket, güvenliği denetlenmiş protokol veya üretim hizmeti sunmaz. Açık kaynak belgelerin yayımlanması, gerçek katılımcılı kullanıma hazır olunduğu anlamına gelmez.

Komite yönetici veya temsilci seçmez; kamu/devlet seçimi, referandum veya bağlayıcı karar üretimi için tasarlanmaz. Nihai karar ve sorumluluk, sistem dışındaki yetkili karar sahibinde kalır. Ayrıntılar: [Kapsam](SCOPE.md).

**Kanıtlanmamış hedefler:** anonymity (anonimlik), unlinkability (bağlantısızlık), ihlal sonrası geçmiş tercihlerin korunması, coercion resistance (baskıya dayanıklılık), global unique-human verification (küresel tekil insan doğrulaması), privacy (mahremiyet) ve sybil resistance (sahte/çoklu kimlikle katılıma dayanıklılık) birlikteliği. Tekil bir hesap veya davet, tekil bir gerçek insanın kanıtı değildir.

“Tek kapı, tek anahtar” yalnız bir metafordur; protokol, anahtar yönetimi veya mimari çözüm değildir. Hiçbir kriptografik yaklaşım henüz seçilmedi. [Mimari yönler](docs/ARCHITECTURE-DIRECTIONS.md) alternatifleri ve açık sorunları gösterir.

## Başlangıç

Kurulum komutu yoktur. Önce kapsamı, sonra karar ve tehdit modellerini okuyun. Araştırma katkısı için [CONTRIBUTING.md](CONTRIBUTING.md) yolunu izleyin; güvenlik açıklarını herkese açık iş kaydına yazmayın.

| Belge | İçerik |
| --- | --- |
| [SCOPE.md](SCOPE.md) | Kullanım sınırları ve kapsam dışı alanlar |
| [Karar modeli](docs/DECISION-MODEL.md) | Katılım, anlama kontrolü, toplu sinyal ve karar sorumluluğu |
| [Tehdit modeli](docs/THREAT-MODEL.md) | Saldırganlar, güven varsayımları, testler ve kalan riskler |
| [Mimari yönler](docs/ARCHITECTURE-DIRECTIONS.md) | Seçilmemiş teknik alternatifler |
| [RESEARCH.md](RESEARCH.md) | Araştırma soruları, birincil kaynaklar ve kanıt standardı |
| [ROADMAP.md](ROADMAP.md) | Takvim vaadi olmayan, kanıta bağlı aşamalar |
| [SECURITY.md](SECURITY.md) | Özel güvenlik bildirimi ve destek sınırı |
| [CONTRIBUTING.md](CONTRIBUTING.md) | Katkı ve inceleme akışı |
| [GOVERNANCE.md](GOVERNANCE.md) | Proje bakım sorumluluğu ve karar yetkileri |
| [Yayın kontrolü](docs/RELEASE-CHECKLIST.md) | Belge yayını ile gerçek kullanım arasındaki kapılar |

## Sunum ve iletişim

[Figma proje sunumu](https://www.figma.com/design/TQpScgWMitXaSP5vlM5bMI) görsel bağlamdır; güvenlik kanıtı veya güncel teknik şartname değildir. Dış bağlantının erişimi ve içeriği değişebilir. Sunumdaki hedef ifadeleri çalışan özellik sayılmamalıdır; bu deponun kapsam ve güvenlik sınırlamaları geçerlidir.

Proje iletişimi: Barbaros Hayrettin Bal — [barbaroshbal@gmail.com](mailto:barbaroshbal@gmail.com) · [LinkedIn](https://www.linkedin.com/in/barbarosb/).

## Lisans

Mevcut [Apache-2.0 LICENSE](LICENSE) korunur. Projenin desteklediği kullanım kapsamı lisansa ek kullanım kısıtı getirmez. Harici yayınlar ve Figma içeriği, bağlantı verilmesiyle bu deponun lisansı altına alınmış olmaz.

## English summary

Komite is an open-source research project for privacy-conscious decision support. **The vote result is not the decision; it is an input to the decision.** It is not a system for electing leaders or representatives, public/state elections, referendums, or binding decisions. This repository contains documentation, not a production-ready service. Human uniqueness, privacy, Sybil resistance, anonymity and coercion resistance are unresolved system-level research goals. “One door, one key” is a metaphor, not an architecture. The existing Apache-2.0 license remains unchanged.
