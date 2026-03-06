# İleri Veri Analizi – Case 3: Enerji Tüketim Verilerinde Anomali Analizi ve Operasyonel İçgörü Üretimi

## Proje Özeti
Bu çalışmada, 5 il (Samsun, Çorum, Amasya, Sinop, Ordu) genelinde 353.949 satırlık enerji tüketim verisi üzerinde kapsamlı bir anomali analizi gerçekleştirilmiştir.

## İçerik

| Dosya | Açıklama |
|-------|----------|
| `Enerji Tüketim Verilerinde Anomali Analizi ve Operasyonel İçgörü Üretimi.ipynb` | Ana analiz notebook'u (9 kural + ML tabanlı anomali tespiti, güven skoru, pivot analizler, görselleştirmeler) |
| `Enerji_Anomali_Raporu.docx` | Otomatik üretilen Word raporu (11 bölüm, 14 gömülü grafik) |
| `enerji_tuketım_verileri.csv` | Ham veri seti (~354K satır, 19 kolon) |
| `dashboard_exports/` | Dashboard için ayrı kaydedilmiş yüksek çözünürlüklü görseller (300 DPI) |

## Dashboard Görselleri

| # | Görsel | Açıklama |
|---|--------|----------|
| 1 | Anomali Türü Dağılımı | Kesişim / Sadece Kural / Sadece ML oransal dağılımı |
| 2 | Bölgesel Risk Haritası | İl-ilçe bazında anomali yoğunluğu ısı haritası |
| 3 | Günlük Anomali Trendi | Zaman içinde anomali değişiminin günlük izlenmesi |
| 4 | Yüksek Riskli Aboneler | Öncelikli müdahale gereken tesisat listesi |

## Yöntem
- **Kural Tabanlı**: 9 operasyonel kural (faz dengesizliği, gerilim sapması, gece tüketimi vb.)
- **ML Tabanlı**: Isolation Forest (n_estimators=250, contamination=0.20)
- **Güven Skoru**: Ağırlıklı bileşik skor (Kesişim %70, Sadece Kural %20, Sadece ML %10)

## Gereksinimler
```
pandas, numpy, matplotlib, seaborn, scikit-learn, python-docx
```
