# *Forecasting Net Prophet*
---
With over 200 million users, MercadoLibre is the most popular e-commerce site in Latin America.
In this jupyter notebook, we will analyze the company's financial and user data and predict search
traffic.  With the forecasted data, we can translate search traffic into successfully trading the 
stock.  We will also analyze daily historical sales figues and be able to forecast future sales 
revenue for the finance group.

---
## Technologies and Usage:

Instead of running Facebook Prophet on your local machine, using Google Colab would be ideal to
run Facebook Prophet.  You can 'Upload' the Jupyter notebook after landing on https://colab.research.google.com

Install and import the required libraries and dependencies in Google Colab:
```python
  pip install pystan
  pip install fbprophet
  pip install hvplot
  pip install holoviews 

  import pandas as pd
  import numpy as np
  from pathlib import Path
  import holoviews as hv
  from fbprophet import Prophet
  import hvplot.pandas
  import datetime as dt
  %matplotlib inline  
```

In the first part of the study, we will analyze search trends, specifically any unusual search trends
patterns in the month of May 2020.  After reading in the csv data: "google_hourly_search_trends.csv", we can
isolate the month of May 2020, and create a plot to visualize the search trends that month.
![search_trends_may_2020](https://github.com/kevin-mau/forecasting_net_prophet/blob/main/Resources/search_trends_may_2020.png?raw=true)
With the median monthly traffic at our fingertips, we can calculate that the search traffic increased
by 8.55% the month that MercadoLibre released its financial results in May 2020.

We are also able to plot the search trends by day of the week, as well as create a heatmap to further 
investigate the google search trends by hour of the day.
![search_trends_by_day](https://github.com/kevin-mau/forecasting_net_prophet/blob/main/Resources/search_trends_by_day.png?raw=true)
![search_trends_heatmap](https://github.com/kevin-mau/forecasting_net_prophet/blob/main/Resources/search_trends_heatmap.png?raw=true)

In the next part of our study, we will analyze the stock price of MercadoLibre, and see whether there is
correlations between search traffic and stock prices.  We will read in the data from "mercado_stock_price.csv", and
analyze the historical prices and create visualizations.
![close_price_plot](https://github.com/kevin-mau/forecasting_net_prophet/blob/main/Resources/close_price_plot.png?raw=true)
![close_vs_search](https://github.com/kevin-mau/forecasting_net_prophet/blob/main/Resources/close_vs_search.png?raw=true)
![close_vs_search2](https://github.com/kevin-mau/forecasting_net_prophet/blob/main/Resources/close_vs_search2.png?raw=true)



## Data:

The google_hourly_search_trends.csv file is a CSV file that is historical daily data of google searches of
MercadoLibre.  The mercado_stock_price.csv is a historical record of the stock prices of MercadoLibre.

---

## Contributors

kevin-mau

---

## License

MIT