Student Performance Prediction - End-to-End ML Pipeline
This repository implements a production-grade, modular, end-to-end Machine Learning pipeline from scratch. The project predicts student test scores based on demographic and socioeconomic features using Python, Flask, and industry-standard MLOps practices.

Features & Architecture
Modular Code Structure: Separate components for Data Ingestion, Data Transformation, and Model Training.

Custom Pipeline: Built-in preprocessing handles categorical encoding and numerical scaling flawlessly.

Flask Web Application: A clean user interface to input student details and get real-time predictions.

MLOps Best Practices: Robust logging, custom exception handling, and containerization support.

Project Directory Structure

├── .github/workflows/    # CI/CD pipelines
├── artifacts/            # Saved models, preprocessor objects, and data splits
├── notebook/             # Jupyter notebooks for EDA and Model Training
├── src/                  # Core source code modules
│   ├── components/       # Data Ingestion, Transformation, Model Trainer
│   ├── pipeline/         # Predict and Train pipelines
│   ├── exception.py      # Custom exception handling
│   └── logger.py         # Custom logging module
├── templates/            # HTML templates for the Flask UI
├── app.py                # Flask application entry point
├── requirements.txt      # Project dependencies
└── setup.py              # Script to package the project

🛠️ Tech Stack
Language: Python 3.8+

Framework: Flask

Libraries: Scikit-Learn, Pandas, NumPy, XGBoost, CatBoost

DevOps/Deployment: Docker, AWS Elastic Beanstalk (.ebextensions)

🏁 Getting Started
Follow these steps to set up and run the project on your local machine.
1. Clone the Repository
   git clone https://github.com/DeepakYadav9892/ml-student-performance-prediction.git
cd ml-student-performance-prediction

2. Create and Activate a Virtual Environment
   # On Windows
python -m venv venv
venv\Scripts\activate

# On macOS/Linux
python3 -m venv venv
source venv/bin/activate

3. Install Dependencies
   pip install -r requirements.txt

4. Run the Pipeline Components (Optional)
If you want to re-run the ingestion, transformation, and training pipeline from scratch:
python src/components/data_ingestion.py

5. Start the Flask App
   python app.py

Open your web browser and navigate to http://127.0.0.1:5000 to interact with the application.

🐳 Docker Setup
To containerize and run the application using Docker:

1.Build the Docker Image:
docker build -t student-performance-app .
2.Run the Docker Container:
docker run -p 5000:5000 student-performance-app

📊 Dataset & Features
The model utilizes the following features to make a prediction:

Gender: Male/Female

Race/Ethnicity: Group A, B, C, D, E

Parental Level of Education: High school, Associate's degree, Bachelor's degree, Master's degree, etc.

Lunch: Standard or free/reduced

Test Preparation Course: Completed or none

Reading Score & Writing Scor
