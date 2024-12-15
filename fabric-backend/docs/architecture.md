## 📁 Klasör Yapısı

Fabric Management Backend, aşağıdaki gibi modüler ve düzenli bir yapıya sahiptir:

```plaintext
fabric-backend/
├── app/               # Uygulamanın ana kodları
│   ├── api/           # API endpoint'leri
│   ├── core/          # Ayarlar ve altyapı
│   ├── models/        # Veritabanı modelleri
│   ├── schemas/       # Pydantic şemaları
│   ├── security/      # Güvenlik işlemleri (JWT, kimlik doğrulama)
│   ├── services/      # İş mantığı (business logic)
│   ├── static/        # Statik dosyalar (favicon, HTML)
│   └── utils/         # Yardımcı fonksiyonlar
├── docs/              # Dokümantasyon
├── migrations/        # Veritabanı migration dosyaları
├── scripts/           # Faydalı scriptler (veritabanı sıfırlama vb.)
├── tests/             # Test dosyaları
└── README.md          # Genel proje açıklaması
```
[Go To Index 🗂️](welcome.md#-index)