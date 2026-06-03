<p align="right">
<a href="./README.md">🇻🇳 Tiếng Việt</a> ·
<a href="./README.en.md">🇬🇧 English</a> ·
<a href="./README.pt-BR.md">🇧🇷 Português</a> ·
🇹🇷 Türkçe ·
<a href="./README.zh-CN.md">🇨🇳 简体中文</a> ·
<a href="./README.hi.md">🇮🇳 हिन्दी</a> ·
<a href="./README.bn.md">🇧🇩 বাংলা</a> ·
<a href="./README.ur.md">🇵🇰 اردو</a> ·
<a href="./README.ru.md">🇷🇺 Русский</a>
</p>

<h1 align="center">G-Labs Voice Studio</h1>
<p align="center">İçerik üreticileri için yapay zekâ ses stüdyosu</p>

<p align="center">
  <a href="https://drive.google.com/drive/u/0/folders/1BOH-3lF_rGu8QU4b07pt203a-WdOAb-G">
    <img alt="Download Windows" src="https://img.shields.io/badge/Download%20Windows-%F0%9F%92%BB-0078D6?style=for-the-badge&logo=windows&logoColor=white">
  </a>
  <a href="https://drive.google.com/drive/u/0/folders/1iEAUo5XOcr_3VmDoqIaiuq-zG8BLnxta">
    <img alt="Download macOS" src="https://img.shields.io/badge/Download%20macOS-%F0%9F%8D%8E-000000?style=for-the-badge&logo=apple&logoColor=white">
  </a>
</p>

<p align="center">
  <a href="https://duckmartians.info/voice">
    <img alt="Homepage" src="https://img.shields.io/badge/Homepage-Visit-0A66C2?style=flat-square&logo=google-chrome&logoColor=white">
  </a>
  <a href="https://discord.gg/munMZEBMw5">
    <img alt="Discord" src="https://img.shields.io/badge/dynamic/json?url=https://discord.com/api/guilds/1369302820037201981/widget.json&query=$.presence_count&label=Discord&color=5865F2&logo=discord&style=flat-square">
  </a>
</p>

**G-Labs Voice Studio**, çok dilli ses sentezi için bir masaüstü uygulamasıdır: kısa bir referans klipten ses klonlayın, öznitelikleriyle yeni sesler tasarlayın, çok karakterli diyaloglar yazın ve konuşmayı metne dönüştürün. Koyu temalı arayüz, modeller doğrudan makinenizde çalışır — model bir kez indirildikten sonra hiçbir ses veya metin cihazdan dışarı çıkmaz.

<p align="center">
  <a href="https://duckmartians.info/voice">
    <img alt="G-Labs Voice Studio UI" width="900" src="https://github.com/user-attachments/assets/d7a08f20-3aee-43ed-bbba-b80997720fdb" />
  </a>
</p>

---

## Özellikler

