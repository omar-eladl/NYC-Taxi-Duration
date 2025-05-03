# 🚖 NYC Taxi Trip Duration Predictor

Welcome to the NYC Taxi Trip Duration Predictor a handy tool that guesses how long your NYC taxi ride will take. Using a smart machine learning model, this app makes predictions based on where you start, where you’re going, and when you’re traveling. It comes with a cool web app built with Streamlit, so you can try it out yourself.


## Features

- 🚕 Precise Predictions with Ridge Regression: Optimized for accuracy using RandomizedSearchCV.  
- 🌟 Innovative Feature Engineering: Custom features like Haversine/Manhattan distances, time-of-day segmentation, and rush-hour flags.  
- 🌐 Interactive Streamlit Interface: Predict trip durations with ease.  
- 📊 Comprehensive Metrics Display: RMSE, R², and MAE for train, validation, and test sets.  
- 📈 Scalable Framework: Easily adaptable for other cities or datasets.

## Usage

1. Install dependencies:

   ```bash
   pip install -r requirements.txt
2. Start the Streamlit application:
   ```bash
   streamlit run Streamlit.py
3. Open your web browser and go to:
   ```bash
   http://localhost:8501

## Model Details

- Model: Ridge Regression with an optimized alpha parameter, fine-tuned using RandomizedSearchCV. 
- Features:  
  - Haversine Distance: Measures the real-world distance between pickup and dropoff points.  
  - Manhattan Distance: Captures NYC’s grid-like street layout for more accurate distance estimates.  
  - Distance Per Hour: Adjusts distance based on the time of day to reflect speed variations.  
  - Time of Day: Segments trips into morning, midday, evening, night, or late-night to capture temporal patterns.  
  - Rush Hour Flag: Identifies peak traffic hours (7-10 AM, 4-7 PM) to adjust predictions.  
  - Weekend Flag: Accounts for different traffic patterns on weekends.  
- Objective: Maximize the R² score through  feature engineering and hyperparameter tuning.  

## Results

Check out how well the NYC Taxi Trip Duration Predictor performs! Here are the key metrics for the model across the training, validation, and test datasets:

- Training Set:  
  - RMSE (log scale): 0.4720  
  - R² (log scale): 0.6126  
  - MAE (log scale): 0.3356  

- Validation Set:  
  - RMSE (log scale): 0.4743  
  - R² (log scale): 0.6111  
  - MAE (log scale): 0.3362  

- Test Set:  
  - RMSE (log scale): 0.4697  
  - R² (log scale): 0.6165  
  - MAE (log scale): 0.3345
