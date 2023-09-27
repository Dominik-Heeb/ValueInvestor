# ValueInvestor

Apziva project #5 on time series forecasting<br>
2023 09 27

__Summary:__
* In this project I try to predict Microsoft stock market prices.
* First the library yfinance by Yahoo is explored:
	* Downloading 27 years of stock market prices.
	* Creating a utility function to display the extensive data retrieved (i.e. not only the price).
* Differencing the data to get a stationary time series.
* Evaluating three baselines:
	* Constant differences.
	* Linear trend in differences.
	* Using L2 to predict one day.
* Evaluating the ARIMA / SARIMA model:
	* Library: from statsmodels.tsa.arima.model import ARIMA
	* Simulating 6 artificial datasets to check the ARIMA results:
		* trend: constant, linear, exponential.
		* seasonality: with and without.
	* ARIMA / SARIMA does not produce reasonable results.
		* Trend and seasonality are not detected in the simulated time series.
		* The deviations in the Microsoft stock market prices are substantial.
* Evaluating the Prophet model:
	* Prophet is very strong on a demo car sales dataset.
		* Detects seasonality.
		* Forecasts future peaks properly.
	* Prophet fails with Microsoft stock market prices.