# 🏠 NYC Airbnb Room Type Predictor

An end-to-end Machine Learning web application that predicts the **room type of an Airbnb listing in New York City** based on listing-related features.

The project covers the complete Machine Learning workflow — from data preprocessing and experimentation with multiple classification models in Jupyter Notebook to deploying the final trained model through a **FastAPI backend** with an interactive **HTML/CSS/JavaScript frontend**.

---

## 🚀 Features

- 🏠 Predicts Airbnb room type based on listing features
- 🤖 Compares multiple classification algorithms
- 🌲 Uses **Random Forest Classifier** as the final selected model
- ⚙️ Uses Scikit-learn `ColumnTransformer` for preprocessing
- 🔗 Uses Scikit-learn `Pipeline` for preprocessing + model inference
- 💾 Saves the trained ML pipeline as a `.pkl` file
- 🚀 Provides a REST API using **FastAPI**
- ✅ Uses **Pydantic** for input validation
- 🌐 Interactive frontend using **HTML, CSS and JavaScript**
- 📊 Model experimentation performed in Jupyter Notebook

---

## 🏗️ Project Architecture

```text
                    ┌─────────────────────┐
                    │      User Input     │
                    │   HTML/CSS/JS UI    │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │      FastAPI        │
                    │      Backend        │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │      Pydantic       │
                    │   Input Validation  │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │   Saved ML Pipeline │
                    │      (.pkl)         │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │  ColumnTransformer  │
                    │   Preprocessing     │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │  Random Forest      │
                    │     Classifier      │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │ Predicted Room Type │
                    └─────────────────────┘