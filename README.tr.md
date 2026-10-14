<h1 align="center">G-Labs Voice Studio</h1>

<p align="center"><b>Kendi bilgisayarınızda çalışan masaüstü yapay zekâ ses uygulaması - birkaç saniyelik sesten ses klonlayın, 600'den fazla dilde metin okutun, çok sesli diyalog oluşturun, ses/videoyu altyazıya dönüştürün ve altyazıları yapay zekâyla çevirin.</b></p>

<p align="center">
  <a href="README.md">Tiếng Việt</a> ·
  <a href="README.en.md">English</a> ·
  <a href="README.pt-BR.md">Português</a> ·
  <b>Türkçe</b> ·
  <a href="README.zh-CN.md">简体中文</a> ·
  <a href="README.hi.md">हिन्दी</a> ·
  <a href="README.bn.md">বাংলা</a> ·
  <a href="README.ur.md">اردو</a> ·
  <a href="README.ru.md">Русский</a>
</p>

<p align="center">
  <a href="https://drive.google.com/drive/u/0/folders/1BOH-3lF_rGu8QU4b07pt203a-WdOAb-G"><img alt="Windows için indir" src="https://img.shields.io/badge/%C4%B0ndir-Windows-0078D6?style=for-the-badge&logo=windows&logoColor=white"></a>&nbsp;
  <a href="https://drive.google.com/drive/u/0/folders/1iEAUo5XOcr_3VmDoqIaiuq-zG8BLnxta"><img alt="macOS (Apple Silicon) için indir" src="https://img.shields.io/badge/%C4%B0ndir-macOS%20Apple%20Silicon-000000?style=for-the-badge&logo=apple&logoColor=white"></a>&nbsp;
  <a href="https://www.youtube.com/watch?v=3J8GdUEfFlI"><img alt="YouTube'da eğitim videosu" src="https://img.shields.io/badge/YouTube-E%C4%9Fitim%20videosu-FF0000?style=for-the-badge&logo=youtube&logoColor=white"></a>
</p>

---

## Kurulum

### Adım 1 - Bilgisayarınıza uygun sürümü seçin

Sürümler resmi Google Drive klasörlerinden dağıtılır:

