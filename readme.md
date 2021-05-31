# voa-data-project



![](CPSpaces.png)

This project illustrates building a machine learning model to perform a regression task.  Specifically an Automated Valuation Model (AVM) is created to predict the 'rateable value' of commercial properties in England and Wales.  There are currently three Jupyter notebooks covering:

1. Initial data processing and exploratory analysis
2. Data visualisation
3. Creating a machine learning model

The main packages used are: pandas, geopandas, LightGBM FLAML, Shap and scikit-learn.

## Data

The data source for this analysis is a list of the rateable values of 2 million commercial properties in England and Wales.  This data is maintained and provide by the Valuation Office Agency ("VOA").  The VOA is an executive agency of the UK government responsible for providing the valuations and property advice needed to support taxation and benefits.  The data can be downloaded [here](https://voaratinglists.blob.core.windows.net/html/rlidata.htm).  Please be sure to review the terms and conditions on that page before accessing the contents of this repository.

In addition, a shapefile of postal areas for England and Wales was obtained from the University of Edinburgh [DataShare](https://datashare.ed.ac.uk/handle/10283/2405).  Citation:  Crone, James. (2017). GB Postcode Areas, [Dataset]. University of Edinburgh. https://doi.org/10.7488/ds/1755



## Overview of Modelling Process

The following chart gives an overview of the modelling process.



![](processflow.png)



## Operational Deployment

Predictions from the model can be obtained from the user-friendly [online calculator](https://voa-ui-app.herokuapp.com/).  

This is a Dash app running on Heroku.  The model LightGBM model is deployed as an API using Flask and also running on Heroku.  The calculator app simply submits an HTTP POST request to the model API in order to obtain predictions, when triggered by the user.

![VOA UI](C:\Users\paul_\voa-data\VOA UI.png)