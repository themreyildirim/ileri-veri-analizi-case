# Case Study 02 — Enerji Sektörü Veri Analizi

Çalık Enerji tahsilat ve tahakkuk verileri üzerinde yapılan ileri seviye veri analizi çalışmasıdır.

## Proje Yapısı

```
case_study_02/
├── README.md
├── requirements.txt
├── data/
│   └── elektrik_veri.xlsx
├── notebooks/
│   ├── notebook_01_veri_kesfi.ipynb
│   ├── notebook_02_gorsellestirme.ipynb
│   └── notebook_03_veri_hikayesi.ipynb
└── outputs/
    └── figures/
        ├── aylik_tuketim_trendi.png
        ├── hesap_sinifi_dagilimi.png
        ├── ilce_hesap_heatmap.png
        ├── kwh_dagilim.png
        ├── mevsimsel_ilce.png
        ├── musteri_segmentasyon.png
        ├── odeme_zamanlama.png
        ├── tahsilat_ilce_sube.png
        └── tahsilat_performans.png
```

## Veri Seti

`elektrik_veri.xlsx` dosyası 5 sayfadan oluşmaktadır:

| Sayfa | Kayıt Sayısı | Açıklama |
|-------|-------------|----------|
| Tahsilat | 636.993 | Tahsilat işlem kayıtları |
| Tahsilat 1 | 917.632 | Detaylı tahsilat verileri (ödeme zamanlaması) |
| Tahakkuk | 124.818 | Tahakkuk kayıtları |
| Tahakkuk 1 | 765.657 | Tahakkuk kayıtları (devam) |
| Tahakkuk 2 | 295.223 | Tahakkuk kayıtları (devam) |

## Notebook'lar

### 1. Veri Keşfi (`notebook_01_veri_kesfi.ipynb`)
- Veri yapısı inceleme (shape, dtypes, null değerler)
- Benzersiz müşteri ve sözleşme sayıları
- Tahakkuk birleştirme
- Veri kalitesi raporu
- Hesap sınıfı bazlı tanımlayıcı istatistikler

### 2. Görselleştirme (`notebook_02_gorsellestirme.ipynb`)
- Hesap sınıfı dağılımları
- Aylık tüketim trendi
- İlçe/şube bazlı tahsilat dağılımı
- Zamanında/geç ödeme analizi
- kWh tüketim dağılımı (histogram + boxplot)

### 3. Veri Hikayesi (`notebook_03_veri_hikayesi.ipynb`)
- İlçe karşılaştırma analizi ve mevsimsel paternler
- Müşteri segmentasyonu (tüketim + ödeme davranışı)
- Tahsilat performans analizi

## Kurulum

```bash
pip install -r requirements.txt
```

## Çalıştırma

Notebook'ları sırasıyla çalıştırın. Her notebook bağımsız olarak veri yükleme yapar; sıralı çalıştırma zorunlu değildir.