- **🔊 Ses Klonlama** — 5–10 saniyelik bir referans klip verin; uygulama o sesle istediğiniz metni okur.
- **🎛️ Metinden Sese / Ses Tasarımı** — bir sesi öznitelikleriyle tarif edin (cinsiyet, yaş, perde, stil, aksan); referans sese gerek yok.
- **💬 Çok Sesli Diyalog** — `<Ad>: replik` sözdizimiyle çok karakterli bir senaryo yazın ve her karaktere kütüphaneden bir ses atayın.
- **📝 Sesten Metne (ASR)** — ses/video dosyalarını yazıya dökün. MP3, WAV, M4A, FLAC, MP4, MOV destekler…
- **🗂 Ses Kütüphanesi + 30 hazır ses** — uygulama 30 kullanıma hazır sesle gelir (erkek/kadın, farklı tonlarda). Kendi seslerinizi de kaydedebilirsiniz. Bir sesi ⭐ ile favoriye alarak en üste sabitleyin ve paylaşmak için taşınabilir `.vcp` dosyaları olarak **yedekleyip geri yükleyin**.
- **🎚 Hız kontrolü + hızı koruyan dışa aktarım** — dalga formunun altından önizleme hızını değiştirin; dışa aktarılan dosya tam olarak o hızda çalar (perde korunur).
- **📄 Altyazı (SRT) dışa aktarımı** — tek birleştirilmiş dosya olarak dışa aktarırken `.srt` otomatik olarak yanında oluşturulur, video düzenleme için hazırdır.
- **🔤 Kişisel telaffuz sözlüğü** — `100%`, `25°C`, `m²` ile karşılaştınız mı? Telaffuzu bir kez yazın, uygulama bir dahaki sefere hatırlasın (çıkış diline göre).
- **✨ Yapay zekâ örnek metin önerisi** — Whisper, referans klibi otomatik olarak yazıya döker, böylece sıfırdan yeniden yazmak zorunda kalmazsınız (yine de üretmeden önce gözden geçirin).
- **⬇ Satır başına indirme** — senaryo tablosundaki her satırın kendi indirme düğmesi vardır — tüm partinin bitmesini beklemenize gerek yok.
- **600+ dil desteği** — 600'den fazla dilde konuşma (Vietnamca, İngilizce, Çince, Japonca, Korece, Fransızca, Almanca, İspanyolca ve birçok azınlık dili).
- **Toplu işlem** — `.txt` veya `.srt` senaryoları içe aktarın, partileri çalıştırın, zaman damgalarını koruyarak sesi dışa aktarın.
- **Akıllı GPU uyumluluk kontrolü** — GPU'nuz hızlandırılmış çekirdekleri çalıştıramıyorsa, uygulama **otomatik olarak çok çekirdekli CPU'ya geri döner** ve bunu açıkça size bildirir; CUDA hatasıyla çökmez.
- **9 dilli arayüz** — Tiếng Việt, English, Português, Türkçe, 简体中文, हिन्दी, বাংলা, اردو, Русский.

---

## 🆕 v1.0.7'de yenilikler

