# 機器學習 — 機器學習於資產定價與選股

研究所「機器學習」課程的作業與期末專案：以機器學習方法做**股票報酬預測與投資組合建構**（empirical asset pricing）。

## 結構
```text
機器學習.ipynb              作業 HW1–HW4（PCR、Sharpe、因子權重、邏輯迴歸）
機器學習_期末報告.ipynb     期末專案（RidgeCV + XGBoost + SHAP 選股回測）
機器學習_美股.ipynb         美股資料前處理（yfinance）
data/                       輸入資料（ML_Data.xlsx、ML_Data2.xlsx、ETF 等權縫效）
figures/                    產出圖檔（SHAP / PDP / permutation 重要度、投組績效，共 174 張）
results/                    產出數據（投組與績效 CSV、final_result.xlsx、score_summary 等）
docs/                       作業與報告（docx / pdf / pptx）
```

## 內容
| Notebook | 說明 |
|------|------|
| `機器學習.ipynb` | 作業 HW1–HW4：資料處理、主成分迴歸 (PCR)、Sharpe ratio、因子權重估計、邏輯迴歸 |
| `機器學習_期末報告.ipynb` | 期末專案：RidgeCV + XGBoost + SHAP，建構並回測選股投組 |
| `機器學習_美股.ipynb` | 美股資料前處理：yfinance 下載 ~100 檔美股(2005–2015)＋合併基本面 |

## 執行
```bash
pip install pandas numpy scikit-learn xgboost shap statsmodels matplotlib openpyxl yfinance
```
- `機器學習.ipynb`／`機器學習_期末報告.ipynb`：讀 `data/ML_Data2.xlsx`，產出寫入 `results/`、`figures/`，可直接執行。
- `機器學習_美股.ipynb`：需自備輸入（原以 Colab `/mnt/data/` 上傳），輸出 `results/SP100_data.xlsx`。

## 資料取得（大檔未隨附）
- `data/ML_Data2.xlsx`：已隨附；`results/final_result.xlsx` 由 notebook 產生。
- `df_merged.xlsx`（>200MB）：中間合併結果，**未隨附**，由 `data/ML_Data2.xlsx` 重新產生。
- 原始資料來源：TEJ。
