# Bus Delay Prediction System 🚌⏱️

## Project Overview
This project implements a Machine Learning pipeline to predict public transport delays based on historical schedule data and environmental factors. Using the UK Bus Open Data Service (BODS) standard as a baseline, the system simulates a 90-day historical dataset to train a predictive model.

The goal is to provide accurate delay estimations to improve passenger journey planning.

## 🚀 Key Features
* **Data Ingestion:** Parses raw XML timetable data (TransXChange format).
* **Big Data Simulation:** Expands limited schedule data into a robust historical dataset (~4,000 records) with simulated "Rush Hour" and "Weather" variables.
* **Machine Learning:** Utilizes a **Random Forest Regressor** to predict delay duration.
* **Comparative Analysis:** Evaluates performance against KNN and Linear Regression models.
* **Visualization:** Generates insights on the primary causes of delays (e.g., Traffic vs. Weather).

## 🛠️ Technologies Used
* **Language:** Python 3.9+
* **Libraries:**
    * `Pandas` (Data Manipulation)
    * `Scikit-Learn` (Machine Learning)
    * `Matplotlib / Seaborn` (Data Visualization)
    * `xml.etree` (XML Parsing)

## 📂 Project Structure
* `Transportation.ipynb` - The main Jupyter Notebook containing the end-to-end pipeline.
* `final_project_dataset.csv` - The processed dataset used for training the model.
* `timetable_converted.csv` - The raw schedule extracted from the XML.
* `delay_visualizations.png` - Generated graphs showing model accuracy and feature importance.

## 📊 Results
The **Random Forest** model was selected as the final production model after outperforming other algorithms.

| Model | R² Score (Accuracy) |
| :--- | :--- |
| **Random Forest** | **0.80** |
| KNN | 0.65 |
| Linear Regression | 0.42 |

* **Key Insight:** The model identified **Hour of Day** (Rush Hour) as the most significant predictor of bus delays, followed by **Weather Conditions**.

## ⚙️ How to Run
1.  Clone this repository:
    ```bash
    git clone [https://github.com/Prayush77/Bus-Delay-Project.git](https://github.com/Prayush77/Bus-Delay-Project.git)
    ```
2.  Install required libraries:
    ```bash
    pip install pandas numpy scikit-learn matplotlib seaborn
    ```
3.  Open `Transportation.ipynb` in Jupyter Notebook to view the code and execution.

## 👤 Author
**Prayush** - *BSc Data Science Assignment*