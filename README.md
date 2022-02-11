# DCCMGARCH-DASH-APP

Project to to acquire the academic title “Master of Science (M.Sc.)” 
in the degree Business Administration
of the Berlin School of Economics and Law


Dash App that forecasts step-ahead VaR for intraday portfolio management

The App is found in the app.ipynb file. 

The App was written with Dash verison 2.0.0 and plotly 5.4.0.
These and further packages may need to be installed and are commented out in the beginning of the app.ipynb file.

The App runs on historical price data of the Dow Jones Index constituents provided in the .csv file.
The App.ipynb and prices.csv will need to be in the same directory to run succesfully.

Running the APP will also create temporary csv files in the directory.

Special thanks to Dr. Christian Contino for providing both the core programmatic solution for Engle's (2002) DCC multivariate GARCH model and additional advice.
See: https://github.com/tinoproductions/DirtyQuant/blob/master/DCC%20Model.ipynb

App Specifications:
  Model Input:
    5 days of Intraday 5-min returns are deseasonalized with a seasonality term according to Taylor & XU (1997)
  DCC Model:
    Univariate standard GARCH(1,1) with t-distributed errors
    Gaussian copula for multivariate dependence.
  VaR:
    Monte Carlo Method (95%) VaR using 5000 portfolio value simulations
    
Screenshots:

Tab1 (real-time risk):

![Tab1-1](https://user-images.githubusercontent.com/75901042/153585845-c1805512-e10f-4db1-a051-a594e477389c.png)
![Tab1-2](https://user-images.githubusercontent.com/75901042/153585851-56b41944-b15a-4976-ad3c-cc0b1c78f9f2.png)
![Tab1-3](https://user-images.githubusercontent.com/75901042/153585853-04a32690-e552-4c44-b99a-95c32d46ab52.png)

Tab 2 (end-of day risk):

![Tab2-1](https://user-images.githubusercontent.com/75901042/153585864-28a6b8b2-149f-474d-9264-f6ea56258a8a.png)

App Process Flowchart (from Dash debugger):
![cryptocite flowchart](https://user-images.githubusercontent.com/75901042/153585913-7662cc3e-a6c2-4aa8-910b-57d8da9a4481.png)






References:

Engle, R. (2002): Dynamic Conditional Correlation: A Simple Class of Multivariate Generalized Autoregressive Conditional Heteroskedasticity Models. In Journal of Business & Economic Statistics 20 (3), 339-350.

Taylor, S. J.; Xu, J. (1997): The Incremental Volatility Information in One Million Foreign Exchange Quotations. In Journal of    Empirical Finance 4, pp. 317–340. DOI: 10.1016/S0927-5398(9
