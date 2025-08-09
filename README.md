# Machine Learning Project - Student Math Score Prediction

This project is a Flask-based Machine Learning web application that predicts a student's **Math Score** based on various input parameters provided by the user.

---

## 🚀 Features
- Takes user input via a web form
- Preprocesses data using a saved preprocessor object
- Uses the best trained ML model for prediction
- Displays predicted Math Score instantly

---

## 📥 Input Parameters

The app takes the following inputs from the user:

| Field | Description |
|-------|-------------|
| **gender** | Gender of the student |
| **race_ethnicity** | Race/Ethnicity group of the student |
| **parental_level_of_education** | Parent's highest education level |
| **lunch** | Type of lunch (Standard / Free/Reduced) |
| **test_preparation_course** | Whether test preparation course was completed |
| **reading_score** | Reading score of the student |
| **writing_score** | Writing score of the student |

> **Note**: In the backend, `reading_score` is fetched from the `writing_score` input, and vice versa.

---

## ⚙️ Project Workflow

1. **Train and Save Model**
   - Run the following file to train and test the model:
     ```bash
     python src/components/data_ingestion.py
     ```
   - This will:
     - Train and test multiple ML models
     - Select the **best performing model**
     - Save the model and preprocessor as `.pkl` files in the `artifacts/` folder

2. **Run the Flask App**
   - Start the Flask server:
     ```bash
     python app.py
     ```
   - Open browser at:
     ```
     http://127.0.0.1:5000
     ```
   - Navigate to:
     ```
     http://127.0.0.1:5000/predictdata
     ```
   - Fill out the form and click **Predict Your Math Score**

---

## 🛠 Setup Instructions

1. **Create Virtual Environment**
   ```bash
   python -m venv .venv
   ```

2. **Activate Virtual Environment**
   - **Windows (PowerShell)**:
     ```bash
     .venv\Scripts\Activate
     ```
   - **Mac/Linux**:
     ```bash
     source .venv/bin/activate
     ```

3. **Install Required Packages**
   ```bash
   pip install -r requirements.txt
   ```

4. **Deactivate Virtual Environment**
   ```bash
   deactivate
   ```

---

## 📊 Example Output
Once prediction is made, you’ll see:
```
Predicted Math Score: 78.56
```

---

## 📌 Notes
- Ensure `.pkl` files (model & preprocessor) are in the `artifacts/` folder before running the Flask app.
- Make sure all dependencies are installed before execution.

---

**Author:** MERAVATH PAVAN KUMAR
