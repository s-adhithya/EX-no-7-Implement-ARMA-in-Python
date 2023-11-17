# EX-no-7-Implement-ARMA-in-Python
## AIM :
To Write a Program to ARMA in Python

## Procedure:
1 .Import necessary libraries

2 .Simulate an ARMA(1,1) Process

3 . Plot the ARMA(1,1) Data

4 .Plot Autocorrelation and Partial Autocorrelation Functions for ARMA(1,1)

5 .Simulate an ARMA(2,2) Process and Plot Its ACF and PACF

## PROGRAM:
```
from pandas import read_csv
from pandas import datetime
from matplotlib import pyplot
from pandas.plotting import autocorrelation_plot
from pandas import DataFrame
from statsmodels.tsa.arima_model import ARIMA
from statsmodels.graphics.tsaplots import plot_acf, plot_pacf
from statsmodels.tsa.arima_process import ArmaProcess
import matplotlib.pyplot as plt
import numpy as np
import warnings
warnings.filterwarnings('ignore')
plt.rcParams['figure.figsize'] = [10, 7.5]
ar1 = np.array([1, 0.33])
ma1 = np.array([1, 0.9])
ARMA_1 = ArmaProcess(ar1, ma1).generate_sample(nsample=1000)
plt.plot(ARMA_1)
plt.title('Simulated ARMA(1,1) Process')
plt.xlim([0, 200])
plt.show()
plot_acf(ARMA_1)
plot_pacf(ARMA_1)
ar2 = np.array([1, 0.33, 0.5])
ma2 = np.array([1, 0.9, 0.3])
ARMA_2 = ArmaProcess(ar2, ma2).generate_sample(nsample=10000)
plt.plot(ARMA_2)
plt.title('Simulated ARMA(2,2) Process')
plt.xlim([0, 200])
plt.show()
plot_acf(ARMA_2)
plot_pacf(ARMA_2)
```
## OUTPUT:
### plt.plot(ARMA_1)
![image](https://github.com/s-adhithya/EX-no-7-Implement-ARMA-in-Python/assets/113497423/2749badb-7718-4b19-8d86-1e52896ae464)


### plot_acf(ARMA_1)
![image](https://github.com/s-adhithya/EX-no-7-Implement-ARMA-in-Python/assets/113497423/65e6bb7c-4499-47dd-a28b-06b5e1327c39)


### plot_pacf(ARMA_1)
![image](https://github.com/s-adhithya/EX-no-7-Implement-ARMA-in-Python/assets/113497423/6dee243b-2be8-4283-abc0-050637a21b74)


### plt.plot(ARMA_2)
![image](https://github.com/s-adhithya/EX-no-7-Implement-ARMA-in-Python/assets/113497423/7ba07c52-f62b-4a57-ac69-bc9c6a0444e1)


### plot_acf(ARMA_2)
![image](https://github.com/s-adhithya/EX-no-7-Implement-ARMA-in-Python/assets/113497423/695b6337-f317-4cb4-9b2f-16a4d7d22378)


### plot_pacf(ARMA_2)
![image](https://github.com/s-adhithya/EX-no-7-Implement-ARMA-in-Python/assets/113497423/1e95c389-beec-4629-8141-b68095bd9a61)


## RESULT:
Thus the program to ARMA model is written and verified using python programming.
