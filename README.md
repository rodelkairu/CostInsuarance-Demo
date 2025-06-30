#  Medical Insurance Cost Prediction Using Machine Learning

This project is a machine learning-based application developed to **predict individual medical insurance charges** based on personal and health-related features. It aims to improve the fairness and accuracy of premium pricing for insurance companies like **Jubilee Insurance** by using a data-driven approach.

---

##  Overview

The system uses a dataset that includes features like:
- Age
- Sex
- BMI (Body Mass Index)
- Economic Status
- Smoking Status
- Region

Using this information, a machine learning model is trained to predict medical insurance charges. The system includes:
- Data preprocessing and encoding
- Model training using Linear Regression
- Prediction script for new data
- Evaluation metrics for testing accuracy
- A GUI for user interaction using `Tkinter`

---

##  Project Structure

Cost-Insurance/
├── insurance.csv # Dataset used for training
├── train_model.py # Trains and saves the prediction model
├── evaluate_model.py # Evaluates the model's accuracy and prints metrics
├── predict_insurance.py # Predicts charges based on user input
├── UI.py # GUI application using Tkinter
├── insurance_model.pkl # Serialized model, scaler, and encoders
└── README.md # This documentation file


---

##  How It Works

### 1. Data Preprocessing
- Categorical variables (`sex`, `smoker`, `region`) are encoded using `LabelEncoder`.
- Numerical variables (`age`, `bmi`) are scaled using `StandardScaler`.
- The number of children has been replaced with **economic status** as a more predictive feature.

### 2. Model Training (`train_model.py`)
- Uses `LinearRegression` from `sklearn` to train the model.
- Saves the trained model, scaler, and encoders to `insurance_model.pkl`.

### 3. Evaluation (`evaluate_model.py`)
- Evaluates the model using metrics:
  - R-squared (R²)
  - Mean Absolute Error (MAE)
  - Root Mean Squared Error (RMSE)

### 4. Prediction (`predict_insurance.py`)
- Loads the saved model and takes input features to make a prediction.

### 5. GUI Interface (`UI.py`)
- Built using `Tkinter`
- Allows users to input features and view predicted charges in a user-friendly interface.

---

## Dependencies

Install dependencies using a virtual environment:

```bash
python3 -m venv venv
source venv/bin/activate  # For Linux/macOS
venv\Scripts\activate     # For Windows

pip install -r requirements.txt

Or install manually:

pip install pandas numpy scikit-learn joblib tkinter


Sample Input & Output

Input:

    Age: 35

    Sex: female

    BMI: 28.4

    Economic Status: High

    Smoker: no

    Region: northeast


    Predicted Insurance Charges: $7275.91


    ## Testing Strategy

The system underwent:

    Preprocessing validation

    Cross-validation

    Performance testing using multiple regression metrics

    GUI testing with edge cases


   ## Contributors

    Samuel Kairu – Developer & Data Analyst

## Future Enhancements

    Integrate deep learning for complex relationships

    Add API for integration with insurance backend

    Extend dataset with real client records

## License

This project is for academic and non-commercial use only. Contact the author for permissions.


