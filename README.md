# 機器學習 — 機器學習於資產定價與選股

研究所「機器學習」課程的作業與期末專案：以機器學習方法做**股票報酬預測與投資組合建構**（empirical asset pricing）。

## 內容
### 程式（Notebooks）
| 檔案 | 說明 |
|------|------|
| `機器學習.ipynb` | 作業 HW1–HW3：資料處理、主成分迴歸 (PCR)、Sharpe ratio、因子權重估計 |
| `機器學習_期末報告.ipynb` | 期末專案：RidgeCV + XGBoost + SHAP，建構並回測選股投組 |
| `機器學習_美股.ipynb` | 美股資料前處理：yfinance 下載 ~100 檔美股(2005–2015)＋合併基本面 |

### 資料 / 產出
- 資料：`ML_Data2.xlsx`、`final_result.xlsx`
- 產出：`ridge_*` / `xgboost_*` / `rls_*` 等約 170 張特徵重要度（SHAP/PDP/permutation）與投組績效圖、CSV

### 文件
作業與報告書面檔：`機器學習HW3/HW4`、`機器學習 期末報告`（docx/pdf）、`機器學習Final Part1.pptx`

## 執行
```bash
pip install pandas numpy scikit-learn xgboost shap statsmodels matplotlib openpyxl
```
依序執行 notebook 即可。

## 注意
- ✅ 已將 notebook 內的本機絕對路徑改為**相對路徑**（`ML_Data2.xlsx`、`final_result.xlsx`），與資料同放本資料夾即可執行。
- `testing.ipynb` 為因子模型零散試算，讀取 `Downloads/` 的外部資料（未隨附），非主線程式。
- Notebook 內嵌大量圖片輸出、檔案較大（~11MB）；GitHub 可正常渲染這些結果圖，建議**保留**（清除輸出只會移除快取顯示、不影響程式碼）。

## 資料取得（大檔未隨附）
- `ML_Data2.xlsx`、`final_result.xlsx`：已隨附。
- `df_merged` / `df_merged.xlsx`（>200MB）：中間合併結果，**未隨附**；執行 notebook 的資料處理 cell 會由 `ML_Data2.xlsx` 重新產生。
- 原始資料來源：TEJ。
