# Bus Delay Prediction System (Big Data Edition) 🚌⏱️

## 📌 Project Overview
This project implements a Big Data analytics pipeline to predict public transport delays. Unlike standard analysis tools, this system utilizes **Apache Spark (PySpark)** to handle data processing and Machine Learning tasks, making it scalable for large-scale transport datasets.

The system processes historical bus trip data, weather conditions, and scheduling information to predict delay minutes using a **Linear Regression** model.

## 🚀 Key Features
* **Big Data Architecture:** Built on **Apache Spark 3.5.7** for distributed data processing.
* **ETL Pipeline:** Handles data extraction, cleaning, and transformation using Spark SQL.
* **Advanced Preprocessing:**
    * **String Indexing:** Converts categorical data (Weather, Day of Week, Line) into numerical indices.
    * **Vector Assembly:** Combines features into a single feature vector for Spark ML.
* **Machine Learning:** Trains a **Linear Regression** model to quantify the relationship between schedule/weather factors and delay time.

## 🛠️ Tech Stack & Requirements
* **Language:** Python 3.9+
* **Core Engine:** Apache Spark (PySpark)
* **Dependencies:**
    * `pyspark`
    * `pandas` (for auxiliary visualization)
    * `findspark`
* **System Requirements:**
    * Java Development Kit (JDK 11)
    * Hadoop Winutils (for Windows execution)

## 📂 Project Structure
* `Transportation.ipynb` - The main PySpark notebook containing the ETL and ML pipeline.
* `final_project_dataset.csv` - The historical dataset used for training.
* `timetable_converted.csv` - Raw schedule data.

## ⚙️ How It Works (The Pipeline)
1.  **Environment Setup:** Configures `JAVA_HOME` and `HADOOP_HOME` to run Spark locally on Windows.
2.  **Data Ingestion:** Reads CSV data into a Spark DataFrame with schema inference.
3.  **Data Cleaning:** Removes duplicate entries and handles null values in the target variable.
4.  **Feature Engineering:**
    * Encodes `Day_of_Week`, `Weather`, and `Line` using `StringIndexer`.
    * Assembles `Hour_of_Day` and encoded features into a dense vector using `VectorAssembler`.
5.  **Model Training:** Fits a **Linear Regression** model to the processed feature vector.

## 📊 Model Selection
**Linear Regression** was selected as the predictive model.
* **Why:** It provides a clear interpretability of how each factor (e.g., Rain vs. Sun) linearly contributes to the delay time.
* **Performance:** The model minimizes the Root Mean Squared Error (RMSE) to estimate delays.

## 💻 How to Run
1.  Ensure Java (JDK 11) and Hadoop binaries are installed.
2.  Install Python dependencies:
    ```bash
    pip install pyspark findspark pandas
    ```
3.  Update the file paths in the notebook (`os.environ` paths) to match your local installation.
4.  Run `Transportation.ipynb` in Jupyter Notebook or JupyterLab.

## 👤 Author
**Prayush** - *BSc Data Science Assignment*