- **🔊 Ses Klonlama sekmesi, daha basit olacak şekilde yenilendi** — kütüphane iki net sütuna ayrıldı (**Hazır sesler** / **Sesleriniz**) ve metin kutusu tek satıra indirildi. Klonlamadan sonra uygulama dinlemenizi önerir, ardından sesi kaydetmek isteyip istemediğinizi sorar — kaydetmek tek dokunuş. 30 saniyeden uzun örnek ses, daha temiz bir klonlama için bir sessizlik noktasında **otomatik kırpılır**.
- **🎛 Daha derli toplu bir Metinden Sese sekmesi** — "Ses kütüphanesi" ve "Ses tasarımı" **tek bir çerçevede** birleştirildi; **Kayıtlı ses kullan** ↔ **Rastgele ses** arasında geçiş yapın, karmaşa yok.
- **▶ Hazır sesleri önizleyin** — kütüphanedeki herhangi bir hazır sesin yanındaki ▶ düğmesine tıklayarak kullanmadan önce dinleyin.
- **⭐ Favoriler her yerde eşitlenir** — bir sekmede bir sese yıldız verin, diğer sekmeler de görür.
- **🐛 Hız denetiminin sesi bozması / dışa aktarmanın başarısız olması düzeltildi** — önizleme çubuğundaki hız denetimi kaldırıldı (bozulmaya ve dışa aktarma hatasına neden oluyordu). Daha hızlı/yavaş okumak için *Gelişmiş ayarlar* altındaki **Okuma hızı** kaydırıcısını kullanın — doğal ses, hatasız.
- **✨ Küçük dokunuşlar** — cümleler arası varsayılan boşluk artık daha kısa (100ms), daha akıcı; silme düğmeleri tutarlı görünüyor; birçok yerde daha derli toplu arayüz.
- **🎙 Konuşma → Metin sekmesi: tanıma modelini seçin** — makinenize göre küçükten büyüğe (Tiny → Turbo) seçin: zayıf bilgisayarlar hız için küçük modeli, güçlüler doğruluk için büyük modeli seçer (her biri **gereken VRAM'i** gösterir). Varsayılan model kurulumdan hemen sonra hazır; diğerleri tek dokunuşla iner ve **bilgisayarınıza kaydedilir**, sonraki sefer çevrimdışı çalışır.
- **🌍 Konuşulan dili seçin** — hangi dilin konuşulduğunu belirtmek (~100 dil destekli) doğruluğu artırır ve ortada dil karışmasını önler; ayrıca zor kısımlarda hata/tekrarı azaltan iyileştirmeler.

---

## 🆕 v1.0.6'da yenilikler

- **🔗 Webhook API (yeni)** — yerel REST sunucusu n8n, Zapier, Python/cURL veya herhangi bir HTTP istemcisinin programatik olarak ses üretimini tetiklemesine olanak tanır. Uygulama içinde ses + dil seçici panelleri (çift tıklayarak kopyala), `xxxx***xxxx` maskelenmiş API anahtarı, otomatik başlatma, gerçek zamanlı istek günlüğü.
- **🚀 Çok daha hızlı dışa aktarma + gerçek ilerleme çubuğu** — birleştirme ve zaman germe CPU çekirdeklerinde paralel çalışır; 50 dakikalık bir proje dakikalar yerine onlarca saniyede dışa aktarılır. Satır içi ilerleme çubuğu 0→100% pürüzsüz ilerler, gerçek **Durdur** düğmesi ortadan iptal edebilir.
- **🧹 Daha sade Ses Klonlama + Konuşma-metin sekmeleri** — Klonlama, Metin-konuşma sekmesi ile çakışan düğmeleri kaldırdı. ASR otomatik olarak kısa parçaları tam cümlelere birleştirir, orijinal zaman çizelgesini korur.
- **💾 Sekmeler arası ayar senkronizasyonu** — *Eşzamanlı cümleler* (batch size) artık üç üretim sekmesi + Webhook eşzamanlılık limiti arasında paylaşılır; herhangi bir yerde değiştirin, geri kalanı otomatik güncellenir. Klonlama / Metin-konuşma sekmeleri yeniden başlatmalarda son seçilen ön ayarı hatırlar.
- **🐛 Birçok hata düzeltmesi** — oturum zaman aşımı sonrası dışa aktarma çökmesi (`AttributeError: NoneType`), ağ kesintisi nedeniyle safetensors eksik kaldığında yanlış "model indirildi" durumu, klonlama gerçekten bitmeden "Sesi kaydet" düğmesinin etkinleşmesi.

---

## 🆕 v1.0.5'te yenilikler

- **🎚 Profesyonel ses ustalama (yeni)** — ses parçalarınızın stüdyo kalitesinde duyulması için 6 işleme modundan birini seçin (Yayın / Sinema / Podcast / Sıcak / Parlak / Ham). 3 üretim sekmesinin (Ses Klonlama / Metinden Sese / Çok Sesli Diyalog) hepsinde kullanılabilir — bir sekmede değiştirin, diğerleri senkron kalır.
- **🌐 Çince / Hintçe / Arapça / Urduca için daha iyi cümle bölme** — bu diller eskiden tek satırda eziliyordu; şimdi cümleler her yazı sisteminin noktalama işaretlerine göre doğru biçimde bölünüyor.
- **🧠 Boştayken belleği otomatik serbest bırakma** — uygulama 5 dakika (varsayılan) kullanılmazsa, makinenizi rahatlatmak için yapay zekâ modelini otomatik olarak bellekten kaldırır. Zaman aşımını Ortam Ayarları sekmesinden değiştirebilir veya devre dışı bırakabilirsiniz.
- **⚙ Aynı anda üretim ve yazıya dökme sırasında daha kararlı** — düşük bellekli makinelerde bu işlem ortada çökerdi; artık uygulama bunu otomatik olarak yönetiyor.

> ⚠️ **Dışa aktarılan seste küçük değişiklik:** Varsayılan **📻 Yayın** ön ayarı + **Cümleler arası ses seviyesini eşitle** seçeneği, v1.0.5'teki ses dosyalarını v1.0.4'e göre **daha yüksek ve daha dolgun** duyurur. Eski davranışa dönmek için herhangi bir üretim sekmesini açın → **Ses ustalama** başlığını genişletin → **🔇 Ham** seçin ve **Cümleler arası ses seviyesini eşitle** kutusunu kaldırın.

---

## 🆕 v1.0.4'te yenilikler

- **💬 Çok Sesli Diyalog sekmesi (yeni)** — çok karakterli senaryolar yazın, her konuşmacı için bir ses. Çalışan bir örnek için **📋 Örnek diyalog**'a tıklayın.
- **🗂 30 hazır ses dahil** — kutudan çıkar çıkmaz kullanıma hazır, önce bir örnek kaydetmeye gerek yok.
- **⭐ Favori yıldızı** — bir sesin yanındaki ☆ işaretine tıklayarak onu kütüphanenin en üstüne sabitleyin.
- **🎚 Oynatıcıda hız kaydırıcısı** — 0.5x → 2x aralığında önizleme yapın, dışa aktarım da tam o hızı korur.
- **📄 Otomatik SRT dışa aktarımı** — birleştirilmiş dosya olarak dışa aktarırken uygulama, `.wav` dosyasının yanına eşleşen bir `.srt` bırakır (devre dışı bırakılabilir).
- **🔤 Özel karakterler için telaffuz sözlüğü** — "100%"i artık manuel olarak "yüzde yüz" diye yazmak zorunda kalmayacaksınız: telaffuzu bir kez yazın, uygulama sonsuza dek hatırlasın.
- **🌐 9 arayüz dili** — Vietnamca / İngilizce'nin üzerine Português, Türkçe, 简体中文, हिन्दी, বাংলা, اردو, Русский eklendi.
- **⏳ Satır başına geçen süre** — hangi satırın şu anda üretildiğini ve ne kadar süredir çalıştığını bir bakışta görün.
- **🌍 Çıkış dili açıkça seçilmelidir** — yanlış telaffuzları önlemek için "Otomatik" seçeneği kaldırıldı.

---

## Kurulum

| Platform | Dosya | Boyut |
|---|---|---|
| Windows x64 | `GLabsVoiceStudio-v1.0.7-win.zip` | ~3 GB |
| macOS Apple Silicon | `GLabsVoiceStudio-v1.0.7-arm64.dmg` | ~2 GB |

### Windows (taşınabilir, kuruluma gerek yok)

1. `GLabsVoiceStudio-v1.0.7-win.zip` dosyasını indirin.
2. Herhangi bir klasöre çıkarın (sürücüde en az 10 GB boş alan olmalı).
3. Çıkarılan klasörü açın ve `GLabsVoiceStudio.exe` dosyasına çift tıklayın.

> Masaüstü kısayolu mu istiyorsunuz? `GLabsVoiceStudio.exe` üzerine sağ tıklayın → *Gönder* → *Masaüstü (kısayol oluştur)*.

> **⏳ İlk açılış 30–60 saniye sürebilir (açılış ekranı ~%90 civarında duraklayabilir) — lütfen bekleyin, kapatmayın.** Windows'un uygulamayı ve GPU dosyalarını taraması gerekir (otomatik bir güvenlik adımıdır, yalnızca ilk seferinde yavaştır). İkinci açılıştan itibaren uygulama hızlıca açılır.

### 🍎 macOS Apple Silicon

1. Resmi dağıtımdan **`GLabsVoiceStudio-v1.0.7-arm64.dmg`** dosyasını indirin.
2. Açmak için `.dmg` dosyasına çift tıklayın.
3. **G-Labs Voice Studio** simgesini **Applications** klasörüne sürükleyin.
4. **Applications**'ı açın, **G-Labs Voice Studio** üzerine **sağ tıklayın** → **Aç**'ı seçin.

> ⚠️ **İlk açılış:** macOS *"Tanınmayan bir geliştiriciden gelen uygulama"* uyarısı gösterebilir. Uygulamaya sağ tıklayın → **Aç** → iletişim kutusunda tekrar **Aç**'a tıklayın. Yalnızca bir kez gereklidir.

> 📁 **Çıktı dosyaları** (ses, senaryolar) varsayılan olarak `~/Documents/G-Labs Voice Studio/output/` konumuna kaydedilir.

> **⏳ İlk açılış 30–60 saniye sürebilir (açılış ekranı ~%90 civarında duraklayabilir) — lütfen bekleyin, kapatmayın.** macOS ilk açılışta tam bir güvenlik kontrolü yapar. İkinci açılıştan itibaren uygulama hızlıca açılır.

#### 🍎 macOS'ta *"Uygulama hasarlı"* hatasını giderme

İnternetten bir `.dmg` indirdiğinizde, macOS dosyaya otomatik olarak bir **karantina bayrağı** ekler. Eğer uygulama Apple tarafından noter onaylı değilse, Gatekeeper onu engeller ve *"Uygulama hasarlı ve açılamıyor"* uyarısı gösterebilir.

**Yöntem 1: Sağ tık → Aç** *(önerilen)*

1. **Applications** klasörünü açın.
2. *G-Labs Voice Studio* üzerine **sağ tıklayın** → **Aç**.
3. Uyarı iletişim kutusunda tekrar **Aç**'a tıklayın.

**Yöntem 2: Terminal'i kullanın** (yöntem 1 hâlâ hata veriyorsa)

**Terminal**'i açın (Launchpad → Diğer → Terminal), aşağıdaki komutu yapıştırın ve Enter'a basın:

```bash
xattr -cr "/Applications/G-Labs Voice Studio.app"
```

Bu komut, uygulama paketinden tüm genişletilmiş öznitelikleri (karantina bayrağı dahil) temizler. Çalıştırdıktan sonra uygulamayı normal şekilde açın. Bunu indirilen her sürüm için yalnızca **bir kez** yapmanız yeterlidir.

**Yöntem 3: Sistem Ayarları → Gizlilik ve Güvenlik**

1. Uygulamayı normal şekilde açmaya çalışın (engellenecektir).
2. **Sistem Ayarları** → **Gizlilik ve Güvenlik**'i açın.
3. En alta inin, *"G-Labs Voice Studio engellendi…"* uyarısını bulun → **Yine de Aç**'a tıklayın.
4. Touch ID veya yönetici şifresiyle onaylayın.

---

## Başlangıç

### Adım 1 — İlk açılış (bir defalık kurulum)

1. Uygulamayı açın — hoş geldiniz ekranı 9 arayüz dili sunar. İstediğinizi seçin.
2. **Oturum açın** — sol kenar çubuğundaki ⚙️ dişli simgesine tıklayın → *Lisans* sekmesi → **"Google ile oturum aç"**.
3. **Yapay zekâ modelini indirin** — *Ortam* sekmesine geçin (veya uygulamanın sizi yönlendirmesine izin verin) → **"Modeli indir"** düğmesine tıklayın. Birkaç GB; bitmesini bekleyin.
4. Ayarları kapatın.

> 💡 Arayüz dilini daha sonra değiştirmek için: Ortam Ayarları → Arayüz dili.

### Adım 2 — Ses Klonlama 🔊

Örnek bir kayıttan ses klonlayın.

1. **🔊 Ses Klonlama** sekmesini açın.
2. Sekmenin üst kısmından **çıkış dili**ni seçin (örn. Vietnamca, İngilizce…).
3. *Örnek ses* alanında **"Seç..."** düğmesine tıklayın ve bir örnek klip seçin (5–10 saniye, net ses, az arka plan gürültüsü).
4. **Zorunlu:** *Örnek metin*'i girin — örnek sesin tam transkripti (doğru noktalama ve yazım).
    > 💡 **"✨ Yapay zekâ önerisi"** düğmesine tıklayın, Whisper sizin için yazıya döksün — yine de üretmeden önce gözden geçirin.
5. Hedef metni *Metin içeriği* alanına yapıştırın (veya `.txt` / `.srt` dosyasından yüklemek için **"📂 İçe aktar (.txt, .srt)"** düğmesine tıklayın).
6. **"📋 Tabloya ekle"** düğmesine tıklayın — uygulama metninizi ayrı cümlelere böler.
7. (İsteğe bağlı) Telaffuz sözlüğünü gözden geçirmek için **🔤 Telaffuz**'a tıklayın — metniniz özel karakter içeriyorsa (örn. `100%`), uygulama bunları nasıl okuyacağını size soracaktır.
8. **"▶ İşlemi başlat"** düğmesine tıklayın → örnek transkripti doğrulamak için bir onay iletişim kutusu açılır → çalıştırmak için onaylayın.
9. Bittiğinde **"💾 Sesi dışa aktar"** düğmesine tıklayın (eşlik eden `.srt` ile tek birleştirilmiş dosya) veya yalnızca o satırı indirmek için bir satırın üzerindeki **⬇** simgesini kullanın.

### Adım 3 — Metinden Sese 🎛️

Öznitelik açıklamalarından yeni bir ses oluşturun — örneğe gerek yok.

1. **🎛️ Metinden Sese** sekmesini açın.
2. **Çıkış dili**ni seçin.
3. **Ses Tasarımı** panelini açın ve şunları seçin: *Cinsiyet*, *Yaş*, *Perde*, *Stil*, *Aksan*.
    > 💡 **Ses Kütüphanesi**'nden kaydedilmiş bir sesi yeniden kullanmak mı istiyorsunuz? Doğrudan açılır listeden seçin — uygulama ilk satırdaki ısınma adımını atlar ve doğrudan 1. satırdan başlar.
4. Metninizi yapıştırın ve **"📋 Tabloya ekle"** düğmesine tıklayın.
5. **"▶ İşlemi başlat"** düğmesine tıklayın.
6. Üretimden sonra: tutmak istediğiniz satıra tablo üzerinde tıklayın → daha sonra yeniden kullanmak için *Ses Kütüphanesi* panelinde **"💾 Kaydet"** düğmesine tıklayın.
7. Sonucu kaydetmek için **"💾 Sesi dışa aktar"** düğmesine tıklayın.

### Adım 4 — Çok Sesli Diyalog 💬 *(yeni)*

Her konuşmacı için bir ses kullanarak çok karakterli diyalog sesi üretin — podcast, sesli drama ve röportaj tarzı videolar için mükemmeldir.

1. **💬 Çok Sesli Diyalog** sekmesini açın.
2. **Çıkış dili**ni seçin.
3. Çalışan bir örnek görmek için (metin alanının sağ üstündeki) **📋 Örnek diyalog** düğmesine tıklayın — uygulama örneği yapıştırır ve ayrıntı düzenleyicisini açar.
4. Senaryonuzu şu sözdizimini kullanarak yazın:
    ```
    <Host>: Welcome everyone, today we have a very special conversation lined up.
    <Anna>: Hi, I'm really glad to be part of the show today.
    <Ben>: Same here, thanks for having us on. What's the topic?
    ```
    > 💡 Konuşmacı adı `< >` içine, ardından `:` ve replik gelir. İki nokta isteğe bağlıdır — `<Anna> Hi there` de çalışır. Adlar büyük/küçük harf duyarsızdır.
5. **"🎭 Diyaloğu ayrıştır"** düğmesine tıklayın — uygulama senaryoyu satırlara böler ve "Karakter" sütununu gösterir.
6. **Ses atamaları** paneli otomatik olarak açılır — her konuşmacı için kütüphaneden bir ses seçin.
7. (İsteğe bağlı — *yeni*) Her konuşmacı satırının, ses seçicinin hemen altında kendi **Hız** kaydırıcısı vardır (0.5x → 2x). Konuşmacılar aynı parti içinde bağımsız tempolarda çalışabilir — örn. sunucu yavaş konuşur, konuk daha hızlı.
8. **"▶ İşlemi başlat"** düğmesine tıklayın — her satır, atanan konuşmacının sesiyle okunur.
9. Sonucu kaydetmek için **"💾 Sesi dışa aktar"** düğmesine tıklayın (eşleşen bir `.srt` dahildir).

### Adım 5 — Sesten Metne 📝

Mevcut bir ses/video dosyasından konuşmayı yazıya dökün.

1. **📝 Sesten Metne** sekmesini açın.
2. **"Seç..."** düğmesine tıklayın ve bir ses/video dosyası seçin (MP3, WAV, M4A, FLAC, MP4, MOV…).
3. **"▶ Çıkarmayı başlat"** düğmesine tıklayın — uygulama sesi analiz eder, konuşma bölümlerine göre parçalara ayırır ve her birini yazıya döker.
4. Sonuçlar, cümle başına zaman damgalarıyla birlikte bir tabloda görünür. Bunları doğrudan düzenleyebilirsiniz.
5. `.txt` (düz metin) veya `.srt` (zaman damgalarıyla, altyazılar için hazır) olarak kaydetmek için **"💾 Sonucu dışa aktar"** düğmesine tıklayın.

---

## 💡 İleri kullanıcı ipuçları

### Ses ustalama *(yeni)*
- Üç üretim sekmesinin (Ses Klonlama / Metinden Sese / Çok Sesli Diyalog) hepsinde formun ortasında bir **Ses ustalama** açılır bölümü bulunur.
- 6 yerleşik ön ayar:
  - 📻 **Yayın** *(varsayılan)* — radyo/podcast standardı, sıcak ve sıkıştırılmış.
  - 🎬 **Sinema** — geniş yankı, hafif sıkıştırma, sinema kalitesi.
  - 🎙️ **Podcast** — yakın mikrofon, yoğun sıkıştırma, yankı yok.
  - 🔇 **Ham** — model çıkışı olduğu gibi, işleme yok.
  - ☀️ **Sıcak** — alt-orta frekanslar yükseltilmiş, samimi his.
  - ✨ **Parlak** — net tiz, ferah his.
- Bir sekmede ön ayarı değiştirin → diğer ikisi otomatik olarak senkronize olur. Önceki sürümle (v1.0.4) tam olarak aynı çıktıyı elde etmek için: **🔇 Ham** seçin ve **Cümleler arası ses seviyesini eşitle** kutusunu kaldırın.

### Boştayken belleği otomatik serbest bırakma *(yeni)*
- Varsayılan: uygulama **5 dakika** kullanılmazsa, sistem kaynaklarını serbest bırakmak için yapay zekâ modeli VRAM/RAM'den otomatik olarak kaldırılır.
- Bir sonraki üretimde model yeniden yüklenir (~30-60 sn).
- Zaman aşımını ayarlamak için **Ortam Ayarları** sekmesi → **VRAM'i otomatik serbest bırak** bölümüne gidin (0 = devre dışı, 1-120 dakika).

### Ses Kütüphanesi ve favori yıldızı
- Kütüphanedeki her sesin satır başında bir ☆ bulunur. Üzerine tıkladığınızda → ★'a dönüşür → o ses listenin en üstüne çıkar (ve bir sonraki sefere de orada kalır).
- Favoriden çıkarmak için tekrar ★'a tıklayın.
- 30 hazır sesin (Achernar, Aoede, Kore, Puck…) tümü de favoriye eklenebilir.

### Telaffuz sözlüğü
- Metniniz `%`, `$`, `°C`, `m²`, marka adları… içerdiğinde üretmeden önce **🔤 Telaffuz** düğmesine tıklayın.
- Uygulama bir simgeyi ilk gördüğünde nasıl okunacağını sorar (örn. `%` → ` yüzde`).
- Her simgenin yalnızca **bir kez** yazılması gerekir — uygulama bunu çıkış diline göre hatırlar. Bir sonraki sefere otomatik olarak uygulanır.
- Aynı simge farklı dillerde ayrı telaffuzlar tutar (örn. Vietnamca ile İngilizce).

### Oynatma hızı + dışa aktarım
- Ses üretildikten sonra, dalga formunun altındaki çubukta bir **hız açılır listesi** bulunur (0.5x → 2x, kademeli).
- Hızı değiştirin → önizleme oynatıcıda hemen güncellenir.
- Dışa aktarılan dosya tam olarak o hızı korur ve **perde de korunur** (sincap efekti yok — zaman germe kullanır).

### SRT dışa aktarımı
- *Dışa aktarma ayarları* panelinde **"Altyazıyı da dışa aktar (.srt)"** varsayılan olarak açıktır.
- Tek birleştirilmiş bir dosya olarak dışa aktardığınızda, uygulama `name.wav`'ın yanına `name.srt` oluşturur.
- SRT'deki zaman damgaları, hız ayarından sonra gerçek satır başına süreyi yansıtır.

---

## Sistem Gereksinimleri

|   | Minimum | Önerilen |
|---|---|---|
| **İşletim sistemi** | Windows 10 (64-bit), macOS 12 Monterey | Windows 11, macOS 13 veya daha yenisi |
| **RAM** | 8 GB | 16 GB veya daha fazla |
| **VRAM (GPU)** | 4 GB (TTS otomatik olarak CPU'ya geçer) | 8 GB+ (NVIDIA RTX 3060 veya üzeri) |
| **Disk** | 10 GB boş alan (model + önbellek) | 20 GB+ SSD |
| **GPU** | İsteğe bağlı — CPU çalışır | NVIDIA CUDA · Apple Silicon (Metal) |

> 💡 **İpucu:** ≤ 8 GB VRAM'li GPU'larda, uygulama yazıya dökme sırasında TTS'i otomatik olarak CPU'ya devreder — yapılandırma gerekmez. Adanmış bir GPU gerekli değildir; tüm hat CPU üzerinde çalışır (sadece daha yavaş).

### Platform notları

**Windows x64**
- **NVIDIA GPU, RTX 20 serisi veya daha yenisi** (işlem yeteneği ≥ 7.0 — RTX 20/30/40/50, Titan V, Tesla V100…). GTX 10 serisi (GTX 1060/1070/1080) gibi daha eski kartlar **hızlandırılmış çekirdekleri çalıştıramaz**; uygulama bunu algılar ve otomatik olarak CPU'ya geri döner.
- CUDA 12.8 destekli NVIDIA sürücüsü.

**macOS**
- Yalnızca **Apple Silicon** (M1/M2/M3/M4…) desteklenir — Apple'ın Metal hızlandırmasını kullanır. Intel Mac'ler desteklenmez.

> Uyumlu GPU'su olmayan makineler **otomatik olarak çok çekirdekli CPU'da çalışır** (uygulama PyTorch / BLAS iş parçacığı sayılarını fiziksel çekirdek sayınıza göre ayarlar). GPU'dan kabaca 5–10× daha yavaştır ama yine de kısa seslendirme işleri için kullanılabilir.

---

© 2026 Duck Martians AI Labs. All rights reserved.
