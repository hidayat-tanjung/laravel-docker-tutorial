# 🐳 Laravel Docker Tutorial

[![Version](https://img.shields.io/badge/version-1.0-red.svg)](https://github.com/hidayat-tanjung/laravel-docker-tutorial)
[![License](https://img.shields.io/badge/license-MIT-blue.svg)](https://opensource.org/licenses/MIT)
[![Docker](https://img.shields.io/badge/docker-ready-blue.svg)](https://www.docker.com/)
[![PHP](https://img.shields.io/badge/php-8.1-purple.svg)](https://www.php.net/)
[![Laravel](https://img.shields.io/badge/laravel-9.x-red.svg)](https://laravel.com/)
[![GitHub](https://img.shields.io/badge/github-repo-181717.svg)](https://github.com/hidayat-tanjung/laravel-docker-tutorial)

---

## 📋 Deskripsi

**Laravel Docker Tutorial** adalah panduan langkah demi langkah untuk menginstal dan menjalankan **Laravel** menggunakan **Docker**. Tutorial ini mencakup instalasi PHP 8.1, Composer, dan inisiasi project Laravel di dalam container Docker. Cocok untuk developer yang ingin belajar containerisasi aplikasi Laravel.

---

## 🚀 Fitur

| No | Fitur | Status |
|----|-------|--------|
| 1 | Instalasi PHP 8.1 di Docker | ✅ |
| 2 | Instalasi Composer di Docker | ✅ |
| 3 | Inisiasi Project Laravel | ✅ |
| 4 | Panduan langkah demi langkah | ✅ |
| 5 | Cocok untuk pemula | ✅ |

---


---

## 📚 Panduan Lengkap

### 1. Instalasi PHP 8.1

```bash
# Pull image PHP 8.1
docker pull php:8.1-fpm
```

### Jalankan container
```bash
docker run -d --name php81 -p 9000:9000 php:8.1-fpm
```


### Cek versi PHP

```bash
docker exec -it php81 php -v
```

### 2 Instalasi Composer
# Download Composer
```bash
docker exec -it php81 curl -sS https://getcomposer.org/installer | php
```

# Install Composer
```bash
docker exec -it php81 php composer.phar
```

# Pindahkan ke global
```bash
docker exec -it php81 mv composer.phar /usr/local/bin/composer
```
### 3. Inisiasi Project Laravel
# Buat project Laravel
```bash
docker exec -it php81 composer create-project laravel/laravel /var/www/html
```

# Install dependencies
```bash
docker exec -it php81 composer install
```

# Run migration
```bash
docker exec -it php81 php artisan migrate
```

# Start server
```bash
docker exec -it php81 php artisan serve --host=0.0.0.0
```

### 🚀 Cara Cepat (Docker Compose)
# Clone repository
```bash
git clone https://github.com/hidayat-tanjung/laravel-docker-tutorial.git
cd laravel-docker-tutorial
```

# Jalankan docker-compose (contoh)
```bash
docker-compose up -d
```

# Buka browser
```bash
http://localhost:8000
```

Konten:

1. [Instalasi PHP 8.1](./Instalasi%20PHP%208/)
2. [Instalasi Composer](./Instalasi%20Composer/)
3. [Inisiasi Project Laravel](./Instalasi%20Laravel/)

### 📄 Lisensi
MIT License – silakan digunakan, dimodifikasi, dan didistribusikan.

### 👤 Author
hidayat-tanjung (イズミー)

- GitHub: https://github.com/hidayat-tanjung

- Project: https://github.com/hidayat-tanjung/laravel-docker-tutorial
