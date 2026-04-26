<div align="center">

<!-- ANIMATED BANNER -->
<img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=6,12,20&height=200&section=header&text=RT-IoT2022%20%7C%20Network%20Flow%20Prediction&fontSize=34&fontColor=ffffff&animation=fadeIn&fontAlignY=38&desc=Predicting%20Flow%20Duration%20in%20Real-Time%20IoT%20Environments&descAlignY=58&descSize=15" width="100%"/>

<!-- ANIMATED TYPING -->
<a href="https://git.io/typing-svg"><img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=22&pause=1000&color=3B82F6&center=true&vCenter=true&width=700&lines=CatBoost+R%C2%B2+%3D+0.9761+%E2%80%94+Best+Model+%F0%9F%8F%86;6+Algorithms+%C3%97+4+Variations+%3D+24+Configs;50+%E2%86%92+4+Features+via+4-Stage+Pipeline;LSTM+%7C+1D-CNN+%7C+XGBoost+%7C+LightGBM+%7C+CatBoost;Supervised+Regression+%7C+123%2C117+IoT+Flows" alt="Typing SVG" /></a>

<br/>

<!-- CORE TECH BADGES -->
<img src="https://img.shields.io/badge/Python-3.10+-3776AB?style=for-the-badge&logo=python&logoColor=white"/>
<img src="https://img.shields.io/badge/TensorFlow-2.x-FF6F00?style=for-the-badge&logo=tensorflow&logoColor=white"/>
<img src="https://img.shields.io/badge/Scikit--Learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white"/>
<img src="https://img.shields.io/badge/Google%20Colab-F9AB00?style=for-the-badge&logo=googlecolab&logoColor=white"/>

<br/>

<!-- PROJECT BADGES -->
<img src="https://img.shields.io/badge/Dataset-RT--IoT2022-8A2BE2?style=for-the-badge&logo=databricks&logoColor=white"/>
<img src="https://img.shields.io/badge/UCI%20ML%20Repo-ID%20942-0052CC?style=for-the-badge&logo=academia&logoColor=white"/>
<img src="https://img.shields.io/badge/Records-123%2C117-10B981?style=for-the-badge&logoColor=white"/>
<img src="https://img.shields.io/badge/Features-50-F59E0B?style=for-the-badge&logoColor=white"/>
<img src="https://img.shields.io/badge/License-CC%20BY%204.0-green?style=for-the-badge&logo=creativecommons&logoColor=white"/>

<br/><br/>

<!-- RESULT HIGHLIGHT BADGES -->
<img src="https://img.shields.io/badge/Best%20R%C2%B2-0.9761-brightgreen?style=flat-square"/>
<img src="https://img.shields.io/badge/Best%20RMSE-2.714s-blue?style=flat-square"/>
<img src="https://img.shields.io/badge/Best%20MAE-0.243s-blue?style=flat-square"/>
<img src="https://img.shields.io/badge/Configurations-24-purple?style=flat-square"/>
<img src="https://img.shields.io/badge/Train%20Split-80%25-orange?style=flat-square"/>
<img src="https://img.shields.io/badge/Test%20Split-20%25-red?style=flat-square"/>

</div>

---

<img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif" width="100%">

## 🧠 About This Project

> **Module:** CMP7239 — Applied Machine Learning &nbsp;|&nbsp; **Institution:** Birmingham City University &nbsp;|&nbsp; **Student:** Jatin Kumar · `25171403` &nbsp;|&nbsp; **Year:** 2025–26

This project tackles **supervised regression** on the **RT-IoT2022** dataset — predicting `flow_duration` (how long a network flow lasts, in seconds) across 123,117 real-world IoT connections. Accurate duration prediction matters for network resource allocation, Quality of Service enforcement, and anomaly detection in IoT environments.

The study evaluates **6 algorithms** across **4 feature-selection variations**, producing a **24-configuration performance matrix**. The headline finding: **CatBoost achieves R² = 0.9761** on the full feature set, while gradient boosting catastrophically fails (R² < −12) on ultra-sparse features where a simple Elastic Net thrives with R² = 0.928.

<img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif" width="100%">

## 📁 Repository Structure

