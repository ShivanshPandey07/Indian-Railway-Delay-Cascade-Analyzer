# 🚂 Indian Railway Delay Cascade Analyzer

## 📌 Project Overview
A data analytics project that models how a single train delay at one station 
cascades through India's entire railway network of 8,990 stations and 5,208 trains. 
Built using real Indian Railways data combining network graph analysis, 
cascade propagation simulation and ML-based delay prediction.

## 🔴 Live Dashboard
🔗 [View Interactive Tableau Dashboard](https://public.tableau.com/app/profile/shivansh.pandey1813/viz/IndianRailwayDelayCascadeAnalyzer/Dashboard1)

## 🔍 Key Findings
- A 60-min delay at **Howrah Junction** cascades to **2,914 stations**
- Generates **69,181 minutes** of total network delay from just ONE station
- **Howrah JN** is the #1 bottleneck with 44 network connections
- Only **17% of trains** arrive on time (≤5 min delay)
- Worst year for delays: **2023** with 64.2 min average delay
- XGBoost model predicts cascaded delay with **98.9% R² accuracy**

## 🛠️ Tech Stack
| Tool | Purpose |
|------|---------|
| Python | Data processing & ML |
| Pandas / NumPy | Data cleaning & EDA |
| NetworkX | Railway network graph |
| XGBoost | Cascade delay prediction |
| Matplotlib / Seaborn | Visualizations |
| Tableau Public | Interactive dashboard |
| Google Colab | Development environment |

## 📊 Dashboard Preview
The dashboard includes:
- 🗺️ **Station Connectivity Map** — 8,690 stations plotted across India
- 📊 **Top 15 Bottleneck Stations** — ranked by network connections
- 💥 **Cascade Impact Chart** — total delay generated per origin station
- 📈 **Delay Trend 2016–2025** — yearly average delay analysis
- 🤖 **ML Delay Decay** — XGBoost predicted delay across hops

## 📁 Project Structure
railway-delay-analyzer/
├── 01_data_collection.ipynb    # Data loading, cleaning, EDA,
│                               # network graph, cascade simulation
│                               # & XGBoost ML model
├── data/
│   ├── indian_railway_delay_data_.csv
│   ├── schedules.json          # 417,080 stop records
│   ├── stations.json           # 8,990 stations
│   ├── trains.json             # 5,208 trains
│   └── tableau_exports/
│       ├── 01_delay_analysis.csv
│       ├── 02_bottleneck_stations.csv
│       ├── 03_cascade_howrah.csv
│       ├── 04_cascade_comparison.csv
│       ├── 05_ml_predictions.csv
│       └── 06_stations_map.csv
└── README.md

## 📈 Model Results
| Metric | Value |
|--------|-------|
| Stations in network | 8,990 |
| Trains analyzed | 5,208 |
| Route connections | 29,263 |
| Total stop records | 417,080 |
| ML Model R² Score | **98.9%** |
| MAE | **0.47 minutes** |
| Max cascade (Howrah JN) | **2,914 stations affected** |
| Total delay generated | **69,181 minutes** |

## 🚀 How to Run
1. Clone the repo
```bash
git clone https://github.com/ShivanshPandey07/indian-railway-delay-cascade-analyzer
cd indian-railway-delay-cascade-analyzer
```
2. Install dependencies
```bash
pip install pandas numpy matplotlib seaborn plotly networkx xgboost scikit-learn
```
3. Open `01_data_collection.ipynb` in Google Colab or Jupyter Notebook
4. Upload the data files from the `data/` folder
5. Run all cells sequentially

## 👤 Author
**Shivansh Pandey** 
