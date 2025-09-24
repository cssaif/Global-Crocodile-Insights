# 🐊 Global Crocodile Species Dataset – EDA

## 📌 Project Overview
This project explores the **Global Crocodile Species Dataset** through a structured **Exploratory Data Analysis (EDA)** pipeline.  
The goal is to uncover insights about crocodile sizes, weights, habitats, geographic distribution, and conservation status.  

We focus on:
- Handling **missing values** and **outliers**  
- Renaming and cleaning columns for readability  
- Aggregating and visualizing trends  
- Applying transformations (e.g., weight differences per species)  
- Querying subsets (e.g., adult females, giant crocodiles)  
- Performing **datetime-based analysis** (observations over time)

---

## 📂 Dataset
The dataset comes from [Kaggle](https://www.kaggle.com/datasets/zadafiyabhrami/global-crocodile-species-dataset) and includes crocodile observation records.  

### Main Columns
- `observation_ID` – Unique observation ID  
- `scientific_name` – Scientific species name  
- `common_name` – Common species name  
- `length_m` – Observed length (meters)  
- `weight_kg` – Observed weight (kilograms)  
- `age_class` – Age category (Hatchling, Juvenile, Subadult, Adult)  
- `sex` – Male / Female  
- `observation_date` – Date of observation  
- `country` – Country or region  
- `location` – Specific location  
- `habitat_type` – Habitat (River, Swamp, etc.)  
- `conservation_status` – IUCN conservation category  
- `observer_name` – Name of the observer (if available)  
- `notes` – Additional notes  

---

## 🛠️ Steps Performed
1. **Data Cleaning**
   - Renamed columns to `snake_case`
   - Checked for duplicates and missing values
   - Converted dates to `datetime`

2. **Outlier Handling**
   - Detected extreme values in `length_m` and `weight_kg` using IQR  
   - Highlighted "giant crocodiles" (`length_m > 5m`)

3. **Exploratory Analysis**
   - Box plots for length/weight distributions  
   - Scatter plots for length vs weight per species  
   - Violin plots for habitat comparisons (rivers vs swamps)  
   - Aggregations: species-level averages, primary habitat mode  
   - Yearly trend analysis of observations  

4. **Transformations**
   - Added `Weight_diff`: difference from species average weight  
   - Extracted `year` from `observation_date`

5. **Queries**
   - Subsets like **adult females**, **species-habitat mapping**, **giant crocodiles**

---

## 📊 Example Visualizations
- **Boxplot**: Length distribution with outliers  
- **Scatter**: Length vs Weight (species averages)  
- **Violin**: Habitat-based distributions  
- **Line chart**: Observation counts per year  

---

## 🚀 Next Steps
- Build predictive models for length/weight based on habitat and region  
- Study conservation status trends across species  
- Explore geographic visualizations (maps)  

---

## 🧑‍💻 Tech Stack
- **Python**: pandas, numpy, plotly  
- **EDA Methods**: masking, splicing, aggregation, transform, apply, query, datetime  
