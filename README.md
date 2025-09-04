# Dataset Values

## Setup


### 1. Create and activate virtual environment

   - python3 -m venv venv

   - source venv/bin/activate   # On macOS/Linux
   - venv\Scripts\activate      # On Windows

### 2. Install dependencies

   - pip install -r requirements.txt
   

### 3. Run the forecasting pipeline

   - python main.py
   

### 4. Outputs

-  Forecast plots are saved in the plots/ folder
-  Trained models and accuracy metrics are saved in the pkl/ folder
-  Model performance summary is exported as pkl/model_accuracy.csv


## Interpretation of Results

### Accuracy Measures

- CV_RMSE → Shows how far predictions are from actuals on unseen data; lower values mean more accurate and reliable forecasts.
- Train_RMSE → Measures how closely the model fits past data; lower values indicate a tighter fit, but a big gap vs. CV_RMSE signals overfitting.
- Train_R² → Explains how much of the variation in the target is captured by the model, with higher values meaning stronger predictive power.

### 1. Revenue 

<img width="959" height="473" alt="Screenshot 2025-09-04 at 18 19 23" src="https://github.com/user-attachments/assets/eb1041ba-6dc4-4e56-bc6a-329eafaa198d" />

With CV_RMSE ≈ 60.7, Train_RMSE ≈ 45.3, and R² ≈ 0.62, the given model captures revenue, explaining about 62% of its variation. Through this plot it can be seen that the forecast can be used for budgeting, inventory, and staffing decisions. Anticipated dips can be addressed through targeted promotions (e.g., weekday happy hours), while peaks such as holidays call for increased inventory and staffing to prevent service bottlenecks.


### 2. Guests

<img width="959" height="473" alt="Screenshot 2025-09-04 at 18 27 51" src="https://github.com/user-attachments/assets/fc873e02-f3fa-4c02-a737-a20526157df3" />

CV_RMSE ≈ 71.4, Train_RMSE ≈ 65.1, and R² ≈ 0.40 indicate weaker predictive power, with only 40% of guest variation explained. While forecasts are noisy, they still highlight general demand trends. The restaurant can use them to prepare for busier vs. slower days, but should complement forecasts with reservations and walk-in monitoring for more precise staffing and seating plans.


### 3. Tax 

<img width="959" height="473" alt="Screenshot 2025-09-04 at 18 31 16" src="https://github.com/user-attachments/assets/4f453b99-e788-42b5-ab0b-e95d492d5810" />

With CV_RMSE ≈ 6.8, Train_RMSE ≈ 4.9, and R² ≈ 0.63, the model predicts tax collectiony. Since tax is directly tied to sales, these forecasts help ensure compliance and accurate financial reporting. Management can also use this to forecast government liabilities and maintain smoother cash-flow planning.


### 4. Transactions

<img width="959" height="473" alt="Screenshot 2025-09-04 at 18 31 57" src="https://github.com/user-attachments/assets/d4611407-4b3c-486e-9934-8a25cbd730e4" />

CV_RMSE ≈ 0.39, Train_RMSE ≈ 0.35, and R² ≈ 0.26 show limited explanatory power, with only about 26% of variation captured. This suggests customer purchasing behavior per transaction is harder to predict. Forecasts can still flag broad transaction trends, but the restaurant should supplement this with loyalty program data, basket analysis, or promotions to influence transaction counts more directly.


### 5. Tables

<img width="959" height="473" alt="Screenshot 2025-09-04 at 18 32 49" src="https://github.com/user-attachments/assets/41e92a79-4b69-4e76-a3a0-27fb723a1ec9" />

With CV_RMSE ≈ 0.31, Train_RMSE ≈ 0.24, and R² ≈ 0.40, the model moderately predicts table usage. This helps in planning seating capacity and wait-time management, especially during peak periods. Because accuracy is limited, real-time table monitoring remains essential to avoid overbooking or long customer waits.


### 6. Quantity 

<img width="959" height="473" alt="Screenshot 2025-09-04 at 18 34 46" src="https://github.com/user-attachments/assets/ee8632b9-67dc-436f-8bea-02ef23c709ab" />

CV_RMSE ≈ 10.6, Train_RMSE ≈ 8.4, and R² ≈ 0.56 reflect solid predictive strength, explaining more than half of order volume variation. This makes forecasts useful for inventory management and supply chain planning. Anticipated order spikes (e.g., weekends or events) can guide bulk purchasing and reduce the risk of stockouts, while slow days allow leaner inventory to cut waste.







