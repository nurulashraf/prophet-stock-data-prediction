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

## How to Use

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

4. **Open notebook**

   Launch Jupyter:

   ```bash
   jupyter notebook
   ```

   or

   ```bash
   jupyter lab
   ```

   Then open the notebook in the `notebooks/` folder.


## License

This project is licensed under the **MIT License**. See the [LICENSE](LICENSE) file for full details.

