# Stock Data Prediction using Prophet

A project to forecast stock price movements using Facebook’s Prophet library, based on historical stock data.  

## Project Structure

- `notebooks/` – Jupyter Notebooks for data analysis, model training and evaluation  
- `requirements.txt` – Python libraries needed to run the project  
- `LICENSE` – MIT Licence for this project  
- `README.md` – this file with overview and instructions
  
## Features

- Load historical stock data (e.g. via CSV or APIs)  
- Data preprocessing (cleaning, formatting) to make it compatible with Prophet  
- Time series forecasting using Prophet for future predictions  
- Plotting and visualization of historic vs predicted values  
- Quantitative evaluation (e.g. error metrics)  
- Jupyter notebooks for interactive exploration  

## Tools & Libraries

- **Python**
- **pandas**
- **matplotlib**
- **yfinance**
- **fbprophet**
- **jupyterlab / jupyter notebooks**

You’ll find all required versions and packages in `requirements.txt`.

## Installation & Setup

1. Clone the repository:

   ```bash
   git clone https://github.com/nurulashraf/prophet-stock-data-prediction.git
   cd prophet-stock-data-prediction
   ```

2. (Optional) Create and activate a virtual environment:

   ```bash
   python3 -m venv venv
   source venv/bin/activate       # On Windows: venv\Scripts\activate
   ```

3. Install dependencies:

   ```bash
   pip install -r requirements.txt
   ```

4. (Optional) Prepare your stock data file(s) in CSV or format required by the notebooks/scripts.

## Usage

Here’s how you can use the project:

1. Open one of the notebooks in the `notebooks/` folder (e.g. `model_training.ipynb`) via:

   ```bash
   jupyter lab
   ```

2. In the notebook, load your stock price data into a DataFrame. The data should include at least two columns:

   * `ds` or a date/time column (timestamp)
   * `y` or the target value to forecast (e.g. closing price)

3. Preprocess your data (e.g. fill missing values, convert date types) so that it matches input format for Prophet.

4. Create and fit a Prophet model:

   ```python
   from prophet import Prophet

   m = Prophet()
   m.fit(train_df)
   ```

5. Make predictions:

   ```python
   future = m.make_future_dataframe(periods=30)  # e.g. 30 days ahead
   forecast = m.predict(future)
   ```

6. Visualize results:

   ```python
   fig = m.plot(forecast)
   fig2 = m.plot_components(forecast)
   ```

7. Evaluate model’s performance (e.g. comparing predictions vs actuals using RMSE, MAE, etc.).

8. (Optional) Experiment with hyperparameters, seasonalities, additional regressors, etc.

## How It Works

* **Data ingestion**: Load historical stock price data (e.g. from CSV or an API)
* **Preprocessing**: Clean, format and transform data into the structure needed by Prophet (`ds`, `y`)
* **Modeling**: Use Prophet to fit a time series model
* **Forecasting**: Generate future predictions
* **Visualization**: Plot the trend, components (seasonality, holidays, etc.), and prediction vs actual
* **Evaluation**: Compute error metrics (e.g. RMSE, MAE) to assess forecast accuracy

You can also extend the pipeline by adding new regressors, tuning hyperparameters, or integrating with live stock APIs.

## Results & Evaluation

In the notebooks, you should see:

* Plots of historical data vs forecast
* Component plots (trend, yearly/weekly/seasonal)
* Tables or metrics summarizing model error and performance
* Possibly cross-validation or backtesting results

You can expand further by comparing the results for different stocks, time windows, or modeling configurations.

## Contributing

Contributions are welcome! If you’d like to improve this project:

1. Fork the repository
2. Create a new branch (`feat/your-feature` or `fix/your-fix`)
3. Make your changes and add tests or documentation
4. Submit a Pull Request

Please ensure your code is well-documented, follows PEP8, and includes explanations where needed.

## License

This project is licensed under the **MIT License**. See the [LICENSE](LICENSE) file for full details.

