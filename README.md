
# 💾 phpDbClass

Basit ve sade bir PHP veritabanı sınıfı ile PDO tabanlı veritabanı işlemlerini kolaylaştırın. **phpDbClass**, veritabanı bağlantısı, sorgu çalıştırma ve kayıt işlemlerini sade bir arayüzle sunar.

![PHP DB Class](https://img.shields.io/badge/PHP-DatabaseClass-blue)  
![License: MIT](https://img.shields.io/badge/license-MIT-green)

---

## 🚀 Özellikler

- ✅ PDO tabanlı güvenli bağlantı  
- ✅ Hazır sorgular ve dinamik veri işlemleri  
- ✅ Insert, update, delete, select işlemleri  
- ✅ Hata yakalama ve basit debug  
- ✅ Kolay yapılandırma ve kullanım

---

## 🧩 Dosya Yapısı

```
phpDbClass/
├── db.class.php         → Veritabanı sınıfı
├── example.php          → Örnek kullanım
└── README.md            → Açıklamalar
```

---

## ⚙️ Kurulum

```bash
git clone https://github.com/haktanakdag/phpDbClass.git
```

veya sadece `db.class.php` dosyasını kendi projenize ekleyin.

---

## 🧪 Kullanım

### 1. Bağlantı Başlatma

```php
require_once 'db.class.php';

$db = new DB("localhost", "veritabani_adi", "kullanici_adi", "parola");
```

### 2. SELECT Örneği

```php
$kullanicilar = $db->select("SELECT * FROM users WHERE status = ?", [1]);

foreach ($kullanicilar as $kullanici) {
    echo $kullanici['name'];
}
```

### 3. INSERT Örneği

```php
$ekle = $db->insert("INSERT INTO users (name, email) VALUES (?, ?)", ['Haktan', 'haktan@example.com']);
```

### 4. UPDATE Örneği

```php
$guncelle = $db->update("UPDATE users SET status = ? WHERE id = ?", [0, 1]);
```

### 5. DELETE Örneği

```php
$sil = $db->delete("DELETE FROM users WHERE id = ?", [2]);
```

---

## ❗ Hata Ayıklama

Sınıf içinde `$debug` özelliğini aktif ederek çalıştırılan sorguları görebilirsiniz:

```php
$db->debug = true;
```

---

## 🧰 Yapılandırma Parametreleri

| Parametre      | Açıklama            |
|----------------|---------------------|
| host           | Veritabanı sunucusu |
| dbname         | Veritabanı adı      |
| user           | Kullanıcı adı       |
| password       | Parola              |

---

## 📄 Lisans

Bu proje MIT lisansı ile lisanslanmıştır.

---

> Hazırlayan: [Haktan Akdağ](https://github.com/haktanakdag)  
> Hafif ve pratik PDO sınıfıyla veritabanı işlemleri çok kolay!
