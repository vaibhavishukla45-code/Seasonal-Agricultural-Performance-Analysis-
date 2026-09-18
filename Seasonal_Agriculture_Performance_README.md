# Seasonal Agriculture Performance Dataset (India)

A farm-level agricultural dataset covering **4,000 records** across 8 Indian states,
capturing crop production, weather conditions, soil properties, input usage, and
financial outcomes across three growing seasons. Designed for yield prediction,
profitability analysis, and resource optimisation research.

---

## File

| Property | Value |
|----------|-------|
| Filename | `seasonal_agriculture_performance_dataset(in).csv` |
| Rows | 4,000 |
| Columns | 28 |
| Missing Values | 120 (across 3 columns) |
| Geography | India — 8 states, multiple districts |
| Seasons | Kharif, Rabi, Zaid |

---

## Column Descriptions

### Identifiers & Location

| Column | Type | Description |
|--------|------|-------------|
| `Farm_ID` | String | Unique farm identifier (e.g. `SF10001`) |
| `State` | Categorical | Indian state where the farm is located |
| `District` | Categorical | District within the state |

### Crop & Season

| Column | Type | Values | Description |
|--------|------|--------|-------------|
| `Crop` | Categorical | Rice, Wheat, Maize, Cotton, Pulses, Groundnut, Chilli, Sugarcane | Crop type grown |
| `Season` | Categorical | Kharif, Rabi, Zaid | Agricultural growing season |

### Farm & Weather Conditions

| Column | Type | Range | Description |
|--------|------|-------|-------------|
| `Farm_Area_Hectares` | Float | 0.5 – 15.0 | Total farm area in hectares |
| `Rainfall_mm` | Float | 80.0 – 1395.2 | Total rainfall in millimetres *(48 missing)* |
| `Avg_Temperature_C` | Float | 16.2 – 39.7 | Average temperature in °C during the season |
| `Humidity_pct` | Float | 25.0 – 95.0 | Average relative humidity (%) |
| `Sunlight_Hours_Day` | Float | 3.5 – 11.0 | Average daily sunlight hours |

### Soil Properties

| Column | Type | Range | Description |
|--------|------|-------|-------------|
| `Soil_pH` | Float | 5.2 – 8.4 | Soil acidity/alkalinity (7 = neutral) |
| `Soil_Moisture_pct` | Float | 8.0 – 47.0 | Soil moisture content (%) *(40 missing)* |

### Nutrient Inputs (per hectare)

| Column | Type | Range | Description |
|--------|------|-------|-------------|
| `Nitrogen_kg_ha` | Float | 40 – 220 | Nitrogen applied (kg/hectare) |
| `Phosphorus_kg_ha` | Float | 15 – 120 | Phosphorus applied (kg/hectare) |
| `Potassium_kg_ha` | Float | 30 – 200 | Potassium applied (kg/hectare) |

### Farm Inputs & Practices

| Column | Type | Values / Range | Description |
|--------|------|----------------|-------------|
| `Irrigation_Method` | Categorical | Drip, Flood, Rainfed, Sprinkler | Water delivery method |
| `Fertilizer_kg_ha` | Float | 40 – 400 | Total fertilizer applied (kg/hectare) |
| `Pesticide_Litre_ha` | Float | 0.5 – 12.1 | Pesticide used (litres/hectare) |
| `Seed_Quality_Score` | Float | 0.65 – 1.00 | Seed quality index (higher = better) |

### Yield & Production

| Column | Type | Range | Description |
|--------|------|-------|-------------|
| `Yield_Tonnes_Ha` | Float | 0.3 – 101.4 | Crop yield in tonnes per hectare *(32 missing)* |
| `Production_Tonnes` | Float | 0.15 – 1424.4 | Total production in tonnes (`Yield × Farm_Area`) |

### Financial Outcomes

| Column | Type | Range (INR) | Description |
|--------|------|-------------|-------------|
| `Market_Price_INR_Tonne` | Integer | 2,594 – 131,240 | Market price per tonne (INR) |
| `Total_Cost_INR` | Integer | 26,826 – 1,349,990 | Total cost of cultivation (INR) |
| `Revenue_INR` | Integer | 6,107 – 5,080,900 | Gross revenue earned (INR) |
| `Profit_INR` | Integer | -1,019,223 – 4,345,421 | Net profit = Revenue − Cost (INR) |

### Water & Risk Metrics

| Column | Type | Range | Description |
|--------|------|-------|-------------|
| `Water_Used_m3` | Integer | 128 – 40,902 | Total water consumed (cubic metres) |
| `Water_Efficiency_t_per_1000m3` | Float | 0.14 – 79.8 | Production per 1,000 m³ of water used |
| `Disease_Pest_Risk_pct` | Float | 5.0 – 88.9 | Estimated disease/pest risk score (%) |

---

## Dataset Statistics

### Categorical Distributions

**States (8)**

| State | Records | % |
|-------|--------:|--:|
| Andhra Pradesh | 529 | 13.2% |
| Telangana | 516 | 12.9% |
| Maharashtra | 512 | 12.8% |
| Madhya Pradesh | 497 | 12.4% |
| Karnataka | 489 | 12.2% |
| Gujarat | 488 | 12.2% |
| Tamil Nadu | 485 | 12.1% |
| Punjab | 484 | 12.1% |

