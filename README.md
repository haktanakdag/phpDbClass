
# 📊 PHPReportingClass

PHP ile HTML tabanlı raporlar oluşturmanın kolay ve hafif yolu: **PHPReportingClass**. Bu sınıf, dinamik olarak tablo oluşturmanızı sağlar ve sade arayüzüyle esnek bir yapı sunar.

![PHP Reporting Class](https://img.shields.io/badge/PHP-ReportingClass-blue)  
![License: MIT](https://img.shields.io/badge/license-MIT-green)

---

## ✨ Özellikler

- ✅ Dinamik HTML tablo üretimi  
- ✅ Kolay entegre edilebilir sınıf yapısı  
- ✅ Header ve veri seti tanımlama  
- ✅ Özelleştirilebilir CSS sınıfları  
- ✅ Hafif ve sade çözüm

---

## 📁 Dosya Yapısı

```
PHPReportingClass/
├── example.php          → Örnek kullanım dosyası
├── Reporting.php        → Ana sınıf dosyası
└── README.md            → Açıklama ve yönergeler
```

---

## ⚙️ Kurulum

Projeyi klonlayın veya doğrudan `Reporting.php` dosyasını projenize ekleyin:

```bash
git clone https://github.com/haktanakdag/PHPReportingClass.git
```

Kullanım için:

```php
require_once 'Reporting.php';
```

---

## 🚀 Hızlı Başlangıç

### 1. Sınıfı başlat

```php
$report = new Reporting();
```

### 2. Başlıkları tanımla

```php
$report->setHeaders(['ID', 'İsim', 'Soyisim', 'E-posta']);
```

### 3. Verileri ekle

```php
$data = [
    [1, 'Haktan', 'Akdağ', 'haktan@example.com'],
    [2, 'Ayşe', 'Yılmaz', 'ayse@example.com'],
];
$report->setRows($data);
```

### 4. Raporu oluştur

```php
echo $report->render();
```

---

## 💡 Örnek HTML Çıktı

```html
<table class="reporting-table">
  <thead>
    <tr>
      <th>ID</th>
      <th>İsim</th>
      <th>Soyisim</th>
      <th>E-posta</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>1</td>
      <td>Haktan</td>
      <td>Akdağ</td>
      <td>haktan@example.com</td>
    </tr>
  </tbody>
</table>
```

---

## 🎨 Stil Özelleştirme

```php
$report->setTableClass('table table-striped');
$report->setHeaderClass('header');
$report->setRowClass('row');
```

Varsayılan CSS örneği:

```css
.reporting-table {
  width: 100%;
  border-collapse: collapse;
}
.reporting-table th, .reporting-table td {
  padding: 8px;
  border: 1px solid #ccc;
}
.reporting-table th {
  background-color: #f2f2f2;
}
```

---

## 🤝 Katkı

1. Fork oluşturun  
2. Yeni bir branch açın (`feature/yenilik`)  
3. Değişiklikleri commit'leyin  
4. Pull request gönderin

---

## 📄 Lisans

MIT Lisansı ile lisanslanmıştır. Detaylar için `LICENSE` dosyasına bakın.

---

> Hazırlayan: [Haktan Akdağ](https://github.com/haktanakdag)
