# Industrial Production Predictive Model File

This repository contains the **Industrial Production Predictive Model** trained to forecast industrial utility production trends. The model leverages the **AutoReg (Auto Regressive)** algorithm and is saved for real-time deployment.

## **Contents**
- `Industrial_Production_Predictive_Model.pkl`: The saved AutoReg model.
- `README.md`: Documentation for understanding and deploying the model.

---

## **How to Use This Model**

### 1. **Clone the Repository**
First, clone the repository to your local machine:
```bash
git clone https://github.com/YourGitHubUsername/Industrial-Production-Predictive-Model.git
cd Industrial-Production-Predictive-Model
```

### 2. **Install Dependencies**
Ensure you have Python installed. Install the required libraries:
```bash
pip install pandas numpy statsmodels
```

### 3. **Load the Model**
You can load the saved model using the following script:
```python
import pickle
from statsmodels.tsa.ar_model import AutoReg

# Load the model
with open('Industrial_Production_Predictive_Model.pkl', 'rb') as file:
    autoReg_model = pickle.load(file)

# Example usage
y_pred = autoReg_model.predict(start=len(autoReg_model.y), end=len(autoReg_model.y) + 10)
print("Predictions:", y_pred)
```

### 4. **Real-Time Deployment**
Integrate the model into your real-time data pipeline to predict future industrial production trends. Replace the input data (`y`) with your real-time data in the appropriate format (time-indexed).

---

## **Notes**
- The model requires data with a time-indexed format and matching pre-processing (e.g., frequency as monthly or daily). 
- Ensure to match the model's lag structure when providing input data.
- For additional customization or support, feel free to contact me at:
  - **Email**: olalekanabdulmumeen3@gmail.com

---

By following the steps above, you can efficiently utilize the **Industrial Production Predictive Model** for forecasting industrial utility trends.
