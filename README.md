# Wikipedia Ölü Link Filtreleyici

Bu proje, Türkçe Vikipedi'de ölü dış bağlantılar içeren maddeleri tarar, bağlantıları çeker ve isteğe bağlı olarak belirli anahtar kelimelere göre filtreler.

## Özellikler

- Türkçe Vikipedi'de ölü linklerin bulunduğu sayfaları tarar.
- Bulunan ölü linkleri `links.txt` dosyasına kaydeder.
- İsteğe bağlı olarak belirli bir anahtar kelimeye göre bağlantıları filtreler ve `filter.txt` dosyasına kaydeder.
- Sayfa sayısı sınırlaması ile işlem yapılabilir.
- Tüm işlemleri `bot.log` dosyasına kaydeder.

## Gereksinimler

Bu proje için aşağıdaki bağımlılıkların kurulu olması gerekir:

- Python 3
- `requests` kütüphanesi
- `beautifulsoup4` kütüphanesi

Bağımlılıkları yüklemek için:

```bash
pip install requests beautifulsoup4
```

## Kurulum ve Kullanım

1. **Depoyu klonlayın veya indirin:**

```bash
git clone https://github.com/EnesKeremAYDIN/wikipedia-olu-link-filtreleyici.git
cd wikipedia-olu-link-filtreleyici
```

2. **Script'i çalıştırın:**

```bash
python bot.py
```

### Kullanım Adımları

1. Script çalıştırıldığında size bir filtreleme yapıp yapmayacağınızı sorar:
   - `evet`: Belirli bir anahtar kelimeye göre filtreleme yapar.
   - `hayır`: Tüm ölü bağlantıları listeler.

2. Kaç sayfanın taranacağını girin:
   - `0`: Limitsiz sayfa taraması yapar.

### Çıktılar

- **`links.txt`**: Tüm bulunan bağlantılar bu dosyada saklanır.
- **`filter.txt`**: Anahtar kelimeye göre filtrelenen bağlantılar burada saklanır (sadece filtreleme yapıldığında).
- **`bot.log`**: İşlem sürecine ait log kayıtları bu dosyada tutulur.

## Örnek Kullanım

```bash
python bot.py
Filtreleme yapmak ister misiniz? (evet-hayır): evet
Filtreleme kelimesini girin: Atatürk
Gezilecek sayfa sayısını girin (0 = limitsiz): 0
```

Bu komut, ölü bağlantıları "Python" anahtar kelimesine göre filtreler ve 5 sayfayı tarar.