**Crops (8)**

| Crop | Records |
|------|--------:|
| Rice | 690 |
| Wheat | 614 |
| Maize | 551 |
| Cotton | 508 |
| Pulses | 496 |
| Groundnut | 424 |
| Chilli | 412 |
| Sugarcane | 305 |

**Seasons**

| Season | Records | Description |
|--------|--------:|-------------|
| Kharif | 1,779 | Monsoon season (Jun – Nov) |
| Rabi | 1,627 | Winter season (Nov – Apr) |
| Zaid | 594 | Summer/short season (Apr – Jun) |

**Irrigation Methods**

| Method | Records |
|--------|--------:|
| Flood | 1,310 |
| Rainfed | 1,041 |
| Drip | 915 |
| Sprinkler | 734 |

### Key Numeric Summary

| Feature | Min | Mean | Median | Max |
|---------|----:|-----:|-------:|----:|
| `Farm_Area_Hectares` | 0.5 | 7.9 | 7.9 | 15.0 |
| `Rainfall_mm` | 80.0 | 601.2 | 582.0 | 1,395.2 |
| `Avg_Temperature_C` | 16.2 | 26.8 | 26.9 | 39.7 |
| `Soil_pH` | 5.2 | 6.7 | 6.7 | 8.4 |
| `Yield_Tonnes_Ha` | 0.3 | 5.3 | 1.7 | 101.4 |
| `Revenue_INR` | 6,107 | 6,37,860 | 4,56,831 | 50,80,900 |
| `Profit_INR` | -10,19,223 | 1,11,557 | 3,673 | 43,45,421 |
| `Disease_Pest_Risk_pct` | 5.0 | 46.4 | 46.4 | 88.9 |

---

## Missing Values

| Column | Missing | % Missing | Recommended Treatment |
|--------|--------:|----------:|-----------------------|
| `Rainfall_mm` | 48 | 1.2% | Median imputation by Season/State |
| `Soil_Moisture_pct` | 40 | 1.0% | Median imputation by Season/Irrigation_Method |
| `Yield_Tonnes_Ha` | 32 | 0.8% | Drop rows (if target) or impute by Crop/Season |

---

## Suggested Use Cases

| Task | Target | Approach |
|------|--------|----------|
| **Yield prediction** | `Yield_Tonnes_Ha` | Regression (Random Forest, GBR, XGBoost) |
| **Profit prediction** | `Profit_INR` | Regression |
| **Profitability classification** | `Profit_INR > 0` | Binary classification |
| **Irrigation method impact** | `Yield_Tonnes_Ha`, `Water_Efficiency_t_per_1000m3` | ANOVA, group comparison |
| **Seasonal crop performance** | `Yield_Tonnes_Ha` by `Season` | EDA, descriptive statistics |
| **Disease/pest risk modelling** | `Disease_Pest_Risk_pct` | Regression, spatial analysis |
| **Water use optimisation** | `Water_Efficiency_t_per_1000m3` | Optimisation, clustering |
| **Market price analysis** | `Market_Price_INR_Tonne` | Time/season trend analysis |

---

## Notes

- **`Profit_INR`** can be negative — many farms operate at a loss, making it a
  realistic representation of agricultural economics in India.
- **`Yield_Tonnes_Ha`** has a large range (0.3 – 101.4); the high values likely
  correspond to Sugarcane, which yields significantly more per hectare than cereals.
  Consider analysing yields **per crop** separately.
- **`Seed_Quality_Score`** is a normalised index between 0.65 and 1.00 — no raw unit.
- Districts appear to be assigned across states in a semi-random manner; treat
  `District` as a nominal identifier rather than a strict geographic label.
- All financial values (`Market_Price_INR_Tonne`, `Total_Cost_INR`, `Revenue_INR`,
  `Profit_INR`) are in **Indian Rupees (INR)**.

---

## Quick Load (Python)

```python
import pandas as pd

df = pd.read_csv("seasonal_agriculture_performance_dataset(in).csv")

print(df.shape)   # (4000, 28)

# Encode categorical columns
df["gender_encoded"] = pd.Categorical(df["Season"]).codes
df = pd.get_dummies(df, columns=["Crop", "Season", "Irrigation_Method"])

# Handle missing values
df["Rainfall_mm"]      = df["Rainfall_mm"].fillna(df["Rainfall_mm"].median())
df["Soil_Moisture_pct"]= df["Soil_Moisture_pct"].fillna(df["Soil_Moisture_pct"].median())

# Drop rows where target is missing (for yield prediction)
df_model = df.dropna(subset=["Yield_Tonnes_Ha"])
print(df_model.shape)  # (3968, ...)
```

---

## Dataset Summary Card

| Property | Value |
|----------|-------|
| Records | 4,000 |
| Features | 28 |
| Target options | `Yield_Tonnes_Ha`, `Profit_INR`, `Revenue_INR` |
| Geography | 8 Indian states |
| Crops | 8 (Rice, Wheat, Maize, Cotton, Pulses, Groundnut, Chilli, Sugarcane) |
| Seasons | Kharif, Rabi, Zaid |
| Irrigation types | Drip, Flood, Rainfed, Sprinkler |
| Missing values | 120 rows affected (3 columns) |
| Financial currency | Indian Rupees (INR) |
