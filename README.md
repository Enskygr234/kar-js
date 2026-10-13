<div align="center">

![kar.js](docs/afis.svg)

[![Canlı demo](https://img.shields.io/badge/Canlı_demo-dene-8ecae6?style=for-the-badge)](https://enskygr234.github.io/kar-js/)
[![Sürüm](https://img.shields.io/github/v/tag/Enskygr234/kar-js?style=for-the-badge&label=sürüm&color=219ebc)](https://github.com/Enskygr234/kar-js/tags)
[![Lisans](https://img.shields.io/badge/lisans-MIT-e63946?style=for-the-badge)](LICENSE)

</div>

Web sayfana tek satırla kar yağdıran küçük bir JavaScript kütüphanesi. Tek dosya, bağımlılık yok, sıkıştırılınca yaklaşık 3 KB.

**[→ Canlı demoyu aç](https://enskygr234.github.io/kar-js/)** — ayarlarla oyna, hazır kodu kopyala.

## Hızlı başlangıç

Sayfanın sonuna şunu ekle, kar yağmaya başlar:

```html
<script src="https://cdn.jsdelivr.net/gh/Enskygr234/kar-js@v1.0.0/kar.js" data-kar></script>
```

Ayar vermek istersen öznitelik olarak yaz:

```html
<script src="https://cdn.jsdelivr.net/gh/Enskygr234/kar-js@v1.0.0/kar.js"
        data-kar data-adet="300" data-ruzgar="-1" data-renk="#cfe8ff"></script>
```

## JavaScript ile kullanım

```html
<script src="kar.js"></script>
<script>
  const kar = Kar.baslat({ adet: 250, hiz: 1.5, ruzgar: 0.8 });

  kar.durdur();                 // dondur
  kar.devam();                  // sürdür
  kar.ayarla({ adet: 600 });    // çalışırken değiştir
  kar.kaldir();                 // tamamen sök
</script>
```

Yalnızca bir kutunun içine yağdırmak için `hedef` ver:

```js
Kar.baslat({ hedef: document.querySelector('.afis'), adet: 80 });
```

## Ayarlar

| Ayar | Varsayılan | Açıklama |
|---|---|---|
| `adet` | `150` | Ekrandaki kar tanesi sayısı |
| `hiz` | `1` | Düşme hızı çarpanı |
| `ruzgar` | `0.3` | Rüzgâr; eksi değer sola, artı değer sağa savurur |
| `renk` | `'#ffffff'` | Kar rengi |
| `enKucuk` | `1` | En küçük tanenin yarıçapı (px) |
| `enBuyuk` | `3.6` | En büyük tanenin yarıçapı (px) |
| `fare` | `true` | Taneler imleçten kaçsın mı |
| `hedef` | `null` | Verilirse yalnızca o elementin içine yağar |
| `zIndex` | `9999` | Kar katmanının sırası |
| `zorla` | `false` | "Hareketi azalt" ayarı açık olsa bile yağdır |

## İncelikler

- **Tıklamaları engellemez.** Kar katmanı fare olaylarını geçirir; sayfan eskisi gibi çalışır.
- **Sekme arkadayken durur.** Görünmeyen sekmede işlemci harcamaz.
- **Hareket hassasiyetine saygılı.** İşletim sisteminde "hareketi azalt" açıksa kar hareketsiz çizilir.
- **Derinlik hissi.** Yakın taneler büyük, parlak ve hızlı; uzaktakiler küçük, soluk ve yavaş.

## Geliştirme

Derleme adımı yok. Depoyu indir, `index.html` dosyasını tarayıcıda aç.

## Lisans

[MIT](LICENSE) © Winterdeveloper
