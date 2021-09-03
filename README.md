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

In the first part of the study, we will analyze search trends and specifically any unusual search trends
patterns in the month of May 2020.  After reading in the csv data: "google_hourly_search_trends.csv", we can
isolate the month of May 2020, and create a plot to visualize the search trends that month.


