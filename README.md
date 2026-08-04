# 📸 alettin.com - Görsel Ekleme ve Güncelleme Rehberi

Bu rehber, **alettin-web** projenizde web sitenize yeni görseller ekleme, mevcut görselleri değiştirme ve GitHub'a güncelleme gönderme adımlarını adım adım açıklar.

---

## 📁 1. Görsel Dosyalarını Konumlandırma

Sitedeki tüm görseller projenizin kök dizininde bulunan `images/` klasöründe yer alır.

1. Eklemek istediğiniz yeni görseli bilgisayarınızdan kopyalayın.
2. Proje klasöründeki `images/` dizinine yapıştırın (Örn: `images/yeni-fotograf.jpg` veya `images/kapak-v2.png`).

> [!TIP]
> **Önemli İpucu (Performans ve GitHub Sınırları):**
> - Görsel boyutlarının çok yüksek olmamasına dikkat edin (Tercihen dosya başı **1 MB - 5 MB** arasında).
> - Tek bir dosya boyutu **100 MB**'ı geçmemelidir (GitHub 100 MB üzeri tekil dosyaları kabul etmez).
> - Web için `.jpg`, `.png` veya `.webp` formatlarını tercih edin.

---

## 💻 2. `index.html` Dosyasında Görseli Bağlama

Eklediğiniz veya değiştirmek istediğiniz görseli `index.html` dosyasında ilgili etikete tanımlayın.

### Örnek 1: Kapak / Hero Portre Görselini Değiştirmek
`index.html` dosyasında `hero-portre` kısmını bularak `src` yolunu güncelleyin:

```html
<img src="images/Kapak.png" alt="hero-portre" style="width:100%; height:100%; object-fit:cover; display:block;">
```

Örneğin yeni görselinizin adı `yeni-portre.jpg` ise:

```html
<img src="images/yeni-portre.jpg" alt="hero-portre" style="width:100%; height:100%; object-fit:cover; display:block;">
```

---

## 🚀 3. Değişiklikleri GitHub ve Canlı Sitemize Yükleme

Görselleri ekleyip `index.html` dosyasını kaydettikten sonra Visual Studio Code terminalinde sırasıyla şu 3 komutu çalıştırarak canlı sitenizi güncelleyebilirsiniz:

```bash
# 1. Tüm yeni ve değişen dosyaları hazırlık alanına ekleyin
git add .

# 2. Değişiklikler için kısa bir açıklama mesajı ekleyin
git commit -m "Yeni görseller eklendi"

# 3. Kodları GitHub'a gönderin (Siteniz otomatik güncellenir)
git push origin main
```

> [!NOTE]
> `git push` komutundan 1-2 dakika sonra GitHub Pages otomatik olarak canlı sitenizi (`https://ffhonor.github.io/alettin-web/`) güncelleyecektir.
