# 📈 Demand Forecasting & Inventory Optimization (Python)

[![Python](https://img.shields.io/badge/python-v3.8+-blue.svg)](https://www.python.org/downloads/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Statsmodels](https://img.shields.io/badge/statsmodels-0.14+-orange.svg)](https://www.statsmodels.org/)
[![Jupyter](https://img.shields.io/badge/jupyter-notebook-orange.svg)](https://jupyter.org/)

> End-to-end project that forecasts demand using time-series models (SARIMAX) and computes inventory decisions (safety stock, reorder point, EOQ) backed by forecast uncertainty. Built for reproducible analysis in Jupyter.
> 
<img width="1364" height="551" alt="Screenshot 2025-12-11 134930" src="https://github.com/user-attachments/assets/edcbbc0f-ae58-47a2-9bd2-c100f9b60d59" />
<img width="1344" height="539" alt="Screenshot 2025-12-11 134946" src="https://github.com/user-attachments/assets/2baecaf6-d2b2-4183-81b8-f1852f1fb7fc" />
<img width="1332" height="421" alt="Screenshot 2025-12-11 135000" src="https://github.com/user-attachments/assets/ba6d69a1-9c12-48cd-b9b7-b701f8e1f3f9" />
---

## ✨ Features

- **Time series EDA**: decomposition, trend/seasonality checks, ACF/PACF.
- **SARIMAX forecasting** with prediction intervals.
- **Model evaluation**: MAE, RMSE, MAPE and rolling time-series cross-validation.
- **Inventory optimization**:
  - Safety stock (probabilistic, using z-score)
  - Reorder point (ROP)
  - Simple EOQ example
  - Inventory simulation under forecasted demand and lead time
- **Per-product pipeline**: run forecasting + inventory logic for each `Product_ID`.
- **Reproducibility**: model saving (joblib), cleaned CSV outputs, requirements file.

---

## 🚀 Quick Start

```bash
# Clone
git clone https://github.com/YOUR_USERNAME/demand-forecasting-inventory-optimization.git
cd demand-forecasting-inventory-optimization

# (Optional) create venv
python -m venv venv
# mac/linux
source venv/bin/activate
# windows
# venv\Scripts\activate

# Install deps
pip install -r requirements.txt

# Run the script for product-level forecasts
python src/demand_forecast.py --data data/demand_inventory.csv --product P1 --forecast-steps 14

# Or open and run the interactive notebook
jupyter notebook notebooks/demand_forecasting.ipynb

```

## 📸 Usage

1. Run the script or the notebook to:
   - Clean & parse dates
   - Visualize series & ACF/PACF
   - Fit SARIMAX and generate forecasts + prediction intervals
   - Compute safety stock, reorder point, EOQ (requires cost params), and simulate inventory
2. Inspect outputs in outputs/ and tune model/hyperparams.

## 🛠️ Tech Stack

- **Python (3.8+)**  
- **Pandas, NumPy** for data handling 
- **Statsmodels** for SARIMAX
- **Matplotlib, Plotly** for visualization
- **Scikit-learn** for evaluation utilities
- **Joblib** for saving models
- Jupyter Notebook for interactive analysis


## 🎨 Future Enhancements

-Auto model selection using pmdarima.auto_arima
- Intermittent demand models (Croston) for sparse demand 
- REST API to serve forecasts
- Dashboard (Streamlit/Plotly Dash) for interactive management 
- More realistic inventory flow (multiple outstanding orders, variable lead times)
- 
## 🤝 Contributing

1. Fork the repo  
2. Create a feature branch  
3. Commit & push 
4. Open a PR

💡 Contributions, issues, and feature requests are welcome!


---


