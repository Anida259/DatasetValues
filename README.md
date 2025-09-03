# Dataset Values


## 1. Create and activate virtual environment

   python3 -m venv venv

   - source venv/bin/activate   # On macOS/Linux
   - venv\Scripts\activate      # On Windows

## 2. Install dependencies

   pip install -r requirements.txt
   

## 3. Run the forecasting pipeline

   python main.py
   

## 4. Outputs

-  Forecast plots are saved in the plots/ folder
-  Trained models and accuracy metrics are saved in the pkl/ folder
-  Model performance summary is exported as pkl/model_accuracy.csv
