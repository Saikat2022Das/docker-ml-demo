## Reproducing the ML Model

Since .gitignore keeps our repo clean by excluding large model files and the venv, follow this flow to rebuild the project locally:

Phase 1: Environment Initialization
Create Environment: python3 -m venv venv

Activate Environment: source venv/bin/activate (Linux/Mac) or .\venv\Scripts\activate (Windows)

Install Dependencies: pip install -r flask_app/requirements.txt

Phase 2: The Execution Pipeline
Follow these steps in order to generate the model artifacts:

Step 1: Data Ingestion python src/data/data_ingestion.py

(Downloads or loads the raw data into the project)

Step 2: Data Preprocessing python src/data/data_preprocessing.py

(Cleans and handles missing values)

Step 3: Feature Engineering python src/features/feature_engineering.py

(Transforms variables for the model)

Step 4: Model Building python src/model/model_building.py

Result: This creates the model file (e.g., .pkl or .h5).

Phase 3: Tracking & Evaluation (Optional)
If you want to track experiments using MLflow:

Install MLflow: pip install mlflow

Run Evaluation: python src/model/model_evaluation.py

Quick Tip: It’s a good idea to add mlflow to your requirements.txt so users don't have to install it manually in the final step!
