# Tax Calculator

IBM Developer Skills Network'in eğitim projesi. ABD federal gelir vergisi hesaplama uygulaması. Modern web teknolojileri kullanılarak geliştirilmiş, kullanıcı dostu arayüze sahip vergi hesaplama aracı.

## 🎯 Proje Amacı

Bu proje, ABD federal gelir vergisi hesaplamalarını yapmak için tasarlanmış bir web uygulamasıdır. Kullanıcılar gelirlerini girerek ödeyecekleri vergi miktarını ve etkili vergi oranını hesaplayabilirler.

## ✨ Özellikler

- 💰 **Vergi Hesaplama**: ABD federal gelir vergisi hesaplama
- 📊 **Vergi Dilimleri**: 2023 vergi dilimlerini gösteren tablo
- 🎯 **Etkili Vergi Oranı**: Toplam gelir üzerinden etkili vergi oranı
- 📱 **Responsive Tasarım**: Mobil uyumlu arayüz
- 🧪 **Test Desteği**: Jasmine test framework ile test edilmiş
- 🐳 **Docker Desteği**: Containerization desteği

## 🏛️ Vergi Dilimleri (2023)

| Gelir Aralığı | Vergi Oranı |
|---------------|-------------|
| $0 - $11,000 | 10% |
| $11,001 - $44,725 | 12% |
| $44,726 - $95,375 | 22% |
| $95,376 - $182,100 | 24% |
| $182,101 - $231,250 | 32% |
| $231,251 - $578,125 | 35% |
| $578,126+ | 37% |

## 🚀 Kurulum ve Çalıştırma

### Yerel Geliştirme
1. **Projeyi klonlayın:**
   ```bash
   git clone https://github.com/SametDulger/zntwk-tax_calculator.git
   cd zntwk-tax_calculator
   ```

2. **Web sunucusu başlatın:**
   ```bash
   # Python ile
   python -m http.server 8000
   
   # Node.js ile
   npx http-server
   ```

3. **Tarayıcıda açın:**
   ```
   http://localhost:8000
   ```

### Docker ile Çalıştırma
```bash
# Docker image oluşturun
docker build -t tax-calculator .

# Container'ı çalıştırın
docker run -p 8080:80 tax-calculator
```

## 🧪 Test Çalıştırma
```bash
# Testleri çalıştırın
npm test
```

## 📁 Proje Yapısı

```
zntwk-tax_calculator/
├── index.html              # Ana HTML dosyası
├── style.css               # CSS stilleri
├── script.js               # Ana JavaScript dosyası
├── taxCalculator.js        # Vergi hesaplama mantığı
├── spec/
│   └── taxCalculator.spec.js  # Test dosyaları
├── Dockerfile              # Docker konfigürasyonu
├── package.json            # Proje bağımlılıkları
├── favicon.ico             # Site ikonu
└── README.md               # Bu dosya
```

## 🛠️ Kullanılan Teknolojiler

- **HTML5**: Yapısal markup
- **CSS3**: Stil ve düzen
- **JavaScript (ES6)**: İnteraktif işlevsellik
- **Bootstrap 5**: Responsive UI framework
- **jQuery**: DOM manipülasyonu
- **Jasmine**: Test framework
- **Docker**: Containerization
- **Nginx**: Web sunucusu

## 📖 Kullanım

1. **Gelir Girin**: "Your Total Income" alanına yıllık gelirinizi yazın
2. **Hesapla**: "Calculate" butonuna tıklayın
3. **Sonuçları Görün**: 
   - Tax due: Ödeyeceğiniz vergi miktarı
   - Effective Tax Rate: Etkili vergi oranınız
   - Vergi dilimleri tablosu

## 🔧 Teknik Detaylar

### Vergi Hesaplama Algoritması
```javascript
// Vergi dilimleri ve birikmiş vergiler
let tax_brackets = [
    { lower: null, higher: 11000, percentage: 0.1, accumulatedTax: 0 },
    { lower: 11001, higher: 44725, percentage: 0.12, accumulatedTax: 1100 },
    // ... diğer dilimler
]
```

### Örnek Hesaplama
- **Gelir**: $50,000
- **Vergi**: $6,146.88
- **Etkili Oran**: %12.29

## 🧪 Test Kapsamı

Jasmine test framework ile aşağıdaki senaryolar test edilir:
- Farklı gelir seviyeleri için vergi hesaplama
- Vergi dilimi sınırları
- Hesaplama doğruluğu

## 🤝 Katkıda Bulunma

Bu proje eğitim amaçlı geliştirilmiştir. Katkıda bulunmak için:

1. Fork yapın
2. Feature branch oluşturun
3. Değişikliklerinizi commit edin
4. Pull request gönderin

## 📄 Lisans

Bu proje [Apache License 2.0](LICENSE) lisansı altında lisanslanmıştır.

**Copyright 2023 IBM Developer Skills Network**

## ⚠️ Önemli Not

Bu uygulama sadece eğitim amaçlıdır. Gerçek vergi hesaplamaları için profesyonel vergi danışmanlarına başvurunuz.

## 🔗 İlgili Kaynaklar

- [IBM Developer Skills Network](https://skills.network/)
- [IRS Tax Brackets](https://www.irs.gov/filing/federal-income-tax-rates-and-brackets)
- [Bootstrap Documentation](https://getbootstrap.com/)
- [Jasmine Testing](https://jasmine.github.io/)

---

IBM Developer Skills Network'in eğitim materyali olarak geliştirilmiştir. 🚀