```
rt-iot2022-flow-prediction/
│
├── 📓 RT_IoT2022_Publication_Notebook.ipynb   ← Main Colab notebook (start here)
│
├── 📦 saved_models/
│   ├── catboost_v1.cbm          ← Best model (R² = 0.9761)
│   ├── catboost_v2.cbm
│   ├── catboost_v3.cbm
│   ├── catboost_v4.cbm
│   ├── xgboost_v{1-4}.pkl
│   ├── lightgbm_v{1-4}.pkl
│   ├── elasticnet_v{1-4}.pkl    ← elasticnet_v4 = best on 4 features (R²=0.928)
│   ├── lstm_v{1-4}.keras
│   ├── cnn1d_v{1-4}.keras
│   ├── results.csv              ← All 24 configuration results
│   ├── feature_variations.pkl   ← V1/V2/V3/V4 feature lists
│   ├── encoders.pkl             ← LabelEncoders (proto + service)
│   └── mi_scores.csv            ← Mutual information rankings
│
├── 📊 figures/                  ← 14 publication figures (300 DPI PNG)
│   ├── fig1_target_analysis.png
│   ├── fig3_correlation_heatmap.png
│   ├── fig6_feature_selection.png
│   ├── fig7_r2_heatmap.png
│   └── ... (14 total)
│
└── 📄 README.md
```

<img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif" width="100%">

## 🚀 Quick Start

<details>
<summary><b>🔵 Option 1 — Google Colab (Recommended)</b></summary>
<br/>

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/YOUR_USERNAME/rt-iot2022-flow-prediction/blob/main/RT_IoT2022_Publication_Notebook.ipynb)

1. Click the badge to open in Colab
2. Upload the dataset when prompted: `rt_iot2022_regression_ready_50_features.csv`
3. Set **Runtime → GPU (T4)** for faster deep learning
4. **Run All** — full pipeline completes in ~30 minutes

