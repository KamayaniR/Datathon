# OrbitShield: AI-Driven Space Debris Management  
*Women in Data Datathon 2025 – Team Datanova*  

## Project Overview  
OrbitShield is a predictive analytics platform developed during the **Women in Data 2025 Datathon** to enhance **Space Situational Awareness (SSA)**. The project addresses the growing challenge of **orbital debris in Low Earth Orbit (LEO)** by combining geospatial clustering, machine learning forecasting, and explainable alerts to proactively identify and mitigate collision risks.

---

## Problem Statement  
- Increasing debris density in LEO poses severe threats to satellites, missions, and space sustainability.
- Existing mitigation strategies are **reactive**, experimental, and lack scalability.  
- No integrated predictive system exists today that prioritises risks and translates them into **actionable intelligence**. 

---

## Proposed Solution – OrbitShield  
**OrbitShield** is an **AI-driven orbital safety system** designed to:  
- Automate **orbital dataset ingestion and fusion** (~845K records, 228 unique objects)  
- Apply **geospatial clustering (DBSCAN)** to detect debris-dense zones
- Forecast collision probabilities with **Random Forest, XGBoost, and LSTM** models
- Generate **human-readable alerts** (via LLMs) for satellite operators  
- Deliver insights via an **interactive Streamlit/Dash dashboard** with real-time trajectories, risks, and alerts
---

## Methodology & Approach  

### 1. Data Extraction & Fusion  
- Collected datasets: Ephemeris, State Vectors, ELSETS, Object Metadata
- Standardized schema → `object_id, epoch, x, y, z, vx, vy, vz`  
- Consolidated into a single dataset for clustering & forecasting.  

### 2. Geospatial Analysis  
- Converted orbital positions into **3D ECI coordinates**.  
- **DBSCAN clustering** identified 7 debris clusters.  
- Classified satellites into **High (45), Medium (55), Low (4955)** risk levels

### 3. Machine Learning Modeling  
- Engineered features: altitude bands, velocity, cluster density.  
- Models trained: **Random Forest, XGBoost, LSTM**.  
- Outputs: collision probabilities + trajectory forecasts

### 4. Forecasting & Alerts  
- Generated predictive warnings such as:  
  *“Satellite Alpha is projected to pass within 3 km of debris cluster Zeta in 72 hours. Risk Score = 0.84.”* 
- Alerts explainable and prioritized by **velocity, mass, mission criticality**.  

### 5. Visualization Dashboard  
- Interactive dashboard with:  
  - 3D orbital cluster maps  
  - Risk monitoring panel  
  - Collision warnings and countdowns  
  - Predictive path projections 

---

## Results & Key Insights  
- **7 orbital clusters** identified, with clear danger vs safe zones.  
- **Collision probability forecasts** aligned with observed risk trends.  
- Dashboard provided a **transparent, scalable** way to monitor orbital safety.  
- **OrbitShield uniqueness:** first to combine **clustering + ML forecasting + explainable alerts** into one solution,

---

## Tech Stack  
- **ETL & Workflow:** Python (Pandas, NumPy), Apache Airflow, PostgreSQL + PostGIS
- **Modeling:** Scikit-learn (RF/XGBoost), TensorFlow/Keras (LSTM)
- **Clustering & Geospatial:** DBSCAN, PostGIS, Plotly
- **Visualization:** PowerBi
- **Alerts:** Rule-based LLMs 

---

## Team Datanova (Women in Data 2025)  
- **Kamayani Rai** – Applied Analytics & ML  
- **Kundana Rasi Tadikonda** – Analytics Engineering & Visualization  
- **Julia Davis** – Industrial Engineering & Visualization  
- **Kimberley Gillette** – Data Science & ML

---

## Deliverables  
- Consolidated Dataset (`consolidated_orbital_data.csv`)  
- Geospatial Analysis Notebook (`GeoSpatial_Analysis.ipynb`)
- ML Predictions (`XGBoostPredictions.csv`, `LSTMPredictions.csv`)
- Dashboard Prototype (Streamlit/Dash)
- Final Presentation & Documentation

---

## Future Scope  
- Real-time integration with live orbital feeds.  
- Reinforcement learning for maneuver recommendations.  
- Public dashboard layer for policy, education, and sustainability  

---

