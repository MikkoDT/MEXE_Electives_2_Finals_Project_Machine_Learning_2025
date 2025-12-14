
---

## 1. Pair Information
- **Pair Name:** Fire Nation
- **Members:** Francisco, Baylon
- **Topic:** Flood Prediction (NCR, Philippines)
- **Chosen Model:** Logistic Regression :contentReference[oaicite:2]{index=2}

---

## 2. Dataset Overview
- **Dataset Source:** Flood_Prediction_NCR_Philippines.csv (converted to cleaned dataset) :contentReference[oaicite:3]{index=3}  
- **Description:** The dataset contains environmental measurements used to determine whether flooding occurs under specific conditions. Each record represents a set of values associated with rainfall intensity, river/water level, and elevation.  
- **Target Variable:** `FloodOccurrence`  
  - `0` = No Flood  
  - `1` = Flood  
- **Features Used (Predictors):**
  | Feature | Meaning | Unit |
  |---|---|---|
  | `Rainfall_mm` | Rainfall intensity | mm |
  | `WaterLevel_m` | Observed water level | m |
  | `Elevation_m` | Elevation of location | m |

---

## 3. Preprocessing Summary
The notebook applies preprocessing steps recommended for classification and for logistic regression stability. :contentReference[oaicite:4]{index=4}  
- **Encoding:** Not required (all selected predictors are numeric). :contentReference[oaicite:5]{index=5}  
- **Scaling:** `StandardScaler` is applied to normalize feature magnitudes before model fitting. :contentReference[oaicite:6]{index=6}  
- **Cleaning steps:**
  - Selected only the required columns: `Rainfall_mm`, `WaterLevel_m`, `Elevation_m`, and `FloodOccurrence`.
  - Checked for missing/invalid values and ensured numeric formatting for model readiness.
- **Train–test split:** 80% training / 20% testing with stratification to preserve the class distribution between flood and non-flood cases. :contentReference[oaicite:7]{index=7}

### Class Imbalance Handling (Key Step)
Flood occurrence is typically rare compared to non-flood cases. To address this imbalance, the model uses:
- `class_weight="balanced"` to increase sensitivity to the minority (flood) class during training.

---

## 4. Model & Results
- **Model used:** Logistic Regression (binary classification). :contentReference[oaicite:8]{index=8}  
- **Rationale:** Logistic Regression is suitable because the objective is to predict a **binary outcome** (Flood vs No Flood) and provide an interpretable probability-based decision boundary. :contentReference[oaicite:9]{index=9}  
- **Metrics reported:**
  - **Recall**
  - **F1-score**
  - **Confusion Matrix** :contentReference[oaicite:10]{index=10}  
- **Visualizations:**
  - Confusion matrix plot (included in the notebook).

### Insights (3–5)
1. Since flood cases are underrepresented, the model prioritizes **Recall** to reduce missed flood events (false negatives), which are more critical in warning scenarios. :contentReference[oaicite:11]{index=11}  
2. Feature scaling improves model stability because the predictors have different numeric ranges (e.g., rainfall values vs elevation values). :contentReference[oaicite:12]{index=12}  
3. Higher rainfall and higher water level tend to increase the predicted flood probability, while higher elevation may reduce flood likelihood due to natural drainage advantage.  
4. The confusion matrix enables clear identification of false alarms versus missed floods, supporting proper interpretation beyond accuracy alone. :contentReference[oaicite:13]{index=13}  
5. Model performance can be further improved by exploring threshold tuning and additional predictors (e.g., soil moisture, historical lag features) if allowed by the study scope.

---

## 5. How to Run
These steps replicate the required execution process for the notebook. :contentReference[oaicite:14]{index=14}  

### Option A — VS Code / Jupyter / PyCharm (Local)
1. Install **Python 3.x** and ensure `pip` is available.
2. Install dependencies:
   ```bash
   pip install -r requirements.txt

