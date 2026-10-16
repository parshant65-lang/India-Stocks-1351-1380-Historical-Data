# India-Stocks-1351-1380-Historical-Data

Institutional Historical 1-Minute Market Data Archive for **India Equities (Constituents 1351 to 1380)** with automated daily cloud capture via GitHub Actions.

---

## 🏛️ Directory Hierarchy

```text
India-Stocks-1351-1380-Historical-Data/
├── .github/workflows/daily_ingest.yml
├── fetch_batch.py
├── README.md
├── <SYMBOL>/
│   └── 1m/
│       ├── README.md
│       └── <YYYY>/
│           └── <MM>/
│               ├── <SYMBOL>_1m_<YYYY-MM-DD>.csv
```

---

## ⏰ 4-Tier Automated Schedule (Mon–Fri)

| Trigger | Time (IST) | Cron (UTC) | Role |
|:---|:---:|:---:|:---|
| **Primary Trigger** | **15:45 IST** | `15 10 * * 1-5` | 15 mins post-market close |
| **Backup Trigger 1** | **16:45 IST** | `15 11 * * 1-5` | 1 hour safety net |
| **Backup Trigger 2** | **17:45 IST** | `15 12 * * 1-5` | 2 hours safety net |
| **Backup Trigger 3** | **18:45 IST** | `15 13 * * 1-5` | 3 hours safety net |

---

## 📦 Constituents (1351 to 1380)

| # | Symbol | Company Name | Yahoo Ticker |
|---|---|---|---|
| 1351 | `IONEXCHANG` | ION Exchange (India) Limited | `IONEXCHANG.NS` |
| 1352 | `IPL` | India Pesticides Limited | `IPL.NS` |
| 1353 | `IPRINGLTD` | IP Rings Limited | `IPRINGLTD.NS` |
| 1354 | `IRIS` | IRIS RegTech Solutions Limited | `IRIS.NS` |
| 1355 | `IRISDOREME` | Iris Clothings Limited | `IRISDOREME.NS` |
| 1356 | `IRMENERGY` | IRM Energy Limited | `IRMENERGY.NS` |
| 1357 | `ISFT` | Intrasoft Technologies Limited | `ISFT.NS` |
| 1358 | `ISGEC` | Isgec Heavy Engineering Limited | `ISGEC.NS` |
| 1359 | `ISHANCH` | Ishan Dyes and Chemicals Limited | `ISHANCH.NS` |
| 1360 | `ISTLTD` | I S T Limited | `ISTLTD.NS` |
| 1361 | `ITDC` | India Tourism Development Corporation Limited | `ITDC.NS` |
| 1362 | `ITL` | ITL Industries Limited | `ITL.NS` |
| 1363 | `IVALUE` | Ivalue Infosolutions Limited | `IVALUE.NS` |
| 1364 | `IVC` | IL&FS Investment Managers Limited | `IVC.NS` |
| 1365 | `IVP` | IVP Limited | `IVP.NS` |
| 1366 | `IWP` | The Indian Wood Products Company Limited | `IWP.NS` |
| 1367 | `IXIGO` | Le Travenues Technology Limited | `IXIGO.NS` |
| 1368 | `IZMO` | IZMO Limited | `IZMO.NS` |
| 1369 | `JAGRAN` | Jagran Prakashan Limited | `JAGRAN.NS` |
| 1370 | `JAGSNPHARM` | Jagsonpal Pharmaceuticals Limited | `JAGSNPHARM.NS` |
| 1371 | `JAIBALAJI` | Jai Balaji Industries Limited | `JAIBALAJI.NS` |
| 1372 | `JAICORPLTD` | Jai Corp Limited | `JAICORPLTD.NS` |
| 1373 | `JAIPURKURT` | Nandani Creation Limited | `JAIPURKURT.NS` |
| 1374 | `JAMNAAUTO` | Jamna Auto Industries Limited | `JAMNAAUTO.NS` |
| 1375 | `JARO` | Jaro Institute of Technology Management and Research Limited | `JARO.NS` |
| 1376 | `JASH` | Jash Engineering Limited | `JASH.NS` |
| 1377 | `JAYAGROGN` | Jayant Agro Organics Limited | `JAYAGROGN.NS` |
| 1378 | `JAYBARMARU` | Jay Bharat Maruti Limited | `JAYBARMARU.NS` |
| 1379 | `JAYKAY` | Jaykay Enterprises Limited | `JAYKAY.NS` |
| 1380 | `JAYNECOIND` | Jayaswal Neco Industries Limited | `JAYNECOIND.NS` |


---

## ⚡ 1-Line Pandas Stream Loader

```python
import pandas as pd

# Example: Stream IONEXCHANG 1m data
url = "https://raw.githubusercontent.com/parshant65-lang/India-Stocks-1351-1380-Historical-Data/main/IONEXCHANG/1m/2026/10/IONEXCHANG_1m_2026-10-12.csv"
df = pd.read_csv(url)
print(df.head())
```
