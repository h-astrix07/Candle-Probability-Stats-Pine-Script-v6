# Candle Probability Stats — Pine Script v6

Indikator TradingView untuk melihat statistik probabilitas arah candle secara real-time.

## Fitur
- Persentase Bullish / Bearish / Doji dalam N candle terakhir
- Analisis perubahan volume
- Garis tren otomatis (linear regression)
- Zona prediksi arah ke depan
- Tabel compact di pojok chart

## Cara Pakai
1. Buka Pine Script Editor di TradingView
2. Paste kode dari `candle_probability_stats.pine`
3. Klik **Add to chart**
4. Atur periode & posisi tabel via ⚙️ Settings

## Parameter
| Parameter | Default | Keterangan |
|---|---|---|
| Periode Statistik | 100 | Jumlah candle yang dihitung |
| Periode Tren | 20 | Panjang linear regression |
| Periode Volume | 10 | Perbandingan volume recent vs baseline |
| Posisi Tabel | Top Right | Sudut tampilan tabel |
| Tampilkan Garis Tren | true | On/off garis tren di chart |
| Tampilkan Prediksi | true | On/off zona prediksi |

## Logika Singkat
```
Bullish  → close > open
Bearish  → close < open
Doji     → |close - open| < 10% × (high - low)
Bias     → selisih > 5% dianggap dominan
Tren     → slope linear regression close
```

## Disclaimer
Untuk keperluan edukasi dan analisis pribadi. Bukan rekomendasi investasi.
