# 🤝 Katkıda Bulunma Rehberi (Contributing Guide)

İDÜ Campus projesine katkıda bulunmak istediğiniz için teşekkür ederiz! Bu proje, tıp öğrencilerinin akademik hayatını kolaylaştırmak amacıyla tamamen gönüllü ve bağımsız bir inisiyatif olarak yürütülmektedir.

Projeye kod yazarak, hata bildirerek, tasarım önerileri sunarak veya dokümantasyonu geliştirerek destek olabilirsiniz.

---

## 📌 Temel İlkelerimiz

1. **Bağımsızlık:** Bu proje üniversitenin resmî bir platformu değildir; ancak her zaman resmî kaynaklarla %100 uyumlu ve saygılı olmayı hedefler.
2. **Sıfır Bağımlılık (Zero Dependencies):** Proje saf modern web standartlarıyla (Vanilla ES Modules, CSS) çalışır. Gerekmedikçe dış kütüphane veya ağır npm paketleri eklenmez.
3. **Gizlilik Odaklılık:** Kullanıcıların hiçbir kişisel verisi (e-posta, telefon vb.) zorunlu tutulamaz.
4. **Resmî Bilgiye Saygı:** Resmî ders programı Excel dosyası asla yapay tahminlerle sessizce değiştirilmez; kaynakta hata varsa saydam biçimde raporlanır.

---

## 🛠️ Katkı Türleri

### 1. Hata Bildirimi (Bug Reports)
Eğer programda yanlış bir ders saati, eksik amfi bilgisi veya arayüzde bir kayma fark ettiyseniz:
- Doğrudan canlı sitedeki **"Geri Bildirim"** formunu kullanabilirsiniz (En hızlı yöntem).
- Veya GitHub üzerinde bir **Issue** açarak sorunu, tarayıcı/cihaz bilginizi ve varsa ekran görüntüsünü paylaşabilirsiniz.

### 2. Özellik Önerileri (Feature Requests)
Tıp fakültesi öğrencilerine fayda sağlayacak yeni bir fikir mi var?
- Bir Issue açarak önerinizi açıklayın.
- Neden gerekli olduğunu ve kullanıcı deneyimini nasıl iyileştireceğini belirtin.

### 3. Kod Katkısı (Pull Requests)
Kod katkısı sunmak isterseniz:
1. Depoyu forklayın (`Fork`).
2. Yeni bir özellik dalı oluşturun:
   ```bash
   git checkout -b ozellik/harika-yeni-ozellik
   ```
3. Değişikliklerinizi yapın ve yerel olarak test edin.
4. Anlaşılır bir commit mesajı yazın:
   ```bash
   git commit -m "feat(takvim): komite sınavı geri sayımına hafta sonu filtresi eklendi"
   ```
5. Dalınızı GitHub'a gönderin ve bir Pull Request (PR) açın.

---

## 📜 Kodlama Standartları

- **HTML & Arayüz:** Erişilebilirlik (WAI-ARIA, ekran okuyucu uyumluluğu, klavye ile gezinme) önceliklidir. Semantik HTML elemanları ve `<dialog>` tercih edilmelidir.
- **CSS:** BEM veya mantıksal bileşen adlandırmaları, CSS değişkenleri (`var(--accent-color)`), mobil öncelikli responsive yaklaşım.
- **JavaScript:** Saf ES Modülleri (`export / import`), `async / await`, hataya dayanıklı (defensive programming) veri işleme.
- **Kişisel Veri Yasağı:** Kodun veya dokümanların hiçbir yerine kişisel e-posta, telefon veya gerçek isimler eklenmemelidir.

---

## 🧪 Testler ve Doğrulama

Değişiklik yapmadan önce mevcut testleri çalıştırmayı unutmayın:
```bash
python -m unittest discover -s tests -v
node --test tests/*.test.mjs
```

---

<div align="center">
  <i>Birlikte daha iyi bir kampüs ajandası inşa ediyoruz! 🩺✨</i>
</div>