> Dataset: [UCI ML Repository ID: 942](https://archive.ics.uci.edu/dataset/942/rt-iot2022)

</details>

<details>
<summary><b>🟣 Option 2 — Load Pre-Trained Models</b></summary>
<br/>

```python
import joblib, catboost, pandas as pd

# Load best model — CatBoost V1 (R² = 0.9761)
model = catboost.CatBoostRegressor()
model.load_model("saved_models/catboost_v1.cbm")

# Load supporting files
encoders  = joblib.load("saved_models/encoders.pkl")
feat_vars = joblib.load("saved_models/feature_variations.pkl")
v1_feats  = feat_vars["V1: All Features"]   # 50 features

# Preprocess & predict
df = pd.read_csv("your_iot_data.csv")
df["proto"]   = encoders["proto"].transform(df["proto"])
df["service"] = encoders["service"].transform(df["service"])
preds = model.predict(df[v1_feats])
print(preds)
```

</details>

<details>
<summary><b>🟢 Option 3 — Local Jupyter</b></summary>
<br/>

```bash
git clone https://github.com/YOUR_USERNAME/rt-iot2022-flow-prediction.git
cd rt-iot2022-flow-prediction

pip install xgboost lightgbm catboost scikit-learn tensorflow \
            pandas numpy matplotlib seaborn scipy joblib

jupyter notebook RT_IoT2022_Publication_Notebook.ipynb
```

</details>

<img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif" width="100%">

## 📊 Dataset: RT-IoT2022

<div align="center">

| Property | Value |
|:---|:---|
| **Source** | UCI Machine Learning Repository (ID: 942) |
| **Authors** | Sharmila B.S. & Nagapadma R. (2023) |
| **Records** | 123,117 bidirectional network flows |
| **Numeric Features** | 48 |
| **Categorical Features** | 2 (`proto`, `service`) |
| **Target** | `flow_duration` (seconds, continuous) |
| **Missing Values** | 0 — dataset is complete |
| **Duplicate Records** | 5,202 |
| **Licence** | Creative Commons Attribution 4.0 |

</div>

**IoT devices captured:** ThingSpeak-LED · Wipro-Bulb · MQTT-Temp · Amazon Alexa · Raspberry Pi  
**Attack types included:** Brute-Force SSH · DDoS-ICMP · DDoS-TCP · DDoS-UDP · Nmap Scanning  
**Capture tool:** Zeek Network Monitor + CICFlowmeter (bidirectional flow features)

**Protocol distribution:**
```
TCP   ████████████████████████████████████  89.7%  (110,427 records)
UDP   ████                                  10.3%  ( 12,633 records)
ICMP  ▏                                      0.05% (     57 records)
```

### ⚠️ Target Variable: Why It's Hard

```
Statistic        Raw Value          After log1p Transform
─────────────────────────────────────────────────────────
Mean             3.81 seconds       0.20
Median           0.000004 seconds   0.000004      ← 6 orders of magnitude gap!
Skewness         120.96             4.43          ← Extreme → manageable
Kurtosis         16,604.65          19.70         ← Heavy-tailed → reduced
Maximum          21,728 seconds     9.98          ← ~6 hour flows exist
Zeros            ~13% of records    —
```

<img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif" width="100%">

## 🔬 4-Stage Feature Selection Pipeline

```
╔══════════════════════════════════════════════════════════════════════╗
║                  FEATURE SELECTION PIPELINE                         ║
╠════════╦══════════╦══════════╦════════════════════════════════════╣
║ Stage  ║ Features ║ Removed  ║ Method & Rationale                 ║
╠════════╬══════════╬══════════╬════════════════════════════════════╣
║ Input  ║    50    ║    —     ║ Raw dataset                        ║
║ S1→V2  ║    46    ║    4     ║ Variance Threshold (>98% constant) ║
║ S2→V2  ║    35    ║   11     ║ Pearson Correlation  |r| > 0.95    ║
║ S3→V3  ║    35    ║    0     ║ Mutual Information   MI > 0.1      ║
║ S4→V4  ║     4    ║   31     ║ Lasso Path  alpha = 0.145062       ║
╚════════╩══════════╩══════════╩════════════════════════════════════╝
```

**4 Dataset Variations evaluated across all 6 models:**

| Variation | Features | Key Detail |
|-----------|:--------:|------------|
| **V1** | 50 | Full baseline — all features |
| **V2** | 35 | After removing 4 constants + 11 collinear features |
| **V3** | 35 | Same as V2 — all 35 pass MI > 0.1 (no additional removal) |
| **V4** |  4 | `fwd_iat.tot` · `bwd_iat.min` · `bwd_iat.max` · `bwd_pkts_payload.min` |

**Top features by Mutual Information:**
```
Rank  Feature                  MI Score   Note
───────────────────────────────────────────────────────────
 1    fwd_pkts_per_sec          2.234     Top MI scorer
 2    fwd_iat.tot               1.127     r=0.9997 with target ⚠️
 3    flow_pkts_payload.avg     0.972
 4    flow_pkts_payload.std     0.959
 5    fwd_iat.avg               0.911
```

<img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif" width="100%">

## 🤖 The 6 Algorithms

### Machine Learning

<table>
<tr>
<td width="50%">

**🚀 XGBoost** — Chen & Guestrin (2016)
```python
XGBRegressor(
    n_estimators=300, max_depth=8,
    learning_rate=0.1, subsample=0.8,
    colsample_bytree=0.8,
    reg_alpha=0.1, reg_lambda=1.0
)
```
Second-order gradient optimisation with L1/L2 regularisation. Sparsity-aware split-finding.

</td>
<td width="50%">

**⚡ LightGBM** — Ke et al. (2017)
```python
LGBMRegressor(
    n_estimators=300, max_depth=8,
    learning_rate=0.1, subsample=0.8,
    colsample_bytree=0.8,
    reg_alpha=0.1, reg_lambda=1.0
)
```
Histogram-based binning. Leaf-wise growth with GOSS + EFB.

</td>
</tr>
<tr>
<td>

**🏆 CatBoost** — Prokhorenkova et al. (2018)
```python
CatBoostRegressor(
    iterations=300, depth=8,
    learning_rate=0.1, l2_leaf_reg=3,
    verbose=0
)
```
Ordered boosting prevents prediction shift. Symmetric trees constrain complexity.

</td>
<td>

**📐 Elastic Net** — Zou & Hastie (2005)
```python
ElasticNet(
    alpha=0.1, l1_ratio=0.5,
    max_iter=10000
)
# StandardScaler applied beforehand
```
L1 + L2 combined regularisation. Linear baseline — best on V4 (Lasso features).

</td>
</tr>
</table>

### Deep Learning

<table>
<tr>
<td width="50%">

**🧠 LSTM** — Hochreiter & Schmidhuber (1997)
```
Input → Reshape(n_feat, 1)
      → LSTM(64, return_seq=True)
      → Dropout(0.2)
      → LSTM(32)
      → Dropout(0.2)
      → Dense(16, relu)
      → Dense(1)          ← output
```
Adam · EarlyStopping(10) · ReduceLROnPlateau · 50 epochs · batch 256

</td>
<td width="50%">

**👁️ 1D-CNN** — LeCun et al. (1998)
```
Input → Reshape(n_feat, 1)
      → Conv1D(64, k=3) + BN
      → MaxPool1D(2)
      → Conv1D(32, k=3) + BN
      → Flatten
      → Dense(32, relu) + Dropout(0.3)
      → Dense(1)          ← output
```
Adam · EarlyStopping(10) · ReduceLROnPlateau · 50 epochs · batch 256

</td>
</tr>
</table>

> ❌ **Excluded by design:** Decision Tree · Random Forest · K-Nearest Neighbours · MLP · DNN / ANN

<img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif" width="100%">

## 📐 Evaluation Metrics

| Metric | Formula | Role | Direction |
|--------|---------|------|-----------|
| **R²** | `1 − SS_res / SS_tot` | Primary | ↑ Higher is better (1.0 = perfect) |
| **RMSE** | `√(Σ(y−ŷ)² / n)` | Error in seconds | ↓ Lower is better |
| **MAE** | `Σ\|y−ŷ\| / n` | Robust error | ↓ Lower is better |
| **MSE** | `Σ(y−ŷ)² / n` | Loss function | ↓ Lower is better |
| **MAPE** | `mean(\|y−ŷ\|/\|y\|) × 100` | Scale-free % | ↓ Lower is better |

> **Note:** MAPE diverges near zero-valued targets. Masked for `\|y\| < 1e-8` in this dataset.

<img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif" width="100%">

## 📈 Results

### Complete 24-Configuration Matrix

<details open>
<summary><b>All results — click to collapse</b></summary>
<br/>

| Variation | Model | R² | RMSE (s) | MAE (s) | MSE | Train R² | Time |
|-----------|-------|:---:|:---:|:---:|:---:|:---:|:---:|
| V1 — 50 feat | **CatBoost** 🥇 | **0.9761** | **2.714** | **0.243** | 7.37 | 0.9999 | 12.8s |
| V1 — 50 feat | LSTM | 0.8819 | 6.039 | 0.596 | 36.46 | 0.4918 | 183.6s |
| V1 — 50 feat | Elastic Net | 0.8127 | 7.603 | 0.564 | 57.80 | 0.9947 | 3.5s |
| V1 — 50 feat | XGBoost | 0.6574 | 10.284 | 0.192 | 105.75 | 1.0000 | 4.1s |
| V1 — 50 feat | LightGBM | −1.888 | 29.856 | 1.030 | 891.41 | 0.9175 | 3.2s |
| V1 — 50 feat | 1D-CNN | −3.894 | 38.864 | 2.532 | 1510.37 | 0.7446 | 32.5s |
| V2 — 35 feat | **CatBoost** 🥈 | **0.9715** | 2.965 | 0.308 | 8.79 | 0.9999 | 10.1s |
| V2 — 35 feat | Elastic Net | 0.8224 | 7.403 | 0.556 | 54.80 | 0.9947 | 0.5s |
| V2 — 35 feat | XGBoost | 0.4291 | 13.274 | 0.228 | 176.21 | 0.9999 | 4.6s |
| V2 — 35 feat | LSTM | 0.2552 | 15.161 | 2.445 | 229.86 | 0.0079 | 50.1s |
| V2 — 35 feat | LightGBM | −2.253 | 31.685 | 1.010 | 1003.94 | 0.8849 | 3.0s |
| V2 — 35 feat | 1D-CNN | −6.769 | 48.965 | 3.136 | 2397.62 | 0.7495 | 31.8s |
| V3 — 35 feat | **CatBoost** 🥉 | **0.9504** | 3.912 | 0.350 | 15.31 | 0.9999 | 10.0s |
| V3 — 35 feat | Elastic Net | 0.8224 | 7.403 | 0.555 | 54.81 | 0.9947 | 0.5s |
| V3 — 35 feat | XGBoost | 0.7555 | 8.687 | 0.161 | 75.46 | 0.9999 | 3.1s |
| V3 — 35 feat | 1D-CNN | 0.3942 | 13.674 | 3.051 | 186.97 | 0.3219 | 29.4s |
| V3 — 35 feat | LSTM | 0.2724 | 14.985 | 2.091 | 224.56 | 0.0080 | 50.2s |
| V3 — 35 feat | LightGBM | −2.165 | 31.254 | 1.056 | 976.79 | 0.8851 | 3.1s |
| V4 — 4 feat | **Elastic Net** ⭐ | **0.9282** | 4.707 | 0.267 | 22.15 | 0.9974 | 0.0s |
| V4 — 4 feat | 1D-CNN | 0.5838 | 11.334 | 3.521 | 128.46 | 0.9705 | 31.7s |
| V4 — 4 feat | LSTM | 0.2696 | 15.014 | 1.768 | 225.41 | 0.0068 | 38.6s |
| V4 — 4 feat | XGBoost | −12.090 | 63.561 | 1.304 | 4039.97 | 0.8677 | 1.9s |
| V4 — 4 feat | CatBoost | −17.378 | 75.312 | 1.205 | 5671.91 | 0.7566 | 4.0s |
| V4 — 4 feat | LightGBM | −20.320 | 81.117 | 2.433 | 6580.01 | 0.5767 | 2.2s |

> 🥇🥈🥉 = Top 3 overall · ⭐ = Best per variation (V4) · Negative R² = worse than mean baseline

</details>

### Performance at a Glance

```
┌─────────────────────────────────────────────────────────────────────┐
│                    BEST PER VARIATION                               │
├───────────────┬─────────────┬────────┬──────────────────────────── │
│  Variation    │  Algorithm  │   R²   │  Visual                     │
├───────────────┼─────────────┼────────┼──────────────────────────── │
│  V1 (50 feat) │  CatBoost   │ 0.9761 │ ████████████████████ 97.6% │
│  V2 (35 feat) │  CatBoost   │ 0.9715 │ ███████████████████▋ 97.2% │
│  V3 (35 feat) │  CatBoost   │ 0.9504 │ ███████████████████  95.0% │
│  V4 ( 4 feat) │ Elastic Net │ 0.9282 │ ██████████████████▌  92.8% │
├───────────────┴─────────────┴────────┴──────────────────────────── │
│  EDGE PICK:  CatBoost V2  →  R²=0.972, 35 features, ΔR²=0.004    │
└─────────────────────────────────────────────────────────────────────┘
```

### 💥 The V4 Paradox

The most surprising finding in this study:

```
With only 4 features (Lasso-selected temporal IAT features):

  GRADIENT BOOSTING COLLAPSES:      LINEAR MODEL THRIVES:
  ┌──────────────────────────┐      ┌──────────────────────────┐
  │ XGBoost   R² = −12.090  │      │ Elastic Net  R² = 0.9282 │
  │ CatBoost  R² = −17.378  │      │ RMSE = 4.707 seconds     │
  │ LightGBM  R² = −20.320  │      │ 0.0s training time!      │
  └──────────────────────────┘      └──────────────────────────┘
```

**Why this happens:** Lasso selects features that relate near-linearly to `flow_duration`. These 4 features give Elastic Net everything it needs — but leave tree-based models with no diversity for meaningful splits. The interaction between algorithm architecture and feature space is the key lesson here.

<img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif" width="100%">

## 🔍 Key Findings

| # | Finding | Impact |
|---|---------|--------|
| 1 | **CatBoost is the clear winner** — R²=0.976, RMSE=2.714s on 50 features | Ordered boosting handles extreme skewness natively |
| 2 | **V4 Paradox** — Gradient boosting R² < −12 vs Elastic Net R² = 0.928 on 4 features | Algorithm × feature space is deeply interdependent |
| 3 | **Deep learning doesn't beat trees** on tabular IoT data | Confirms Grinsztajn et al. (2022) |
| 4 | **35 features is enough** — ΔR² = 0.005 for CatBoost V1→V2 | Edge deployment viable with compact model |
| 5 | **fwd_iat.tot** dominates (r = 0.9997) | Potential leakage — requires further investigation |

<img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif" width="100%">

## 💾 Using the Saved Models

```python
import joblib, catboost, lightgbm, tensorflow as tf, pandas as pd

# ── Best model ──────────────────────────────────────────────────────
best_model = catboost.CatBoostRegressor()
best_model.load_model("saved_models/catboost_v1.cbm")     # R² = 0.9761

# ── Edge-friendly model (35 features) ───────────────────────────────
edge_model = catboost.CatBoostRegressor()
edge_model.load_model("saved_models/catboost_v2.cbm")     # R² = 0.9715

# ── Ultra-lightweight model (4 features, 0.0s inference) ────────────
micro_model = joblib.load("saved_models/elasticnet_v4.pkl")  # R² = 0.9282

# ── Deep learning ───────────────────────────────────────────────────
lstm_model  = tf.keras.models.load_model("saved_models/lstm_v1.keras")
cnn_model   = tf.keras.models.load_model("saved_models/cnn1d_v1.keras")

# ── Supporting files ────────────────────────────────────────────────
feat_vars = joblib.load("saved_models/feature_variations.pkl")
encoders  = joblib.load("saved_models/encoders.pkl")
results   = pd.read_csv("saved_models/results.csv")
mi_scores = pd.read_csv("saved_models/mi_scores.csv")

# ── Inference example ────────────────────────────────────────────────
df = pd.read_csv("new_iot_flows.csv")
df["proto"]   = encoders["proto"].transform(df["proto"])
df["service"] = encoders["service"].transform(df["service"])

v1_feats = feat_vars["V1: All Features"]   # 50 features
v4_feats = feat_vars["V4: +Lasso Selected"] # 4 features

preds_best  = best_model.predict(df[v1_feats])
preds_micro = micro_model.predict(df[v4_feats])
```

<img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif" width="100%">

## 🗺️ Future Work

- [ ] **Edge Deployment** — Quantise CatBoost V2 (35 features) for Raspberry Pi real-time inference
- [ ] **Leakage Investigation** — Verify if `fwd_iat.tot` is mathematically derived from `flow_duration`
- [ ] **Anomaly Detection** — Use CatBoost prediction residuals as anomaly signals for IoT device compromise
- [ ] **Cross-Dataset Validation** — Test transferability on UNSW-NB15, NSL-KDD, Edge-IIoTset, IoTID20
- [ ] **SHAP Explainability** — Per-prediction explanations for Security Operations Centre analysts
- [ ] **Temporal Split** — Evaluate time-ordered train-test splitting for temporal IoT data
- [ ] **LightGBM Tuning** — Investigate instability with Optuna hyperparameter search

<img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif" width="100%">

## 📚 References

<details>
<summary><b>Harvard-style citations (click to expand)</b></summary>
<br/>

- Chen, T. and Guestrin, C. (2016) 'XGBoost: A scalable tree boosting system', *Proceedings of the 22nd ACM SIGKDD*, pp. 785–794.
- Grinsztajn, L., Oyallon, E. and Varoquaux, G. (2022) 'Why do tree-based models still outperform deep learning on typical tabular data?', *NeurIPS 35*, pp. 507–520.
- Guyon, I. and Elisseeff, A. (2003) 'An introduction to variable and feature selection', *JMLR*, 3, pp. 1157–1182.
- Hall, M.A. (1999) *Correlation-based feature selection for machine learning*. PhD thesis, University of Waikato.
- Hochreiter, S. and Schmidhuber, J. (1997) 'Long short-term memory', *Neural Computation*, 9(8), pp. 1735–1780.
- Ke, G. et al. (2017) 'LightGBM: A highly efficient gradient boosting decision tree', *NeurIPS 30*, pp. 3146–3154.
- Kraskov, A., Stögbauer, H. and Grassberger, P. (2004) 'Estimating mutual information', *Physical Review E*, 69(6), p. 066138.
- LeCun, Y. et al. (1998) 'Gradient-based learning applied to document recognition', *Proceedings of the IEEE*, 86(11), pp. 2278–2324.
- Prokhorenkova, L. et al. (2018) 'CatBoost: unbiased boosting with categorical features', *NeurIPS 31*, pp. 6638–6648.
- Shannon, C.E. (1948) 'A mathematical theory of communication', *Bell System Technical Journal*, 27(3), pp. 379–423.
- Sharmila, B.S. and Nagapadma, R. (2023) 'RT-IoT2022', UCI Machine Learning Repository. doi: 10.24432/C5P338.
- Tibshirani, R. (1996) 'Regression shrinkage and selection via the lasso', *JRSS-B*, 58(1), pp. 267–288.
- Zou, H. and Hastie, T. (2005) 'Regularization and variable selection via the elastic net', *JRSS-B*, 67(2), pp. 301–320.

</details>

<img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif" width="100%">

## 👤 Author

<div align="center">

**Jatin Kumar**
MSc Cybersecurity · Birmingham City University · Student ID: 25171403

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/YOUR_LINKEDIN)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/YOUR_USERNAME)
[![TryHackMe](https://img.shields.io/badge/TryHackMe-Top%202%25-212C42?style=for-the-badge&logo=tryhackme&logoColor=white)](https://tryhackme.com/p/YOUR_USERNAME)

<br/>

**Certifications:** CEH · CEH Masters · AZ-900 · ISO/IEC 27001:2022 Lead Auditor

</div>

<img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=6,12,20&height=100&section=footer" width="100%"/>
