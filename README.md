# Cloudflare Web Application Firewall Rules

Koleksi CloudFlare WAF expressions untuk meningkatkan keamanan situs web Anda dengan memblokir trafik berbahaya dan redundant.

## Overview

Repositori ini menyediakan WAF expressions yang dioptimalkan untuk Cloudflare yang membantu melindungi server asal Anda dengan filterisasi:

- Kebocoran data dan referrers yang mencurigakan
- Malicious URL paths dan user agents
- Eksploitasi dan traversal attempts
- Outdated browsers dan suspicious clients
- Bot, pemindai, dan web scrapers yang berbahaya
- Traffic dari Tor dan ASN berbahaya

## Implementasi

### Manual Setup

1. Buka dasbor Cloudflare Anda
2. Buka Security > WAF > Custom rules
3. Buat rules menggunakan ekspresi dari [expressions.md](expressions.md)
4. Terapkan action yang disarankan (Blokir atau Managed Challenge) untuk setiap set aturan

## Direkomendasikan

- Nonaktifkan “Bot Fight Mode” di pengaturan Keamanan Cloudflare untuk mencegah pemblokiran bot yang legitimate
- Mengonfigurasi perlindungan DDoS yang tepat dengan custom ruleset dan rate limiting
- Pastikan server Anda hanya menerima permintaan dari IP Cloudflare
