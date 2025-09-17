# Price Optimization & Demand Forecasting

This notebook suggests **optimal prices (MRP) per SKU** and forecasts 30-day demand.  
It uses conditional pricing method (approach 1) and regression models (arpproach 2) (to estimate demand elasticity) and a SARIMAX model (to capture seasonality and simulate demand under different prices).  

Outputs include:
- Recommended price per SKU based on conditional pricing method. (approach 1 result)
- Recommended price per SKU (from multiple models)
- Forecasted 30-day demand and expected profit
- Model validation metrics (R², MAE, RMSE, MAPE)
- One-line summary per SKU with sales KPIs and the best price

---

## Setup Instructions

1. **Clone this repository**
   ```bash
   git clone https://github.com/<your-repo>.git
   cd <your-repo>

Install dependencies
It’s best to use a virtual environment:
 - python -m venv venv
 - source venv/bin/activate    # on macOS/Linux
 - venv\Scripts\activate       # on Windows
 - pip install -r requirements.txt

requirement.txt:
pandas numpy scikit-learn statsmodels patsy matplotlib

- Place your sales CSV (e.g. Amazon Sale Report.csv) in a folder.
- Update the dataset path inside the config cell:
