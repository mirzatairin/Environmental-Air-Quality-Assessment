# 🌍 Air Quality Analysis and Instantaneous Hourly AQI Calculation

This project performs a complete **end-to-end air quality data analysis pipeline** using real-world environmental data from the **OpenAQ platform**. It processes raw pollutant measurements, converts them into standardized units, computes pollutant-wise and overall Air Quality Index (AQI), and identifies the most polluted time periods.

---

## 📌 Project Objectives

- Load and preprocess air quality dataset
- Clean and restructure raw pollutant measurements
- Convert pollutant concentrations into consistent units (µg/m³)
- Calculate pollutant-wise Air Quality Index (AQI)
- Compute overall AQI using maximum pollutant contribution
- Identify dominant pollutants during pollution peaks
- Extract and visualize top 10 worst polluted hours

---

## 📊 Dataset Source

- OpenAQ Platform (global air quality monitoring network)
- Real-world air quality monitoring data
- Includes major pollutants such as:
  - PM2.5
  - PM10
  - CO
  - NO₂
  - O₃
  - SO₂

---

## ⚙️ Technologies Used

- Python 🐍
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Google Colab

---

## 🧠 Methodology

### 1. Data Cleaning
- Removed unnecessary location-based columns
- Converted datetime values into proper format
- Pivoted dataset from long to wide format for analysis

### 2. Unit Conversion
Pollutant concentrations were converted into **µg/m³** using standard scientific conversion formulas to ensure consistency across all measurements.

### 3. AQI Calculation
Air Quality Index (AQI) was computed using the **standard linear interpolation method** based on pollutant-specific concentration breakpoints.

- Defined pollutant-specific breakpoints
- Applied AQI scaling formula for each pollutant
- Computed AQI values individually for all pollutants

### 4. Overall AQI Computation
- Final AQI for each timestamp was calculated as the **maximum AQI value among all pollutants**, representing the dominant pollution impact.

### 5. Dominant Pollutant Detection
- Identified the pollutant contributing the highest AQI at each timestamp
- Used this to understand primary pollution sources over time

---

## 📈 Key Outputs

- Pollutant-wise AQI values (PM2.5, PM10, CO, NO₂, O₃, SO₂)
- Hourly overall AQI values
- Identification of dominant pollutants per timestamp
- Top 10 most polluted hours
- Visualization of AQI spikes over time

---

## 📉 Visualization

A bar chart was generated to visualize:

- The top 10 worst polluted hours
- Corresponding AQI values
- Dominant pollution events over time

---

## 📁 Project Structure
```
Environmental-Air-Quality-Assessment/
│
├── Environmental_Air_Quality_Assessment.ipynb
├── top_10_worst_polluted_hours.csv
├── README.md
```


---

## 🚀 How to Run

1. Open the notebook in **Google Colab**
2. Upload the dataset (`air-quality-data-set.csv`)
3. Run all cells sequentially
4. View AQI computations and visualizations

---

## 📌 Key Insights

- AQI spikes are strongly driven by **PM2.5 and PM10**
- Pollution levels vary significantly across different time periods
- Certain hours show extreme pollution events dominated by specific pollutants
- Particulate matter (PM pollutants) contributes most to poor air quality episodes

---

## 📊 Future Improvements

- Build a real-time AQI dashboard
- Integrate geospatial visualization (maps)
- Develop a predictive model for AQI forecasting
- Deploy as a web application using Streamlit or Flask

---

## 👨‍💻 Author

Rin — Data Science & AI Enthusiast  

This project demonstrates an end-to-end workflow for environmental air quality analysis using real-world datasets and custom AQI computation logic.

---

## 📜 License

This project is open-source and available for educational and research purposes.
