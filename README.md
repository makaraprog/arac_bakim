# 🔧 Araç Bakım Takip - PWA (Android & iOS)

## Nedir?
Mevcut masaüstü uygulamanızın **Progressive Web App (PWA)** versiyonudur.  
Android ve iOS'ta **uygulama gibi** çalışır, **tamamen offline** çalışır, veriler telefonda saklanır.

---

## 📱 Telefona Nasıl Yüklenir?

### Android (Chrome ile)
1. Uygulamayı Chrome'da açın
2. Sağ üstteki **⋮ menüsüne** tıklayın
3. **"Ana ekrana ekle"** seçin
4. Onaylayın → Uygulamanız ana ekrana eklenir ✓

### iOS (Safari ile)
1. Safari ile açın
2. Alt kısımdaki **Paylaş** (□↑) butonuna tıklayın
3. **"Ana Ekrana Ekle"** seçin
4. Onaylayın → Uygulamanız ana ekrana eklenir ✓

---

## 🚀 Nasıl Çalıştırılır?

### Seçenek 1: Python ile yerel sunucu (Test için)
```bash
cd arac-bakim-pwa
python -m http.server 8080
# Tarayıcıda: http://localhost:8080
```

### Seçenek 2: Ücretsiz deploy (Herkes erişsin)
**Netlify ile (önerilen):**
1. [netlify.com](https://netlify.com) → üye olun
2. `arac-bakim-pwa` klasörünü sürükle-bırak
3. Otomatik URL alırsınız → telefondan açın → yükleyin ✓

**GitHub Pages ile:**
```bash
git init && git add . && git commit -m "init"
# GitHub'a push edin → Settings → Pages → Deploy
```

---

## 📦 Özellikler

| Özellik | Açıklama |
|---|---|
| 👤 Müşteri Yönetimi | Çoklu araç desteği, arama |
| 🔧 Bakım Kaydı | Parça listesi, ücret hesaplama |
| 📸 Fotoğraf Ekleme | Kameradan veya galeriden |
| 📊 Raporlar | Aylık gelir, genel özet, CSV export |
| 💾 Offline | İnternet olmadan çalışır |
| 📤 Yedek | JSON olarak dışa aktarma |
| 🖨️ Yazdırma | Her bakım için fatura/rapor |

---

## 💾 Veri Depolama
- **IndexedDB** kullanılır (tarayıcıda kalıcı)
- İnternet gerektirmez
- Veriler telefonda şifreli saklanır
- **JSON yedekleme** ile PC'ye aktarabilirsiniz

---

## 📁 Dosya Yapısı
```
arac-bakim-pwa/
├── index.html     ← Ana uygulama (tek dosya!)
├── manifest.json  ← PWA tanımı
├── sw.js          ← Offline çalışma (Service Worker)
└── README.md      ← Bu dosya
```

---

## ⚙️ Özelleştirme
`index.html` içinde arayabilirsiniz:
- `--accent: #f97316` → Ana rengi değiştir
- Bakım türleri listesi → `<select id="b-tur">` bölümü
- Uygulama adı → `topbar-logo` bölümü
