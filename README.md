# DİJİTAB PWA - Kurulum Talimatları

## Dosya Yapısı
```
dijitab-pwa/
├── index.html
├── manifest.json
├── service-worker.js
├── icons/
│   ├── icon-72x72.png
│   ├── icon-96x96.png
│   ├── icon-128x128.png
│   ├── icon-144x144.png
│   ├── icon-152x152.png
│   ├── icon-192x192.png
│   ├── icon-384x384.png
│   └── icon-512x512.png
└── js/
    ├── app.js
    ├── store.js
    └── views.js
```

## Özellikler

### ✅ Progressive Web App (PWA)
- **Çevrimdışı Çalışma**: Service Worker ile offline destek
- **Ana Ekrana Eklenebilir**: iPhone ve Android'de uygulama gibi çalışır
- **Tam Ekran Mod**: iOS'ta tarayıcı çubuğu olmadan çalışır
- **Hızlı Yükleme**: Önbelleğe alınmış kaynaklar sayesinde anlık başlatma

### 📱 iPhone Uyumluluğu
- Safari'de "Ana Ekrana Ekle" özelliği ile tam ekran
- Apple Touch Icon desteği
- Status bar optimizasyonu
- Standalone display mod

## Kurulum Adımları

### 1. Web Sunucuya Yükleme
PWA özelliklerinin tam çalışması için HTTP veya HTTPS protokolü gereklidir.

**Seçenek A: Basit Python HTTP Server (Test için)**
```bash
cd dijitab-pwa
python -m http.server 8000
```
Tarayıcıda: `http://localhost:8000`

**Seçenek B: Netlify/Vercel (Ücretsiz Hosting)**
1. Tüm dosyaları GitHub reposuna yükleyin
2. Netlify veya Vercel ile bağlayın
3. Otomatik deploy edilecek

**Seçenek C: cPanel/Hosting Panel**
1. Dosyaları public_html veya www klasörüne yükleyin
2. HTTPS aktif olduğundan emin olun
3. Sitenizi ziyaret edin

### 2. iPhone'da Ana Ekrana Ekleme
1. Safari'de uygulamayı açın
2. Paylaş butonuna tıklayın (⬆️)
3. "Ana Ekrana Ekle" seçeneğini seçin
4. İsim verin ve "Ekle"ye basın

Uygulama artık ana ekranınızda, tarayıcı çubuğu olmadan çalışacak!

### 3. Android'de Ana Ekrana Ekleme
1. Chrome'da uygulamayı açın
2. Menü (⋮) > "Ana ekrana ekle"
3. Uygulamayı onaylayın

## Özellik Listesi

### 📊 Dashboard (Genel Bakış)
- Toplam portföy değeri
- Aktif müşteri sayısı
- Ciro hedefi takibi
- Piyasa verileri (USD, EUR, Altın)

### 👥 CRM (Müşteri Yönetimi)
- Müşteri listesi
- Yeni müşteri ekleme
- Müşteri detayları ve notları

### 🏢 Portföy Yönetimi
- İlan listesi
- Yeni ilan ekleme
- Satılık/Kiralık kategorileri

### 💰 Ciro & Hedefler
- Yıllık ciro hesaplama
- KDV hesaplaması
- Net gelir takibi
- Hedef karşılaştırması

### 📅 Takvim & Planlama
- Aylık takvim görünümü
- Günlük görevler
- Görev ekleme/silme

### 💳 Finans Modülü
- Gelir/Gider takibi
- Fatura okutma (OCR)
- Kategori bazlı raporlama

### 📱 Sosyal Medya Planlayıcı
- İçerik takvimi
- Platform seçimi
- Post planlama

## Teknik Detaylar

### Veri Saklama
- Tüm veriler `localStorage` kullanılarak tarayıcıda saklanır
- Offline çalışma için Service Worker cache
- Tarayıcı geçmişi silindiğinde veriler de silinir

### Tarayıcı Uyumluluğu
- ✅ Chrome 90+
- ✅ Safari 14+
- ✅ Firefox 85+
- ✅ Edge 90+

### Güvenlik
- HTTPS zorunlu (PWA özellikler için)
- Client-side veri saklama
- Sunucu bağlantısı gerektirmez

## Sorun Giderme

### Service Worker çalışmıyor
- HTTPS kullandığınızdan emin olun
- `file:///` protokolü PWA desteklemez
- Console loglarını kontrol edin

### iPhone'da tam ekran çalışmıyor
- "Ana Ekrana Ekle" ile açtığınızdan emin olun
- Safari'den direkt açmayın
- Cache'i temizleyip tekrar ekleyin

### Offline çalışmıyor
- İlk yüklemeden sonra internet kesildiğinde çalışmalı
- Hard refresh (Ctrl+Shift+R) sonrası cache sıfırlanır

## Destek

Sorun yaşarsanız:
1. Tarayıcı console'unu kontrol edin (F12)
2. Application tab > Service Workers bölümüne bakın
3. Cache temizleyip yeniden deneyin

## Lisans

Bu uygulama emlak profesyonelleri için geliştirilmiş özel bir çözümdür.