| Bilgisayarınız | Google Drive | Not |
|---|---|---|
| 🪟 **Windows 10/11 (64-bit)** | [Windows](https://drive.google.com/drive/u/0/folders/1BOH-3lF_rGu8QU4b07pt203a-WdOAb-G) | Bir `.zip` - çıkarın ve çalıştırın, kurulum yok |
| 🍎 **Apple çipli Mac (M1/M2/M3/M4…)** | [macOS Apple Silicon](https://drive.google.com/drive/u/0/folders/1iEAUo5XOcr_3VmDoqIaiuq-zG8BLnxta) | Bir `.dmg`, macOS 12 veya üzeri gerekir |

> **Intel Mac desteklenmez** - yalnızca Apple Silicon sürümü vardır. Mac'inizin çipinden emin değil misiniz?  menüsü → **Bu Mac Hakkında**: **Çip** satırında "Apple M…" yazıyorsa çalışır; **İşlemci** satırında "Intel…" yazıyorsa çalışmaz.

### Adım 2 - Kurulum

<details open>
<summary><b>🪟 Windows'ta</b></summary>

1. Windows `.zip` dosyasını indirin (ör. `G-Labs-Voice-Studio-v2.0.3-win.zip`) ve herhangi bir klasöre **çıkarın** - sürücüde en az 10 GB boş alan olmalı (sonradan indirilen yapay zekâ modelleri birkaç GB yer kaplar).
2. Çıkarılan klasörü açın ve **`G-Labs-Voice-Studio.exe`** dosyasını çalıştırın (exe, bu klasörde ihtiyaç duyduğu dosyaların yanında durur - bunları taşımayın veya silmeyin).
3. **"Windows bilgisayarınızı korudu"** (SmartScreen) çıkarsa: **Ek bilgi** → **Yine de çalıştır**'a tıklayın. *(Uygulama Microsoft sertifikasıyla imzalı olmadığı için Windows uyarır - virüs değildir.)*
4. **Kısayol oluşturun:** `G-Labs-Voice-Studio.exe` üzerine sağ tıklayın → **Gönder** → **Masaüstü (kısayol oluştur)**; sonraki seferlerde hızlıca açarsınız.

> ⏳ **İlk açılış 30-60 saniye sürebilir** (açılış ekranı bir süre durur), çünkü Windows uygulamayı ve grafik kitaplıklarını güvenlik taramasından geçirir. Bekleyin, kapatmayın - sonraki açılışlar daha hızlıdır.

</details>

<details open>
<summary><b>🍎 macOS'ta</b></summary>

1. İndirilen **`.dmg`** dosyasını açın ve **G-Labs Voice Studio simgesini Uygulamalar klasörüne sürükleyin**.
2. **Uygulamalar**'da **G-Labs Voice Studio**'ya **sağ tıklayın** (veya Control ile tıklayın) → **Aç** → onay penceresinde yeniden **Aç**. *(Uygulama Apple tarafından onaylanmadığı için **ilk seferde** bu şekilde açılır; sonrasında normal açılır.)*
3. macOS uygulamanın **"hasarlı / açılamıyor"** olduğunu söylerse veya Aç düğmesi yoksa **Terminal**'i açın, şunu yapıştırıp Enter'a basın:
   ```bash
   xattr -dr com.apple.quarantine "/Applications/G-Labs Voice Studio.app"
   ```
   Ardından uygulamayı yeniden açın. Alternatif: **Sistem Ayarları → Gizlilik ve Güvenlik**, en alta kaydırın ve G-Labs Voice Studio'nun engellendiğini bildiren satırın yanındaki **Yine de Aç**'a tıklayın.

> ⏳ **İlk açılış 30-60 saniye sürebilir**, çünkü macOS uygulamanın tamamını güvenlik denetiminden geçirir. Sonraki açılışlar daha hızlıdır.

</details>

### Adım 3 - Giriş yapın ve plan seçin

Uygulamanın lisansınızı doğrulayabilmesi için **Google ile giriş yapmanız gerekir** (Ayarlar ⚙️ → **Lisanslı hesaplar** sekmesi → **Google ile giriş yap**). Bir hesap **aynı anda tek bilgisayarda** çalışır - başka bir cihazda giriş yapmak eski cihazdaki oturumu sonlandırır.

| Plan | Fiyat | İçerik |
|---|---|---|
| **Deneme** | Ücretsiz | Üretim başına sınırlı satır (varsayılan 1) - satın almadan önce bilgisayarınızın iyi çalıştığını görmeye yeter |
| **Studio planı** | 1 ay $5 · 6 ay $25 · 1 yıl $50 (VietQR ile 100.000đ / 500.000đ / 1.000.000đ) | Sınırsız satır, **Oluşturma kuyruğu**, **Çeviri** sekmesi, **Webhook API** |

- Uygulama içinden satın alın (Ayarlar → **Lisanslı hesaplar**): **VietQR banka havalesi**, **PayPal** (uluslararası kart) veya **USDT**. Planlar süre bazlıdır, otomatik yenilenmez ve giriş yaptığınız Google hesabında etkinleşir.
- Studio planı yalnızca Voice Studio'ya aittir ve G-Labs Studio Plus/Max'tan **ayrıdır**.
- Ödemeden sonraki ilk **24 saat** içinde iade mümkündür - bkz. [İade politikası](https://duckspace.net/refunds.html#en). Bilgisayarınızın kaldırabildiğinden emin olmak için önce ücretsiz denemeyi çalıştırın.

---

## İlk çalıştırma

1. **Uygulamayı açın ve karşılama ekranında arayüz dilini seçin** (daha sonra Ayarlar'dan değiştirebilirsiniz).
2. **Google ile giriş yapın** - Ayarlar ⚙️ → **Lisanslı hesaplar** → **Google ile giriş yap**.
3. **Ses modelini indirin** - **Model Yönetimi** sekmesini açın (veya uygulamanın uyarısını izleyin) ve yapay zekâ ses modelini indirin (birkaç GB, yalnızca bir kez). Konuşma tanıma modelleri ilk kullandığınızda ayrıca indirilir.
4. **Metin Okuma sekmesini açın**, **çıkış dilini** seçin ve kitaplıktan bir ses seçin (30 hazır ses).
5. Metninizi yapıştırın → **Tabloya ekle** → **Başlat**. Her satırı dinleyin, ardından dosyayı kaydetmek için **Sesi dışa aktar**'a tıklayın (varsayılan olarak `.srt` altyazısıyla).

---

## Özellikler

<p align="center">
  <img alt="G-Labs Voice Studio arayüzü" width="900" src="docs/screenshots/en/voicechange.webp" />
</p>

- **Bilgisayarınızda çalışır** - modeller indirildikten sonra ses üretimi ve yazıya dökme yerel olarak çalışır (NVIDIA GPU, Apple Metal veya CPU); sesiniz ve metniniz sunucuya gönderilmez. Yalnızca çeviri sekmesi altyazı metnini seçtiğiniz yapay zekâ sağlayıcısına gönderir.
- **Ses klonlama** - 5-10 saniyelik bir örnekten, herhangi bir metni tam o sesle okutun.
- **Rastgele ses** - cinsiyet, yaş ve perdeye göre (İngilizce için ayrıca aksan) yeni bir ses tarif edin; örnek dosya gerekmez, beğendiklerinizi kitaplığa kaydedin.
- **600'den fazla çıkış dili** - Vietnamca, İngilizce, Çince, Japonca, Korece, Fransızca, Almanca, İspanyolca ve daha fazlası.
- **Çok sesli diyalog** - `<Ad>: replik` biçiminde senaryolar, her karakterin kendi sesi ve hızı.
- **Ses değiştirme ve dublaj** - bir video yükleyin, konuşmayı tanıyın veya çevrilmiş altyazıları getirin ve her satırı özgün zaman aralığı içinde yeniden seslendirin; sesi ya da sesi değiştirilmiş bir videoyu, özgün müziği koruyarak dışa aktarın.
- **Altyazı çıkarma** - MP3, WAV, M4A, FLAC, MP4, MOV… dosyalarını yazıya döker; kelime düzeyinde zamanlamayla TXT veya SRT dışa aktarır.
- **Yapay zekâ ile altyazı çevirisi** *(Studio planı)* - `.srt`, `.vtt`, `.ass`, `.sbv`, `.txt` dosyalarını çevirin veya düzeltin; zamanlamalar ve satır sayısı aynen korunur.
- **Ses kitaplığı** - kendi sayfası var: 30 hazır ses, kendi seslerinizi kaydedin, yazdığınız bir cümleyle her sesi önceden dinleyin, ⭐ favorileri sabitleyin, `.vcp` dosyalarıyla yedekleyin/geri yükleyin.
- **Ses ince ayarı** - 6 işleme modu, ses seviyesi dengeleme, 13 ifade etiketi ve `100%`, `25°C`, `m²` gibi şeylerin nasıl okunacağını hatırlayan bir telaffuz sözlüğü.
- **Esnek dışa aktarma** - WAV veya MP3, tek birleşik dosya veya cümle başına bir dosya, `.srt` ile; tek bir satırı ⬇ düğmesiyle indirin.
- **Oluşturma kuyruğu** *(Studio planı)* - birden çok senaryoyu sıraya koyun; uygulama bunları tek tek çalıştırır ve dosyaları kaydeder.
- **Webhook API** *(Studio planı)* - n8n, Make, Zapier, Python/cURL veya yapay zekâ ajanları için yerel bir REST sunucusu.
- **Donanımınızla başa çıkar** - uyumsuz bir ekran kartı net bir bildirimle CPU'ya geçer; GPU belleği boştayken otomatik serbest bırakılır.
- **9 arayüz dili** - Tiếng Việt, English, Português, Türkçe, 简体中文, हिन्दी, বাংলা, اردو, Русский.

---

## Sayfalar

Sayfalar sol kenar çubuğundadır ve gruplara ayrılmıştır: **Ses üret** (Metin Okuma, Grup Diyaloğu, Ses değiştir) · **Altyazı** (Altyazı Çıkar, Çeviri) · **Sesler** (Ses Klonu, Ses kitaplığı) · **Sistem** (Model Yönetimi, Webhook API, Kuyruk). Ses sayfaları aynı akışı izler: araç çubuğundan **Okuma dili**ni seçin → metni **Kaynak metin** alanına yapıştırın veya bir `.txt` / `.srt` dosyasını **İçe aktar** ile alın → **Tabloya ekle** (uygulama cümleleri seçtiğiniz biçimde böler, varsayılan **Akıllı birleştirme**) → **Üret** → dinleyin ve tek tek satırları düzeltin → **Dışa aktar**.

### 🔊 Ses Klonu

![Ses Klonu](docs/screenshots/en/clone.webp)

Örnek ses dosyasını yüklemek için **Seç...**'e tıklayın, ardından dalga formu üzerindeki vurgulu kutuyu sürükleyerek 3-30 saniyelik bir bölüm seçin (bıraktığınızda kenarlar sessizliğe oturur) veya **En iyi bölümü seç**'e basın.

- **Kaliteyi örnek belirler:** klon yalnızca sesi değil, örnekteki gürültüyü, yankıyı ve müziği de kopyalar. En temiz 5-15 saniyeyi kullanın; sesin arkasında müzik varsa önce **Müziği kaldır**'a basın.
- **Metin, örnekle kelimesi kelimesine eşleşmelidir** (noktalama ve yazım dahil). **Yapay zekâ önerisi** sizin için yazıya döker, ama dinleyip metni okuyarak izleyin ve hataları düzeltin: yanlış metin yanlış ses üretir.

Bir deneme cümlesi yazın, **Başlat**'a basın, dinleyin; ardından sağ panelde sese bir ad verip **Kitaplığa kaydet**'e tıklayın.

### 🎛️ Metin Okuma

![Metin Okuma](docs/screenshots/en/tts.webp)

Sağdaki **Ses** sekmesinde kitaplıktan bir **Kayıtlı ses** seçin ya da *cinsiyet, yaş ve perde*ye göre yeni bir ses tasarlamak için **Rastgele ses**'i seçin (İngilizce aksanı **Ayarlar → Genel ayarlar** içindedir). Tek bir satırı yeniden üretmek aynı sesi korur; beğendiklerinizi **Kaydet** ile kitaplığa ekleyin.

Metnini düzenlemek, öncesine bir duraklama eklemek (**Önce ara**) veya yalnızca o satırı yeniden üretmek (**Yeniden üret**) için bir satıra tıklayın; aşağıdaki zaman çizelgesi parçanın tamamını çalar, oynatma imlecini sürükleyerek istediğiniz yere atlayın. **Telaffuz**, uygulamaya `25°C` veya `100%` gibi ifadelerin nasıl okunacağını öğretir (sonraki tüm senaryolar için saklanır); **İfade etiketleri** metne `[laughter]`, `[sigh]`… ekler. Okuma hızı ve 6 ses stili **Ayarlar** sekmesindedir.

### 💬 Grup Diyaloğu

![Grup Diyaloğu](docs/screenshots/en/dialogue.webp)

Çok karakterli bir senaryo yazın - podcast, sesli drama ve röportajlar için ideal:

```
<Sunucu>: Herkese hoş geldiniz.
<Mai>: Merhaba, programda olmaktan çok mutluyum.
<Minh>: Ben de - bugün ne konuşacağız?
```

Karakter adını satır başında `< >` içine yazın (`:` isteğe bağlıdır, adlar büyük/küçük harf duyarsızdır). Örnek için **Örnek diyalog**'a, ardından **Diyaloğu ayrıştır**'a tıklayın - sağdaki **Ses** sekmesi her karakter için bir kart gösterir; kitaplıktan bir ses ve karaktere özel **Hız** (0.5× → 2×) seçin. Zaman çizelgesi her ses için bir satır gösterir; bir repliği başka satıra sürükleyerek onu kimin okuyacağını değiştirin.

### 🔁 Ses değiştir

![Ses değiştir](docs/screenshots/en/voicechange.webp)

Bir video veya ses dosyası yükleyip **Konuşmayı tanı**'ya basın - ya da Altyazı Çıkar / Çeviri sayfalarından **Ses değiştir'e gönder** düğmesiyle altyazıları alın (kaynak video da birlikte gelir). Her altyazı, özgün zamanlamasına sabitlenmiş bir satır olur; yeni sesi ve okuma dilini seçip **Üret**'e basın - **Altyazıya uydur** her satırı kendi zaman aralığında tutar.

Monitör, **Orijinal / Yeni ses / Yeni ses + fon** seçeneklerini karşılaştırmanızı sağlar (müzik, eski sesten Demucs ile ayrılır; ilk seferde yaklaşık 80 MB indirilir). 6 yolla dışa aktarın: yalnızca yeni ses, yeni ses + özgün müzik, yeni ses + kısık özgün ses - ses olarak ya da doğrudan videoya yazılmış halde.

> **Bir videoyu başka bir dile dublajlayın:** Altyazı Çıkar → **Çeviriye gönder** → çevirin → **Ses değiştir'e gönder** → bir ses + okuma dili seçin → Üret → videoyu dışa aktarın.

### 📝 Altyazı Çıkar

![Altyazı Çıkar](docs/screenshots/en/asr.webp)

Bir ses/video dosyası (MP3, WAV, M4A, FLAC, MP4, MOV…), konuşulan dili ve bir tanıma modeli seçin (Tiny → Large v3; her biri gereken VRAM'i gösterir) ve çalıştırın. Altyazı satırları kelime zaman damgalarından oluşturulur ve gerçek duraklamalarda / cümle sonlarında / karakter sınırında bölünür; *en fazla karakter, en fazla saniye, duraklama eşiği* kutularını değiştirdiğinizde tablo anında güncellenir, yeniden yazıya dökmek gerekmez. Doğrudan tabloda düzenleyin ve `.txt` veya `.srt` olarak dışa aktarın.

### 🌐 Çeviri *(Studio planı)*

![Çeviri](docs/screenshots/en/srt.webp)

Altyazıları başka bir dile çevirin veya yazım ve satır sonlarını düzeltin - **yalnızca metin değişir; zamanlamalar ve satır sayısı aynı kalır**.

1. **Model Yönetimi → LLM** bölümünde tek seferlik kurulum: **9Router** (bilgisayarınızda çalışan bir ağ geçidi - adresini ve API anahtarını girin), **Claude CLI**, **Antigravity** (`agy`) veya **Codex CLI** (kurun ve giriş yapın). Her satırda kurulum komutunu gösteren bir **Kılavuz** düğmesi vardır; kurduktan sonra **Listeyi yenile**'e tıklayın, uygulama onu algılayıp modellerini listeler.
2. `.srt`, `.vtt`, `.ass`, `.sbv`, `.txt` dosyasını **İçe aktar** ile açın - veya **Altyazıdan Al**. `.txt` dosyasında zamanlama yoktur; uygulama geçici zamanlar atar ve bunu bildirir.
3. Önerilir: **Metni düzenle**, cümle ortasında bölünmüş parçaları birleştirir (video düzenleyicilerden dışa aktarılan altyazılarda yaygındır); uygulamadan önce *"120 satır → 68 satır"* gibi bir önizleme gösterir.
4. **Çeviri**, **Düzenleme** veya **Çeviri + Düzenleme** seçin, hedef dili ve modeli seçin, ardından **Başlat**.
5. **Tutarlılık tablosu**, tüm dosya için adları, terimleri ve hitap biçimlerini sabitler ve her parçayla birlikte gönderilir; düzenleyebilir ve isterseniz çeviriden önce gözden geçirmek için durdurabilirsiniz.
6. **Sonuç** sütununu kontrol edin (yapay zekânın atladığı satırlar ⚠ ile işaretlenir ve orijinal metni korur), **SRT / VTT / TXT** seçin ve **Dışa aktar**.

### 🗂️ Ses kitaplığı

![Ses kitaplığı](docs/screenshots/en/library.webp)

Tüm sesleriniz tek yerde: ad / açıklama / etiketlere göre arayın, **Tümü / Benim / Hazır / Favoriler** ile filtreleyin, sabitlemek için ⭐'a tıklayın. Ayrıntıları görmek için bir ses seçin, özgün örneği çalın (hazır sesler) ya da bir cümle yazıp **Üret ve dinle**'ye basın; **Metin okumada kullan** o sesi seçili hâlde Metin Okuma'ya götürür. Sesleri yedeklemek veya başka bir bilgisayara taşımak için `.vcp` dosyalarını dışa/içe aktarın.

### 📚 Model Yönetimi

![Model Yönetimi](docs/screenshots/en/model.webp)

Üç bölüm: **Yapay zeka modelleri**, **Altyazı LLM** ve **Donanım** (GPU / CPU seçimi, boştayken VRAM'i serbest bırakma). Yapay zeka modelleri altında her model için boyut ve durumuyla bir satır: yapay zekâ ses modeli ve tanıma boyutları (Tiny, Base, Small, Turbo, Large v3). Yalnızca ihtiyacınız olanı indirin ve **model klasörünü** değiştirin (ör. C sürücüsünü rahatlatmak için D'ye - eski model klasörünü kopyalayın veya uygulamanın yeniden indirmesine izin verin). Çeviri için **LLM** sağlayıcısı ve **VRAM'i otomatik serbest bırak** zamanlayıcısı da burada ayarlanır.

### 🗒 Oluşturma kuyruğu *(Studio planı)*

Bir senaryoyu üretip elle dışa aktarmak yerine, mevcut senaryo + ses + ayarları **kendi adı ve çıkış klasörü** olan bir iş olarak kaydetmek için **Kuyruğa ekle**'a tıklayın. **Kuyruğu çalıştır** ile uygulama işleri tek tek yapar ve dosyaları kaydeder. Her iş `X/N cümle` gösterir; böylece hangisinde hata nedeniyle satır eksik kaldığını görürsünüz; **Yeniden yükle** işi düzeltmek için sekmesine geri getirir (başarısız satırlar ❌ ile işaretlenir). Kuyruk, uygulamayı kapatıp yeniden açtığınızda da korunur.

### 🔗 Webhook API *(Studio planı)*

![Webhook API](docs/screenshots/en/webhook.webp)

n8n, Make, Zapier, Python/cURL veya yapay zekâ ajanlarının otomatik olarak ses üretebilmesi için yerel bir REST sunucusu. Varsayılan `127.0.0.1:8766` (yalnızca bu bilgisayar); API anahtarı, kopyalama düğmeli tam **URL** kutusu, uygulamayla birlikte otomatik başlatma seçeneği ve canlı istek günlüğü vardır. Diğer cihazların çağırabilmesi için IP'yi `0.0.0.0` / yerel ağ IP'si yapın - bu durumda API anahtarı şifrelenmemiş HTTP üzerinden gider. Tam şema: [`docs/WEBHOOK_INTEGRATION.en.md`](docs/WEBHOOK_INTEGRATION.en.md).

---

## İpuçları

<details>
<summary><b>Ses ustalama - 6 işleme modu</b></summary>

Üç ses sekmesindeki **Ses ustalama** bölümünde (birinde değiştirin, diğerleri de uyar):

- 📻 **Yayın** *(varsayılan)* - radyo/podcast standardı, sıcak, sıkıştırılmış.
- 🎬 **Sinema** - geniş yankı, hafif sıkıştırma.
- 🎙️ **Podcast** - yakın mikrofon, güçlü sıkıştırma, yankısız.
- ☀️ **Sıcak** - güçlendirilmiş alt-orta frekanslar, sıcak his.
- ✨ **Parlak** - net tizler, ferah.
- 🔇 **Ham** - modelin çıktısı olduğu gibi.

**Cümleler arası ses seviyesini eşitle**, algılanan ses yüksekliğine (RMS) göre dengeler; yüksek ve alçak satırlar kalmaz. Modelin dokunulmamış çıktısı için **Ham** seçin ve bu kutunun işaretini kaldırın.

</details>

<details>
<summary><b>İfade etiketleri</b></summary>

Metne bir etiket yazın (köşeli parantezleri koruyun; tek başına veya cümle ortasında, ör. `Çok komik [laughter] gülmeden duramıyorum.`) - ses, kelimeyi okumak yerine o sesi çıkarır. Ezberlemeniz gerekmez: **İfade etiketleri** düğmesiyle bakıp ekleyebilirsiniz.

| Etiket | Ses |
|---|---|
| `[laughter]` | Gülme |
| `[sigh]` | İç çekme |
| `[confirmation-en]` | Onaylama - "mm-hmm" |
| `[question-en]` · `[question-ah]` · `[question-oh]` · `[question-ei]` · `[question-yi]` | Soru tonlaması |
| `[surprise-ah]` · `[surprise-oh]` · `[surprise-wa]` · `[surprise-yo]` | Şaşkınlık |
| `[dissatisfaction-hnn]` | Hoşnutsuzluk - "hnn" |

Etkinin gücü dile ve sese göre değişir - önce kısa bir cümlede deneyin.

</details>

<details>
<summary><b>Telaffuz sözlüğü</b></summary>

Metinde `%`, `$`, `°C`, `m²`, marka adları… mı var? Üretmeden önce **Telaffuzu düzelt**'a tıklayın: uygulama her sembolün/kelimenin nasıl okunacağını sorar, okunuşu bir kez yazarsınız (ör. `%` → `yüzde`) ve her çıkış dili için hatırlar.

</details>

<details>
<summary><b>Dışa aktarırken hız ve altyazı</b></summary>

- **Okuma hızı** *Gelişmiş ayarlar* içindedir; oynatıcıdaki **Hız** denetimi daha hızlı/yavaş dinlemenizi sağlar ve dışa aktarılan dosya bu hızı perde bozulmadan korur.
- **Altyazıyı da dışa aktar**, sesin yanına eşleşen bir `.srt` yazar; zamanlamalar, hız ayarından sonra her cümlenin gerçek uzunluğundan alınır.
- **Konuşmayı altyazı zamanlamasına uydur**: senaryo bir `.srt` dosyasından geldiyse her satır kendi aralığına sığması için hızlandırılır (en fazla 1.8×) - asla yavaşlatılmaz.

</details>

<details>
<summary><b>Otomatik bellek boşaltma</b></summary>

Uygulamayı bir süre boşta bırakın (varsayılan 5 dakika); yapay zekâ modeli bilgisayarınızı rahatlatmak için VRAM/RAM'den kaldırılır ve bir sonraki işleminizde yeniden yüklenir. Süreyi değiştirin veya kapatın: **Model Yönetimi → VRAM'i otomatik serbest bırak**.

</details>

---

## Sistem gereksinimleri

|   | En düşük | Önerilen |
|---|---|---|
| **İşletim sistemi** | Windows 10 (64-bit), Apple Silicon üzerinde macOS 12 | Windows 11, macOS 13 veya üzeri |
| **Windows** | CUDA destekli NVIDIA ekran kartı, **RTX 2060** veya üzeri; 8 GB RAM | **12 GB VRAM'li RTX 3060** veya üzeri; 16 GB RAM |
| **Mac** | Apple Silicon **M1** veya daha yeni, **16 GB RAM** | M2 / M3 / M4, daha fazla RAM |
| **Disk** | 10 GB boş (modeller + önbellek) | 20 GB veya daha fazla, SSD |
| **Ağ** | Giriş/lisans denetimi ve model indirme için internet | |

- **Windows:** CUDA destekli bir NVIDIA kart gerekir: **RTX 2060** veya daha yeni (compute capability ≥ 7.0) ve CUDA 12.8 destekli sürücü; akıcı ve kararlı çalışma için **12 GB VRAM'li RTX 3060** veya üzerini kullanın. GTX 10 serisi gibi eski kartlar algılanır ve CPU'ya düşer - yaklaşık 5-10 kat yavaş, yalnızca uygulamayı denemek için uygundur.
- **macOS:** **16 GB veya daha fazla RAM'li Apple Silicon M1 ya da daha yenisi**, Metal ile hızlandırılır.

---

## Verileriniz nerede

| Ne | Windows | macOS |
|---|---|---|
| Dışa aktarılan ses (varsayılan) | Uygulamayı çıkardığınız klasörün içindeki `output\` | `~/Documents/G-Labs Voice Studio/output` |
| Ayarlar, giriş oturumu | `%APPDATA%\G-Labs Voice Studio` | `~/Library/Application Support/G-Labs Voice Studio` |
| Ses kitaplığınız | `%APPDATA%\G-Labs Voice Studio\voice_studio\voices` | `~/Library/Application Support/G-Labs Voice Studio/voice_studio/voices` |
| Yapay zekâ modelleri | `%APPDATA%\G-Labs Voice Studio\voice_studio\model` (veya seçtiğiniz klasör) | `~/Library/Application Support/G-Labs Voice Studio/voice_studio/model` (veya seçtiğiniz klasör) |
| Oluşturma kuyruğu | `%APPDATA%\G-Labs Voice Studio\voice_studio\queue` | `~/Library/Application Support/G-Labs Voice Studio/voice_studio/queue` |

Ses kitaplığınızı başka bir bilgisayara taşımak için ses kitaplığı panelindeki **`.vcp` yedekle/geri yükle** özelliğini kullanın.

---

## Sorun giderme

**İlk açılış çok yavaş, açılış ekranı kıpırdamıyor** - Windows/macOS ilk güvenlik taramasını yapıyor; 30-60 saniye bekleyin, kapatmayın. Sonraki açılışlar daha hızlıdır.

**Windows "Windows bilgisayarınızı korudu" ekranında duruyor** - **Ek bilgi → Yine de çalıştır**'a tıklayın. Uygulama Microsoft sertifikasıyla imzalı değildir; virüs değildir.

**macOS uygulamanın hasarlı olduğunu / açılamadığını söylüyor** - uygulama Apple tarafından onaylanmamıştır. İlk seferde sağ tık → **Aç**, ya da `xattr -dr com.apple.quarantine "/Applications/G-Labs Voice Studio.app"` komutunu çalıştırın.

**CPU'ya geçildiği bildirimi** - ekran kartınız uyumlu değil (ör. GTX 10 serisi). Her şey çalışmaya devam eder, yalnızca daha yavaş; hız için NVIDIA RTX 20 serisi veya daha yenisi ya da Apple Silicon Mac gerekir.

**Her seferinde yalnızca 1 satır üretiliyor** - deneme sürümündesiniz. Sınırsız satır için Studio planını satın alın.

**Hesabın başka cihazda giriş yaptığı mesajıyla oturum kapandı** - bir hesap aynı anda tek bilgisayarda çalışır; kullanmak istediğiniz bilgisayarda yeniden giriş yapın.

**Klonlanan ses yanlış kelimeler söylüyor / kayıyor** - *Örnek metin* örnekteki sözcüklerle birebir eşleşmelidir; net ve az gürültülü bir örnek seçin.

**Özel karakterler yanlış okunuyor (`100%`, `25°C`…)** - okunuşlarını **Telaffuzu düzelt** bölümüne ekleyin.

**C sürücüsü modellerle doluyor** - **Model Yönetimi** içinde model klasörünü değiştirin, ardından eski klasörü kopyalayın veya uygulamanın yeniden indirmesine izin verin.

**Çeviri sekmesinde seçilecek model yok** - **Kılavuz** düğmesini izleyerek bir LLM sağlayıcısı (9Router, Claude CLI, Antigravity, Codex) kurun ve giriş yapın, sonra **Listeyi yenile**'e tıklayın.

**Ayrıntılı hata bilgisi gerekiyor** - kenar çubuğundaki **Ayrıntılı Günlük**'a tıklayın.

---

📖 [Ürün sayfası](https://duckspace.net/en/voice-studio/) · [Kılavuz](https://duckmartians.info/voice/guide/en/) · [Değişiklik günlüğü](CHANGELOG.md) · [Discord](https://discord.gg/munMZEBMw5)

© 2026 Duck Martians AI Labs. Tüm hakları saklıdır.
