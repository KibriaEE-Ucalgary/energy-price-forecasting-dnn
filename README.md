# energy-price-forecasting-dnn
#ENEL-682-L01-(Winter 2025)
## A Case Study on Crude Oil and Natural Gas

---

### 👨‍🔬 Team Members

- **G.K. Md. Muttakin** 
- **Monjurul Haque**  
- **Ahmed Mashook Iqbal**  

---

## 📌 Introduction (Problem Statement)

The prices of energy commodities like crude oil and natural gas are inherently volatile due to geopolitical, economic, and environmental factors. These fluctuations affect a broad range of stakeholders including industries, governments, and individual consumers.

This project presents a deep learning-based approach to forecast daily prices of crude oil and natural gas, providing a tool for stakeholders to make informed and timely decisions.

---

## 📊 Dataset Description

- **Source**: Historical commodity price data (e.g., WTI Crude Oil, Henry Hub Natural Gas)  
- **Time Range**: Daily records from **January 1997 to early 2023**  
- **Key Features**:
  - `Date`: Timestamp of each price record
  - `Settle`: Daily settlement price (used as target)
  - **Derived Features**: 
    - 14-day moving averages
    - Lagged values
    - Seasonal indicators (month, weekday, etc.)

---

## 🔁 Methodology

### 📈 Data Preprocessing Workflow

- Data Parsing  
- Column Filtering  
- Missing Value Removal  
- Normalization  
- Sequence Generation for Time Series  
- Train-Test Split  
- Seasonal Data Extraction (for Crude Oil & Natural Gas)

---

## 🧠 Deep Learning Models

### 1️⃣ LSTM Model
- LSTM Layer → Dense Output Layer
- Compiled with Mean Squared Error (MSE) Loss
- Metrics: RMSE, MAE, R²

### 2️⃣ CNN Model
- Conv1D → Dropout → Conv1D → Flatten → Dense Layers
- Compiled and trained on same data as LSTM

### 3️⃣ Hybrid CNN+LSTM Model
- Conv1D → Dropout → LSTM → Dropout → Dense Layers
- Combined strengths of CNN (feature extraction) and LSTM (temporal learning)

---

## 📉 Results & Metrics

| Model       | Crude Oil (RMSE, MAE, R²) | Natural Gas (RMSE, MAE, R²) |
|-------------|----------------------------|------------------------------|
| **LSTM**     | 5.37, 3.95, 0.9053         | 0.55, 0.36, 0.9094           |
| **CNN**      | 5.70, 4.45, 0.8935         | 0.58, 0.39, 0.9005           |
| **CNN+LSTM** | **4.80, 3.58, 0.9246**     | **0.53, 0.35, 0.9161**       |

> 📌 **Observation**: The hybrid CNN+LSTM model consistently outperformed standalone models in both accuracy and robustness for forecasting.

---

## ✅ Conclusion & Future Work

- The CNN+LSTM model provided the best forecasting performance for both oil and gas price prediction.
- Future improvements may include:
  - **Incorporating Attention Mechanisms or Transformer Architectures** for enhanced temporal modeling.
  - **Probabilistic Forecasting** to quantify prediction uncertainty.
  - **External Factor Integration**, such as geopolitical events, OPEC decisions, or macroeconomic indicators.

---

## 🛠 Tools & Technologies

- Python 3.x  
- TensorFlow / Keras  
- Pandas, NumPy  
- Matplotlib, Seaborn  
- Scikit-learn

---

## 📂 Project Structure

