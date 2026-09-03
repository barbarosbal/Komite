# Komite

[PDF / Project Deck](docs/Komite-Open-Project-Deck-v0.1.pdf)

> Bu yayın araştırma ve tasarım belgeleridir; çalışan uygulama, kurulabilir paket veya üretime hazır hizmet değildir. Aşağıdaki ifadeler hedefleri anlatır, kanıtlanmış özellikleri değil.
>
> This release contains research and design documents, not a working application, installable package or production-ready service. The statements below describe objectives, not proven capabilities.

Daha iyi kararlar. Daha iyi gelecek.

Better decisions. Better future.

Açık kaynak karar destek projesi

Open-source decision support project

Barbaros Hayrettin Bal · Bağımsız Geliştirici

Independent Developer · barbaroshbal@gmail.com · LinkedIn : https://www.linkedin.com/in/barbarosb/

## 01 · MERHABA DÜNYA

HELLO, WORLD

Türkiye benim evim, dünya mahallem.

Türkiye is my home. The world is my neighborhood.

Amacım; komşularımla birlikte, daha iyi kararların alındığı, daha huzurlu, daha mutlu ve daha güzel bir gelecekte yaşamak.

My goal is to live with my neighbors in a more peaceful, happier and better future shaped by better decisions.

Milyarlarca beyin, bir beyinden daha akıllıdır.

Billions of brains are smarter than one.

## 02 · PROBLEM

PROBLEM

İnsanlar her zaman gerçekten düşündüklerini söylemez.

People do not always say what they really think.

Hiyerarşi, sosyal baskı, otorite etkisi, kariyer riski ve grup dinamikleri gerçek görüşleri değiştirebilir, yumuşatabilir veya görünmez hale getirebilir.

Hierarchy, social pressure, authority, career risk and group dynamics can distort, soften or suppress genuine opinions.

## 03 · TEMEL TEZ

CORE THESIS

Kimlerin katılabileceği doğrulanabilir olmalı.

Kimin ne tercih ettiği belirlenememeli.

Membership must be verifiable. Individual choice must not be attributable.

01 · İnsan uygunluğu  —  Yalnızca doğrulanmış gerçek insanlar katılabilir.

01 · Human eligibility  —  Only verified real humans may participate.

02 · Bağlantısızlık  —  Gerçek kimlik ile seçim arasında yeniden kurulabilir bir bağ olmamalıdır.

02 · Unlinkability  —  There should be no recoverable link between real identity and individual choice.

## 04 · Komite NEDIR?

WHAT IS Komite?

Komite bir seçim sistemi değildir.

Komite is not an election system.

Yönetici seçmez. Temsilci seçmez. Referandum yürütmez. Bağlayıcı karar üretmez.

It does not elect leaders or representatives, conduct referendums, or produce binding decisions.

Komite, karar sahibine karar öncesinde daha geniş, daha dürüst ve daha nitelikli kolektif sinyal sağlar.

Komite provides broader, more candid and higher-quality collective signals before a decision is made.

## 05 · KARAR DESTEĞI

DECISION SUPPORT

Oy sonucu kararın kendisi değildir.

Karar için bir girdidir.

The vote is not the decision. It is an input to the decision.

Şirketler, ekipler, STK’lar ve kamu kurumları Komite’yi danışma ve karar destek amacıyla kullanabilir. Komite seçim, temsilci veya yönetici seçimi, referandum, bağlayıcı kamu oylaması ya da resmî seçim altyapısı değildir.

Companies, teams, NGOs and public institutions may use Komite for consultation and decision support. Komite is not an election, representative or leader selection system, referendum, binding public vote, or official election infrastructure.

## 06 · KARAR DÖNGÜSÜ

DECISION CYCLE

Problem Tanımı → Komite → Anlama Kontrolü → Anonim Seçim → Alternatif Tavsiye → Toplu Sonuç → Karar → Sonuç → Öğrenme ↻

Problem Definition → Komite → Understanding Gate → Anonymous Choice → Alternative Recommendation → Aggregate Result → Decision → Outcome → Learning ↻

Yönetim izi · Karar Sahibi → Uygunluk Kuralı → Soru → Seçenekler → Komite → Sonuç → Nihai Karar<br>
Anonimlik, kimin davet edildiği veya seçeneklerin nasıl çerçevelendiği sorununu tek başına çözmez.

Governance provenance · Decision Owner → Eligibility Rule → Question → Options → Komite → Result → Final Decision<br>
Anonymity alone does not solve who is invited or how choices are framed.

## 07 · KATILIMCI AKIŞI

PARTICIPANT FLOW

01 · Anlama Kontrolü

Kararın bağlamını anlamaya yönelik çoktan seçmeli sorular. Yanlış cevap katılım hakkını kaldırmaz.

Understanding Gate · Multiple-choice questions about the decision context. Incorrect answers do not remove participation rights.

02 · Ana Seçim

Kabul · Red · Çekimser

Approve · Reject · Abstain

03 · Alternatif Tavsiye

Önceden tanımlı seçeneklerden isteğe bağlı tavsiye. İlk tasarımda serbest metin yok.

Optional recommendation from predefined alternatives. No free text in the initial design.

## 08 · BASIT MODEL

SIMPLE MODEL

Tek kapı. Tek anahtar. Tek seçim.

One door. One key. One choice.

Bu bir teknik çözüm değil; çözmeye çalıştığımız güvenlik problemini anlatan bir metafordur.

This is not a technical solution. It is a metaphor for the security problem we are trying to solve.

Gerçek insan → Kimlik doğrulama → Tek kullanımlık anahtar → Kapı → Seçim → Toplu sonuç

Real human → Identity verification → Single-use key → Door → Choice → Aggregate result

## 09 · KAPI VE ODA

THE DOOR AND THE ROOM

Kapı kimin girmeye hakkı olduğunu bilir.

Oda içeri girenin kim olduğunu bilmez.

The door knows who is allowed in. The room does not know who entered.

Kimlik kapıdan önce vardır. Seçim kapıdan sonra vardır. İkisi bir daha buluşmamalıdır.

Identity exists before the door. Choice exists after the door. They must not meet again.

## 10 · MİMARİ VE GÜVEN SINIRLARI

ARCHITECTURE & TRUST BOUNDARIES

Dört katman. Açık güven sınırları.

- Kimlik / Uygunluk — kimlerin katılabileceğini bilir; seçimi bilmez
- Oy / Seçim — geçerli anonim anahtarı ve seçimi görür; kimliği bilmez
- Toplulaştırma / İfşa — kohort eşiği, sonuç bastırma ve alt-grup ifşasını zorlar
- Yönetişim / Çerçeveleme — karar sahibi, uygunluk kuralı, soru ve seçeneklerin iz kaydını tutar
- Aynı operatörün birden fazla katmanı kontrol etmesi veya katmanlar arası işbirliği ayrı bir risk olarak modellenir
- v0.1 anonimlik protokolü henüz seçilmedi

Four layers. Explicit trust boundaries.

- Identity — knows eligibility, never the choice
- Ballot — sees a valid anonymous token + choice, never identity
- Aggregation / Disclosure — enforces cohort thresholds, suppression and subgroup disclosure rules
- Governance / Framing — records provenance of decision owner, eligibility rule, question and options
- Common control or cross-layer collusion is an explicit risk
- The v0.1 anonymity protocol has not yet been selected

## 11 · GÜVENLIK VE MAHREMIYET HEDEFLERI

SECURITY AND PRIVACY TARGETS

Kanıtlanması gereken hedefler

- gerçek insan doğrulaması
- bağlamsal uygunluk
- tekil katılım
- kimlik-seçim bağlantısızlığı
- veri ihlali sonrası geçmiş seçimlerin yeniden eşleştirilememesi
- üstveri minimizasyonu
- müdahale edildiğinde tespit edilebilir / doğrulanabilir sonuç

Targets to be demonstrated

- real-human verification
- contextual eligibility
- unique participation
- identity-choice unlinkability
- post-compromise unlinkability of past choices
- metadata minimization
- tamper-evident / verifiable result

