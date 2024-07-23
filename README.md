# Carbon Tarih ve Saat Formatlama

Carbon, PHP'nin `DateTime` sınıfını genişleterek tarih ve saat ile ilgili işlemleri daha kolay ve esnek hale getirir. Aşağıda, Carbon'un `format` metodunda kullanılabilecek tüm format karakterlerinin bir listesi bulunmaktadır.

## Tam Tarih ve Saat Formatları

| Karakter | Açıklama                 | Örnek     |
|----------|--------------------------|-----------|
| `d`      | Gün (0-31)               | 01-31     |
| `D`      | Kısa gün adı             | Mon-Sun   |
| `j`      | Gün (0-31, ön sıfırsız)  | 1-31      |
| `l` (küçük L) | Tam gün adı       | Monday    |
| `N`      | ISO-8601 haftanın günü   | 1 (Pzt)-7 (Paz) |
| `S`      | Gün sırası ek (st, nd, rd, th) | 1st, 2nd |
| `w`      | Haftanın günü (0-6)      | 0 (Paz)-6 (Cmt) |
| `z`      | Yılın günü (0-365)       | 0-365     |
| `W`      | ISO-8601 hafta numarası  | 01-53     |
| `F`      | Tam ay adı               | January-December |
| `m`      | Ay (01-12)               | 01-12     |
| `M`      | Kısa ay adı              | Jan-Dec   |
| `n`      | Ay (1-12, ön sıfırsız)   | 1-12      |
| `t`      | Ayda gün sayısı          | 28-31     |
| `L`      | Artık yıl (1 ise evet, 0 ise hayır) | 0-1 |
| `o`      | ISO-8601 yılı            | 2024      |
| `Y`      | Tam yıl                  | 2024      |
| `y`      | Kısa yıl (iki hane)      | 24        |
| `a`      | Küçük harf am/pm         | am/pm     |
| `A`      | Büyük harf AM/PM         | AM/PM     |
| `B`      | Swatch İnternet zamanı   | 000-999   |
| `g`      | Saat (1-12, ön sıfırsız) | 1-12      |
| `G`      | Saat (0-23, ön sıfırsız) | 0-23      |
| `h`      | Saat (01-12)             | 01-12     |
| `H`      | Saat (00-23)             | 00-23     |
| `i`      | Dakika (00-59)           | 00-59     |
| `s`      | Saniye (00-59)           | 00-59     |
| `u`      | Mikro saniye             | 123456    |
| `v`      | Milisaniye               | 123       |
| `e`      | Zaman dilimi tanımlayıcısı | UTC, GMT, Europe/Paris |
| `I`      | Yaz saati (1 ise evet, 0 ise hayır) | 0-1 |
| `O`      | GMT farkı (saat ve dakika) | +0200    |
| `P`      | GMT farkı (saat ve dakika, iki nokta ile) | +02:00 |
| `p`      | Lowercase am/pm         | am/pm     |
| `T`      | Zaman dilimi kısaltması  | EST, MDT  |
| `Z`      | UTC farkı (saniye cinsinden) | -43200-50400 |
| `c`      | ISO 8601 tarih          | 2004-02-12T15:19:21+00:00 |
| `r`      | RFC 2822 tarih          | Thu, 21 Dec 2000 16:01:07 +0200 |
| `U`      | Unix zaman damgası      | 1612322655 |

## Özel Karakterler

Eğer formatınızda sabit bir metin kullanmak isterseniz, bu metni ters eğik çizgi (`\`) ile kaçırabilirsiniz:

```php
$date = Carbon::now()->format('Y-m-d\TH:i:s');
echo $date; // Örnek: 2024-05-29T14:34:00
