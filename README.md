# Insurance Risk Analytics 🚦

A comprehensive analytics platform for assessing and managing insurance risk using data-driven methodologies, statistical modeling, and machine learning.

## 📚 Table of Contents

- [📖 Overview](#overview)
- [✨ Features](#features)
- [🏗️ Architecture](#architecture)
- [⚙️ Installation](#installation)
- [🚀 Quick Start](#quick-start)
- [🛠️ Usage](#usage)
- [📂 Project Structure](#project-structure)
- [📝 Configuration](#configuration)

## 📖 Overview

**Insurance Risk Analytics** is an end-to-end platform designed to help insurance companies, actuaries, and data scientists evaluate risk, predict claims, and optimize underwriting processes. The platform supports the full analytics lifecycle, from data ingestion and preprocessing to advanced modeling and dashboard reporting.

**Key objectives:**
- 🤖 Automate risk assessment using statistical and machine learning models.
- 📊 Enable exploratory data analysis (EDA) and visualization.
- 🧩 Provide modular, extensible components for custom analytics workflows.

## ✨ Features

- 📥 **Data Ingestion & Preprocessing:** Import data from CSV, Excel, or databases. Includes cleaning, missing value handling, and feature engineering.
- 📈 **Exploratory Data Analysis:** Generate summary statistics, correlation matrices, and interactive visualizations.
- 🧮 **Risk Scoring & Segmentation:** Segment policyholders by risk profiles using clustering and scoring algorithms.
- 🔮 **Predictive Modeling:** Build and evaluate models for claim frequency, severity, and fraud detection using scikit-learn, XGBoost, or custom algorithms.
- 📏 **Model Evaluation:** Automated metrics reporting (AUC, RMSE, confusion matrix, etc.) and cross-validation.
- 📊 **Reporting & Dashboards:** Export results as HTML/PDF reports and interactive dashboards (Plotly, Dash, or Streamlit).
- 🛠️ **Extensible Pipeline:** Modular codebase for easy integration of new models, data sources, or analytics steps.

## 🏗️ Architecture

The platform is organized into modular components:

- 🗃️ **Data Layer:** Handles data loading, validation, and transformation.
- 🧠 **Analytics Engine:** Houses EDA, modeling, and evaluation logic.
- 📊 **Reporting Layer:** Generates visualizations and dashboards.
- ⚙️ **Configuration:** Centralized YAML/JSON config for reproducibility.

## ⚙️ Installation

### Prerequisites

- 🐍 Python 3.8+
- 📦 pip (Python package manager)
- 📓 (Optional) Jupyter Notebook for interactive analysis

### Steps

1. **Clone the repository:**
    ```bash
    git clone https://github.com/estif-lul/insurance_risk_analytics.git
    cd insurance_risk_analytics
    ```
2. **Create a virtual environment (recommended):**
    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows: venv\Scripts\activate
    ```
3. **Install dependencies:**
    ```bash
    pip install -r requirements.txt
    ```

## 🚀 Quick Start

1. **Prepare your dataset:** Place your input files (CSV, Excel, etc.) in the `data/` directory.
2. **Configure the pipeline:** Edit `config.yaml` to specify data paths, model parameters, and output options.
3. **Run the main script:**
    ```bash
    python main.py --config config.yaml
    ```
4. **View results:** Outputs (reports, models, logs) are saved in the `output/` directory. If dashboarding is enabled, follow the terminal link to access the web interface.

## 🛠️ Usage

### 🗂️ Data Preparation

- Ensure your dataset includes relevant fields (e.g., policy ID, claim amount, risk factors).
- Supported formats: CSV, XLSX, or database connections (see `config.yaml` for details).

### ⚡ Running Analysis

- **Basic run:** Executes the full pipeline (EDA, modeling, reporting).
- **Custom modules:** You can run specific modules (e.g., only EDA or modeling) by adjusting the config.

### 💻 Example Command

```bash
python main.py --config config.yaml --step modeling
```

### 📤 Output

- 📄 **Reports:** HTML/PDF summaries in `output/reports/`
- 🧩 **Models:** Serialized models in `output/models/`
- 📝 **Logs:** Execution logs in `output/logs/`

## 📂 Project Structure

```
insurance_risk_analytics/
├── data/             # Input datasets
├── src/              # Source code 
│   ├── notebooks/    # Jupyter notebooks for EDA and prototyping
│   ├── scripts/
│   ├── tests/       
├── output/           # Generated reports, models, and logs
│   ├── reports/
│   ├── models/
│   └── logs/
├── config.yaml       # Main configuration file
├── requirements.txt  # Python dependencies
├── main.py           # Entry point for running the pipeline
└── README.md         # Project documentation
```

## 📝 Configuration

All pipeline settings are managed via `config.yaml`, including:

- 📁 **Data paths:** Input/output directories, file formats
- 🧮 **Model parameters:** Algorithm selection, hyperparameters
- 🧹 **Preprocessing:** Feature selection, scaling, encoding
- 📊 **Reporting:** Output formats, dashboard options

**Example snippet:**
```yaml
data:
  input_path: data/claims.csv
  target_column: claim_amount
```