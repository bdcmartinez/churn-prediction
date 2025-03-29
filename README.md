#  🧠 Churn Prediction Project

This project aims to build a machine learning model to predict the likelihood of a customer churning (i.e., stopping the use of a service or product). It follows a structured and reproducible approach, including organized data folders, Jupyter notebooks for exploration and modeling, and an environment setup for consistent development.

## 📁 Project Structure
    
    churn-prediction/
    │
    ├── README.md
    ├── requirements.txt
    ├── .env
    ├── .gitignore
    │
    ├── data/                         # Datos crudos y procesados
    │   ├── raw/                     # Datos originales extraídos
    │   ├── processed/               # Datos limpios y transformados
    │   └── external/                # Archivos externos o de terceros
    │
    ├── notebooks/                   # Jupyter notebooks exploratorios
    │   └── exploracion_inicial.ipynb
    │
    ├── dags/                        # DAGs de Airflow
    │   └── pipeline_prediccion.py   # DAG principal
    │
    ├── src/                         # Código fuente modular
    │   ├── data/                    # Extracción, limpieza, transformación
    │   │   ├── extract.py
    │   │   ├── clean.py
    │   │   └── transform.py
    │   │
    │   ├── features/                # Ingeniería de características
    │   │   └── build_features.py
    │   │
    │   ├── models/                  # Entrenamiento y evaluación de modelos
    │   │   ├── train_model.py
    │   │   ├── evaluate_model.py
    │   │   └── predict.py
    │   │
    │   ├── monitoring/              # Métricas, drift, alertas
    │   │   └── model_monitor.py
    │   │
    │   └── utils/                   # Funciones utilitarias comunes
    │       └── helpers.py
    │
    ├── api/                         # API para servir el modelo (FastAPI/Flask)
    │   ├── main.py
    │   ├── predict.py
    │   └── model_loader.py
    │
    ├── docker/                      # Configuración Docker
    │   ├── Dockerfile.api           # Para servir modelo
    │   ├── Dockerfile.airflow       # Para orquestación
    │   └── docker-compose.yml       # Orquestación de todos los servicios
    │
    ├── database/                    # Scripts SQL o conexión a DB
    │   └── setup_database.sql
    │
    ├── dashboards/                  # Reportes y visualizaciones
    │   ├── powerbi/
    │   └── streamlit_app/
    │
    ├── tests/                       # Tests automáticos
    │   └── test_train_model.py
    │
    └── config/                      # Parámetros del proyecto
        ├── config.yaml
        └── model_params.yaml


## 📊 Project Stages

    Data Cleaning: Handling missing values, encoding, normalization.

    Exploratory Data Analysis (EDA): Visualizing and understanding customer behavior patterns.

    Model Training: Testing different ML algorithms (e.g., Logistic Regression, Random Forest, XGBoost).

    Evaluation: Analyzing model performance with metrics like AUC, precision, recall.

## 🚀 Goals
- Identify customers with a high likelihood of churn.
- Provide actionable insights to reduce churn.
- Deploy the model for real-time or batch scoring (future scope).

## 🧪 Requirements

All required packages are listed in:
- requirements.txt (for pip users)
- environment/environment.yml (for conda users)

## 📌 Notes
- Data files are not included in the repo for privacy reasons.
- This project is for educational and demonstration purposes.

## 📬 Contact

For questions or feedback, feel free to open an issue or reach out at [bdcmartinez@outlook.com].


# ⚙️ Setup Instructions to dowload the project

- Clone the repository:

      git clone https://github.com/your-username/churn-prediction.git
  
- Navigate to the folder:

      cd churn-prediction
  
- Create a conda environment for being able to run the notebooks:

      conda env create -f environment.yml
  
- Activate the environment:
    
      conda activate churn-prediction
  
- Open Jupyter Notebook:

      Jupyter Notebooks