## 12 · HENÜZ KANITLANMADI

NOT YET PROVEN

Anonimlik bir slogan değil, kanıtlanması gereken bir özelliktir.

Anonymity is not a slogan. It is a property that must be demonstrated.

Henüz kanıtlanmadı: anonimlik garantisi · bağlantısızlık · ihlal sonrası bağlantısızlık · üretim güvenliği · baskıya dayanıklılık · küresel tekil insan doğrulaması · milyarlarca katılımcıya ölçek.

Not yet proven: anonymity guarantees · unlinkability · post-compromise unlinkability · production security · coercion resistance · global unique-human verification · scalability to billions.

## 13 · BAĞLAMA GÖRE Komite

CONTEXTUAL COMMITTEES

Örnek · Eğitim politikası

Example · Education policy

Uzman eğitimciler<br>
Öğrenciler<br>
Eğitim çağındaki çocukların aileleri<br>
Vatandaşlar

Education professionals<br>
Students<br>
Families of school-age children<br>
Citizens

Her grubun sinyali ayrı ayrı ve toplam olarak incelenebilir; bireysel seçimlerin kimlere ait olduğu bilinmeden.

Signals can be examined by group and in aggregate, without knowing which individual made which choice.

## 14 · KÜÇÜK GRUP İFŞA POLİTİKASI

SMALL-GROUP DISCLOSURE POLICY

Bu bir uç durum değil.

This is not an edge case.

Varsayılan kullanım bağlamı küçük ve orta büyüklükte Komitelerdir.

Small and medium committees are the default deployment context.

Yayın öncesi zorunlu tasarım kararları:

- minimum kohort eşiği
- eşik altında güvenli kapanma: sonuç yayımlanmaz
- alt-grup sonuç bastırma / toplulaştırma
- Anlama Kontrolü aynı ifşa kurallarına tabidir
- dış bilgiyle çıkarım riski varsa detay seviyesi azaltılır

Kesin eşikler henüz kilitlenmedi; bu politika olmadan yayına çıkış yok.

Required before launch: minimum cohort threshold · fail-closed suppression below threshold · subgroup aggregation/suppression · the Understanding Gate follows the same disclosure rules · reduce detail when outside knowledge creates inference risk. Exact thresholds are not locked yet; no launch without this policy.

## 15 · ÖLÇEK HEDEFI

SCALE TARGET

Bir ekipten insanlığın tamamına.

From one team to all of humanity.

Bir ekip → şirket → kurum → şehir → bölge → ülke → dünya nüfusu

A team → company → institution → city → region → country → global population

Bu mevcut performans iddiası değil; uzun vadeli north-star kapasite hedefidir. Ölçek hedefi, küçük-grup güvenlik politikasını gevşetmez.

This is not a current performance claim; it is a long-term north-star capacity target. Scale never relaxes the small-group safety policy.

## 16 · AÇIK ARAŞTIRMA PROBLEMI

OPEN RESEARCH PROBLEM

Küresel tekil insan doğrulaması + mahremiyet + sybil direnci: üçünün birlikte çözüldüğü varsayılmıyor.

Global unique-human verification + privacy + sybil resistance are not assumed to be solved together.

Komite’nin görevi bu problemi gizlemek değil; açıkça tanımlamak, araştırmak ve bağımsız incelemeye açmaktır.

Komite should not hide this problem. It should define it openly, research it and expose it to independent review.

## 17 · KULLANIM ALANLARI · I

USE CASES · I

İşletmeler

mikro → küçük → orta → büyük → holding → şirket grubu → çok uluslu şirket → şirket ekosistemi

Businesses · micro → small → medium → large → holding → corporate group → multinational → business ecosystem

Kamu kurumları ve yerel yönetimler

yerel yönetimler · belediyeler · il ve bölgesel kurumlar · merkezi kamu kurumları · bakanlıklar · ulusal düzey kurumlar

Public institutions and local government · local authorities · municipalities · provincial and regional institutions · central public institutions · ministries · national-level institutions

