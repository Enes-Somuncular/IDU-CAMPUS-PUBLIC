# 📋 Sürüm Günlüğü (Changelog)

İDÜ Campus projesindeki tüm önemli değişiklikler, yeni özellikler ve hata düzeltmeleri bu belgede kayıt altına alınmaktadır.

Format [Keep a Changelog](https://keepachangelog.com/tr/1.0.0/) standartlarına ve [Semantic Versioning](https://semver.org/lang/tr/) kurallarına dayanmaktadır.

---

## [1.8.3] - 2026-11-10

### 🚀 Eklendi & İyileştirildi
- **400ms Ultra Hızlı Bulut Senkronizasyonu:** Ders taşıma, geri alma ve yoklama işaretlemelerinde buluta aktarım gecikmesi 400ms'ye indirildi. Bir ders taşındığında veya geri alındığında eşitleme anında tetiklenir.
- **Sayfa Yenileme (F5) ve Sekme Kapatma Koruması:** Bir değişiklik yapıldıktan hemen sonra sayfa yenilense veya tarayıcı sekmesi kapatılsa bile bekleyen istekler yerel kuyrukta korunur; bir sonraki açılışta buluta otomatik aktarılır.
- **Optimistic UI:** Ağ gecikmesinden bağımsız olarak arayüz anında güncellenir, arka planda sunucu mutabakatı sağlanır.

---

## [1.8.2] - 2026-11-10

### 🎨 Arayüz & Görsel İyileştirmeler
- **Canlı Senkronizasyon Durum Rozetleri:** Profil menüsünün altında sabit yazı yerine gerçek zamanlı senkronizasyon durumu yansıtılır:
  - `✓ Eşitlendi` (Yeşil - Tüm veriler bulutla senkron)
  - `↻ Eşitleniyor…` (Mavi - Veri Cloudflare D1'e aktarılıyor)
  - `⚠ Çevrimdışısın` (Sarı - İnternet bağlantısı kesildi, yerel depolama devrede)
- Senkronizasyon anı animasyonlu geçişlerle kullanıcıya hissettirilir.

---

## [1.8.1] - 2026-11-10

### 🔄 Senkronizasyon & Çoklu Cihaz
- **Taşınan Derslerin Bulut Senkronizasyonu:** Takvim üzerinde raptiye ile başka güne taşınan veya ertelenen dersler ve özel notlar, kullanıcının bulut hesabına tam entegre edildi.
- **Cihazlar Arası Kesintisiz Deneyim:** Telefondan ertelenen bir ders veya işaretlenen bir yoklama, masaüstü bilgisayarda oturum açıldığında saniyeler içinde ekranda belirir.
- **Otomatik Arka Plan Eşitleme:** Oturum açık olan cihazlarda değişiklik gerçekleştiği anda arka planda D1 SQLite veri tabanına işlenir.

---

## [1.8.0] - 2026-11-10

### ✨ Büyük Sürüm: Öğrenci Hesapları & Kişisel Ders Taşıma (Raptiye)
- **Gizlilik Odaklı Öğrenci Hesapları:** 
  - E-posta veya telefon numarası gerektirmeyen sıfır kişisel veri modeli.
  - Dilediğin `@kullanici` adı ve sistemin ürettiği 4 haneli güvenli PIN ile anında hesap oluşturma.
  - Brute-force ve kötüye kullanıma karşı PIN deneme kilidi ve güvenlik soğuma süreleri.
- **Tıp Temalı Profil Avatarları:** 
  - Stetoskop 🩺, DNA/Genetik 🧬, Mikroskop 🔬, Beyin/Nöroloji 🧠, Klinik 🏥, Yıldız ✨ avatar seçenekleri.
  - Tek tıkla yeni 4 haneli PIN üretme ve aylık kullanıcı adı güncelleme kotası.
- **Kişisel Ders Taşıma (Raptiye Sistemi):**
  - Saati veya günü değişen dersleri takvim üzerinde istenilen tarih ve saate taşıma imkanı.
  - 3D raptiye ve kıvrık kağıt görünümüyle görsel ayırt edicilik.
  - Aynı saate denk gelen başka derslerle çakışma uyarı kontrolü.
  - İsteğe bağlı özel not iliştirme (örn. "Mukaddes hoca ile perşembeye ertelendi").
- **Eski Sistemden Geçiş Köprüsü:**
  - Önceki sürümlerden kalan 16 haneli anonim yedek kodlarını tek tıkla yeni hesaba aktarma ve verileri bağlama aracı.
- **Yenilenen Yoklama Paneli:**
  - 3 sekmeli temiz arayüz: 📊 Genel Durum, 📚 Dersler, ✍️ Hızlı Yoklama Ver.
  - Tıp Fakültesi devam barajı (%30 Teorik / %20 Pratik) ilerleme barları ve akıllı devamsızlık risk banner'ları.

---

## [1.7.1] - 2026-11-08

### 📊 Yoklama Takibi & Komite Analizi
- **Hızlı Yoklama İşaretleme:** Teorik ve pratik ders kartlarında tek dokunuşla Var (✓), Yok (✕), İptal (−) işaretleme.
- **Toplu İşaretleme:** Seçili günün tüm derslerini tek hareketle "Var" yapabilme.
- **Komite Bölümleme:** Dersleri komiteler halinde ayırarak inceleme veya tüm komiteleri birleştirme.
- **Devamsızlık Barajı Takibi:** Kalan devamsızlık hakkı simülatörü ve muaf ders (dikkate alınmayan) seçimi.
- **Komite Sınavı Geri Sayımı:** Aktif komite sınavına kalan gün sayısı ve ders/soru ağırlık dağılım kartı.
- **Yedekleme Desteği:** D1 Cloud eşitlemesinin yanı sıra okunabilir `.txt` formatında yedek indirme ve geri yükleme.

---

## [1.7.0] - 2026-11-08

### 🎯 Sadeleşme ve Yönetim Mimarisi
- Menü yapısı doğrudan ders programına, yoklamaya ve geri bildirimlere odaklandı.
- Çevrimdışı bağlantı koruması: Ağ kopsa bile son açılan program ekranda aktif kalır.
- Yönetim paneli ve yerel masaüstü aracı (`Open-Campus-Manager.cmd`) ile güvenli Excel önizleme ve yayınlama boru hattı.

---

## [1.6.0] - 2026-11-06

### 🌊 Akış (Flow) Tasarımı
- **Yatay Zaman Akışı:** Masaüstünde pürüzsüz yatay akış ve yapışkan gün başlıkları.
- **Mobil Gün Seçici:** Dar ekranlarda takvim karmaşasını engelleyen sezgisel gün sekmeleri.
- **Canlı Zaman Çizgisi:** İstanbul saatine göre geçerli anı gösteren dinamik saat çizgisi.
- **Ortak Tasarım Sistemi:** Bildirim takibi, hesap, ek ders ve yönetim ekranlarında tutarlı tipografi ve yüzey dili.
- **Yerel NLP Asistan Denemeleri:** Tarayıcı üzerinde çalışan Qwen 2.5 ve Türkçe Niyet (Intent) modeli ile "Sıradaki dersim ne?", "Sınav ne zaman?" sorularını yanıtlama ar-ge çalışması.

---

## [1.5.0] - 2026-11-04

### 📱 Mobil İyileştirmeler & Kaynak Şeffaflığı
- Gruplandırılmış sol menü çekmecesi (Drawer).
- Alttan açılan mobil ders ayrıntı paneli (Bottom Sheet).
- Kaynak doğrulama raporu: Excel'deki eksik veya atlanan satırların şeffaf dökümü.

---

## [1.4.0] - 2026-11-02

### 📑 Kurul Excel Ayrıştırma
- Kurul Excel dosyalarını doğrudan ayrıştıran ve tarih kapsamını otomatik çıkaran yükleme akışı.
- Otomatik gün seçimi ve elle tarih aralığı tanımlama desteği.

---

## [1.0.0] - 2026-10-26

### 🎉 İlk Kararlı Sürüm
- Fakültenin resmî 26.10.2026 tarihli Excel bülteninden tam ders programı takvimi.
- Günlük ve haftalık görünüm modları.
- Grup filtreleri (A, B, C, D) ve serbest çalışma saatleri geçişi.
- Açık ve koyu tema desteği (cihaz hafızasında saklanan tercihler).
- Kriptografik takip kodlu anonim geri bildirim formu ve Cloudflare D1 entegrasyonu.
- Build gerektirmeyen Vanilla JS ES modülleri ve PWA temeli.
