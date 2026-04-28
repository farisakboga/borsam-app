# Borsam - Borsa Portföy Takip Uygulaması

Borsam, borsa portföyünüzü takip etmek, analiz etmek ve büyütmek için tasarlanmış bir web uygulamasıdır.

## Özellikler

- 📊 Portföy özeti ve hisse listesi
- 💰 Kâr/zarar hesaplamaları
- 📈 Sıralama ve filtreleme
- 🎯 Hedef fiyat takibi
- 📱 Mobil uyumlu tasarım
- 🔄 İşlem yönetimi

## Kurulum

### Lokal Geliştirme

```bash
# Bağımlılıkları yükleyin
npm install

# Cordova'yı global olarak yükleyin
npm install -g cordova

# Android platformunu ekleyin
cordova platform add android

# Geliştirme sunucusunu başlatın
cordova serve
```

### APK Oluşturma

```bash
# Debug APK
cordova build android

# Release APK
cordova build android --release
```

## GitHub Actions ile Otomatik Build

Bu repository GitHub Actions kullanarak otomatik olarak APK oluşturur.

### Kurulum Adımları

1. **GitHub'a Push Edin**
   ```bash
   git init
   git add .
   git commit -m "Initial commit"
   git branch -M main
   git remote add origin https://github.com/YOUR_USERNAME/borsam-app.git
   git push -u origin main
   ```

2. **GitHub Actions Workflow Çalışacak**
   - Her push'ta otomatik olarak APK oluşturulur
   - Artifacts sekmesinde indirebilirsiniz

3. **Release Oluşturun (Opsiyonel)**
   ```bash
   git tag v1.0.0
   git push origin v1.0.0
   ```
   - Release otomatik olarak oluşturulur
   - APK dosyası release'e eklenir

## Dosya Yapısı

```
borsam-cordova/
├── www/
│   ├── index.html          # Ana uygulama
│   ├── css/
│   │   └── index.css
│   ├── js/
│   │   └── index.js
│   └── img/
├── config.xml              # Cordova yapılandırması
├── package.json
├── .github/
│   └── workflows/
│       └── build-apk.yml   # GitHub Actions workflow
└── README.md
```

## Teknoloji Stack

- **Frontend**: HTML5, CSS3, JavaScript
- **Framework**: Apache Cordova
- **Build**: GitHub Actions
- **Platform**: Android

## APK İndirme

### Seçenek 1: GitHub Actions Artifacts
1. GitHub repository'ye gidin
2. "Actions" sekmesini açın
3. Son workflow'u tıklayın
4. "Artifacts" bölümünden APK'yı indirin

### Seçenek 2: GitHub Releases
1. Repository'de "Releases" sekmesini açın
2. Son release'i tıklayın
3. APK dosyasını indirin

## Kurulum (Android)

1. APK dosyasını Android telefonunuza aktarın
2. Dosya yöneticisinden APK'yı açın
3. "Yükle" butonuna tıklayın
4. Uygulamayı kullanmaya başlayın

## Gereksinimler

- Node.js 14+
- npm veya yarn
- Java 17+ (APK oluşturmak için)
- Android SDK (lokal build için)

## Lisans

ISC

## Destek

Sorunlar veya öneriler için GitHub Issues'u kullanın.

## Notlar

- Uygulama tamamen client-side çalışır
- Veriler tarayıcı localStorage'ında saklanır
- İnternet bağlantısı gerekli değildir (PWA desteği)