Yalnızca danışma ve karar desteği. Seçim, referandum veya bağlayıcı kamu oylaması değildir.

Consultation and decision support only. Never elections, referendums or binding public voting.

## 18 · KULLANIM ALANLARI · II

USE CASES · II

Kamu kuruluşları · eğitim · sağlık

yerel kamu birimi → okul → hastane → üniversite → kamu işletmesi → düzenleyici kurum → ulusal kamu ağı

Public institutions · education · healthcare

Dernekler · vakıflar · STK’lar · meslek örgütleri

yerel → bölgesel → ulusal → uluslararası → küresel ağ

Associations · foundations · NGOs · professional organizations · local → regional → national → international → global network

Kooperatifler · sendikalar · işveren örgütleri · federasyonlar · konfederasyonlar

Cooperatives · unions · employer organizations · federations · confederations

## 19 · KULLANIM ALANLARI · III

USE CASES · III

Bilim ve araştırma · kültür ve sanat · spor

ekip → laboratuvar → merkez → enstitü → akademi → ulusal kurum → uluslararası konsorsiyum

Science & research · culture & arts · sports

Yerel topluluklar · dijital topluluklar · sektörel yapılar

apartman → mahalle → kent konseyi → çevrim içi topluluk → açık kaynak ağı → sektör birliği → küresel konsorsiyum

Local communities · digital communities · industry structures

Çok paydaşlı Komiteler: kurumlar kararın çevresinde farklı grupları birlikte dinleyebilir.

Multi-stakeholder committees: institutions can listen to different groups around the decision itself.

## 20 · TEHDİT MODELİ ÖZETİ

THREAT MODEL OVERVIEW

Üst düzey tehdit aktörleri

- karar sahibi / süreç sahibi
- meraklı veya ele geçirilmiş operatör
- harici saldırgan / veri ihlali
- ağ gözlemcisi / zamanlama korelasyonu
- işbirliği yapan katılımcılar
- uygunluk / sybil saldırganı
- baskı / zorlama
- yönetişim / çerçeveleme manipülasyonu
- hukuki veya kurumsal zorlama

High-level threat actors

- decision owner / process owner
- curious or compromised operator
- external attacker / data breach
- network observer / timing correlation
- colluding participants
- eligibility / sybil attacker
- coercion
- governance / framing manipulation
- legal or institutional compulsion

## 21 · AÇIK KAYNAK GELIŞTIRME

OPEN-SOURCE DEVELOPMENT

“Bize güvenin.” yeterli değildir.

“Trust us.” is not enough.

Problem tanımı · tasarım ilkeleri · tehdit modeli · mimari kararları · güvenlik varsayımları · araştırma soruları · testler · başarısızlıklar · bağımsız incelemeler

Problem definition · design principles · threat model · architecture decisions · security assumptions · research questions · tests · failures · independent reviews

## 22 · KIMLERLE ÇALIŞMAK İSTIYORUZ?

WHO WE WANT TO WORK WITH

Kriptografi · Privacy Engineering · Application Security · Distributed Systems · Governance · Decision Science · UX · Accessibility · Hukuk · Veri Koruma

Cryptography · Privacy Engineering · Application Security · Distributed Systems · Governance · Decision Science · UX · Accessibility · Law · Data Protection

Aradığımız insanlar Komite’yi onaylayacak insanlar değil; nerede yanlış olduğunu gösterebilecek insanlar.

We are not looking for people who agree with Komite; we are looking for people capable of showing us where it is wrong.

## 23 · MEVCUT DURUM

CURRENT STATE

TANIMLANDI

problem · açık kaynak yönü · karar destek sınırı · anonim seçim hedefi · küresel ölçek hedefi

DEFINED · problem · open-source direction · decision-support boundary · anonymous-choice objective · global scale target

ARAŞTIRILIYOR

kimlik doğrulama · anonimlik mimarisi · güven sınırları · küçük grup politikası · yönetişim/çerçeveleme · doğrulanabilirlik tanımı · baskıya dayanıklılık kapsamı · üstveri · ölçek mimarisi

