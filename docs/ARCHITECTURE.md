# İDÜ Campus mimarisi

- **Tarayıcı:** HTML, CSS ve JavaScript modülleri ders programını, grup filtresini ve kişisel yoklamayı gösterir. İsteğe bağlı profil, yoklama ve kişisel ders taşıma kayıtları yerel depoda tutulur.
- **TXT yedek:** Kullanıcı dosyayı dışa aktarır veya kendi tarayıcısına geri yükler. Uygulama dosyayı doğrular ve onay öncesinde eklenecek ya da değişecek kayıtları gösterir. Öğrenci hesabı, PIN ve cihazlar arası bulut eşitlemesi kapalıdır.
- **Çevrimdışı kullanım ve güncelleme:** Service Worker uygulama dosyalarını ve doğrulanmış son program kopyasını önbelleğe alır. Yeni uygulama sürümü hazır olduğunda açık işlem pencerelerinin kapanmasını bekleyip otomatik uygulanır. Kullanıcı **Güncelle** düğmesiyle de kontrol başlatabilir.
- **Program verisi:** Fakülte Excel’i Python ve openpyxl ile işlenir. Kullanılan revizyon, dosya özeti ve aktarılamayan satırlar kaynak bilgilerinde gösterilir. Program bağımsız bir öğrenci aracıdır.
- **Barındırma:** Cloudflare Pages statik dosyaları sunar. Yönetim, program ek kayıtları ve önceki bildirimlerin takibi öğrenci profilinden ayrı işlevlerdir.
