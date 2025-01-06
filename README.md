# Soil Moisture Prediction Model

Welcome to the **Soil Moisture Prediction** project by **Team Defiance**. This project leverages a hybrid machine learning approach to predict soil moisture levels accurately using time series data.

## Deployment

- **Detailed Report**: [View Report](https://docs.google.com/document/d/1lO0DX5hBEHyaye1iGuFdh5X1E15zbmJ4PUPtuV-gsr4/edit?tab=t.0)
- **Replit Deployment**: [Access Here](https://soil-moisture-pred-nith-2.sarthaksharma27.repl.co/)

---

## Methodology

### Data Preprocessing
1. **Parameter Selection for SARIMAX**:
   - Melted soil moisture levels using the `pm3` variable and its values.
   - Calculated the first, second, and third differences of the moisture levels for comparative analysis.

2. **Seasonal Decomposition**:
   - Decomposed the time series into three components using LOESS decomposition (`STL` class from `statsmodels`) over an 8-month subset.

3. **Stationarity Check**:
   - Verified stationarity using the Augmented Dickey-Fuller (ADF) test.
   - Plotted autocorrelation and partial autocorrelation values to determine optimal parameters.

### Model Development
1. **SARIMAX Model**:
   - Utilized SARIMAX for capturing seasonality and trend patterns in the data.

2. **Random Forest Regression (RFR) Pipeline**:
   - Built an imputed RFR pipeline for predicting soil moisture levels.
   - Exported and sliced the model using `pickle slicer` into four smaller divisions, each with unique weights and sizes.

### Optimization
- Fine-tuned `P`, `Q`, `D`, and `M` parameters to maximize accuracy.
- Evaluated model performance using ADFuller and other statistical tests.

---

## Future Work
- Enable users to customize model parameters for prediction.
- Provide a more interactive and user-friendly interface for real-time soil moisture predictions.

---

## Technologies Used
- **Languages**: Python
- **Libraries**: `statsmodels`, `pickle`, `scikit-learn`
- **Deployment**: Replit

---

For any inquiries or contributions, feel free to contact **Team Defiance**.
