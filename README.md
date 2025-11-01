<h2> 📊 Customer Churn Prediction with ML.NET and ASP.NET Core 9 </h2>
<hr>
This project predicts whether a customer is likely to churn using machine learning in .NET. It includes:</br>

A model training console application using ML.NET<br>
An ASP.NET Core 8 Web API for serving predictions
<hr>
<h3>🚀 Project Structure</h3><br>
CustomerChurnPrediction-MLNet-ASPNET/ │ ├── ChurnPredictionTrainer/ # Console app for model training │ └── customer_data.csv # Sample training dataset │ └── churn_model.zip # Trained model (saved after training) │ ├── ChurnPredictionAPI/ # ASP.NET Core 8 Web API │ └── Controllers/ │ └── Models/ │ └── Services/ │ └── README.md
<hr>
<h3>🧠 ML Task</h3><br>
Type: Binary Classification<br>
Target: Predict if a customer will churn (true or false)<br>
Algorithm: SDCA Logistic Regression (ML.NET)
<hr>
<h3>📦 Dataset (CSV)</h3><br>
Example format:
<br>
<code>
CustomerId,Tenure,MonthlyCharges,TotalCharges,IsActive,Churned
1,12,29.85,345.12,true,false
2,1,56.95,56.95,false,true

Features Used:

Tenure

MonthlyCharges

TotalCharges

IsActive

Label (Target):

Churned (boolean)

🛠 How to Run
✅ Train the Model

Open ChurnPredictionTrainer in Visual Studio 2022

Build and run the project

The trained model (churn_model.zip) will be saved in the output directory

✅ Use in Web API

Open ChurnPredictionAPI in Visual Studio 2022

Ensure churn_model.zip is placed in the root or loaded from the correct path

Run the API

Use tools like Postman or Swagger to test the /api/churn endpoint

🔍 API Endpoint

POST /api/churn

Request (JSON):
{
  "Tenure": 6,
  "MonthlyCharges": 70.5,
  "TotalCharges": 420.0,
  "IsActive": false
}

Response:
{
  "Churned": true,
  "Probability": 0.89,
  "Score": 2.15
}

🛠 Tech Stack

.NET 8

ML.NET

ASP.NET Core 9 Web API

Visual Studio 2022


</code>