BEING RESEARCHED · identity verification · anonymity architecture · trust boundaries · small-group policy · governance/framing · definition of verifiability · coercion scope · metadata · scaling architecture

HENÜZ KANITLANMADI

anonimlik · bağlantısızlık · ihlal sonrası bağlantısızlık · üretim güvenliği · baskıya dayanıklılık · küresel tekillik · milyarlarca katılımcı

## 24 · İLK HEDEFLER

FIRST MILESTONES

01 Specification<br>
02 Independent Review I<br>
03 Threat Model<br>
04 Policy & Trust Boundaries<br>
05 Independent Review II<br>
06 Protocol Decision<br>
07 Security Review<br>
08 Reference Implementation<br>
09 Independent Audit<br>
10 Evidence<br>
11 Iterate ↻

Önce sınırları ve politikaları kilitle. Sonra protokol seç. İnceleme her aşamada tekrar eder.

Lock boundaries and policies first. Then choose the protocol. Review repeats at every stage.

## Açık çağrı / Open Call

Komite’nin açık araştırma sorularına, tasarımına ve bağımsız incelemesine katkıda bulunun. İletişim: Barbaros Hayrettin Bal, Bağımsız Geliştirici / Independent Developer — [barbaroshbal@gmail.com](mailto:barbaroshbal@gmail.com) · [LinkedIn](https://www.linkedin.com/in/barbarosb/).

Contribute to Komite’s open research questions, design and independent review. Contact: Barbaros Hayrettin Bal, Independent Developer — [barbaroshbal@gmail.com](mailto:barbaroshbal@gmail.com) · [LinkedIn](https://www.linkedin.com/in/barbarosb/).

## DAHA İYİ KARARLAR. DAHA İYİ GELECEK.

BETTER DECISIONS. BETTER FUTURE.

Komite’nin amacı daha fazla oylama yapmak değil; insanların, kurumların ve toplumların daha iyi bilgiyle daha iyi kararlar almasına yardımcı olmaktır.

Komite exists to help people, institutions and societies make better decisions with better information.

“Egemenlik kayıtsız şartsız milletindir.”

Mustafa Kemal Atatürk

“Sovereignty unconditionally belongs to the nation.”

Barbaros Hayrettin Bal · Bağımsız Geliştirici / Independent Developer · barbaroshbal@gmail.com · LinkedIn :https://www.linkedin.com/in/barbarosb/

## Teknik Belgeler / Technical Documents

Bu belgeler sunumdaki hedefleri teknik ayrıntı ve sınırlarla tamamlar. Dünya nüfusu ölçeği uzun vadeli bir araştırma hedefidir. Kamu/devlet seçimleri dahil hiçbir seçim, referandum veya bağlayıcı karar üretimi kapsamda değildir. Kurulum komutu yoktur; güvenlik açıklarını herkese açık iş kayıtlarına yazmayın.

These documents add technical detail and boundaries to the deck’s objectives. Global population scale is a long-term research target. All elections, including public/state elections, referendums and binding decisions are out of scope. There is no installation command; do not report security vulnerabilities in public issues.

- [Scope / Kapsam](SCOPE.md)
- [Research / Araştırma](RESEARCH.md)
- [Security / Güvenlik](SECURITY.md)
- [Governance / Yönetişim](GOVERNANCE.md)
- [Roadmap / Yol haritası](ROADMAP.md)
- [Decision Model / Karar modeli](docs/DECISION-MODEL.md)
- [Threat Model / Tehdit modeli](docs/THREAT-MODEL.md)
- [Architecture Directions / Mimari yönler](docs/ARCHITECTURE-DIRECTIONS.md)
- [Contributing / Katkı](CONTRIBUTING.md)
- [Release Checklist / Yayın kontrolü](docs/RELEASE-CHECKLIST.md)
- [Apache-2.0 License / Lisans](LICENSE)

Apache-2.0 lisansı değişmeden korunur; projenin desteklediği kullanım kapsamı lisansa ek kısıt getirmez.

The Apache-2.0 license remains unchanged; the project’s supported scope adds no license restriction.
