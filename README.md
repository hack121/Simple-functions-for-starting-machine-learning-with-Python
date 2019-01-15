# Simple-functions-for-starting-machine-learning-with-Python
The current repository contains different functions implemented in Python to understand the basic steps to carry out a machine learning problem

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. See deployment for notes on how to deploy the project on a live system.

### Prerequisites

You need Python 3.x to run the following code.  You can have multiple Python versions (2.x and 3.x) installed on the same system without problems.

In Ubuntu, Mint and Debian you can install Python 3 like this:

    sudo apt-get install python3 python3-pip
    
For other Linux flavors, OS X and Windows, python is availabe at http://www.python.org/getit/.  


## File descriptions

* 'ETF_data' which is a univariate time series of the price history of the ETF.
* 'Main.py' which contains the main procedure, as well as the data pre-processing of the xlsx file 'ETF_data.xlsx'
* 'Monte_Carlo_GBM.py' which contains the different algorithms used for comparison.
* 'Post_processing.py' where all the functions for post-processing (plots, information, descriptive statistics) are implemented.

### Running the program

The code is ready to be used and just requires running the following command:

    $ python Main.py

The code is well commented and easy to understand. The different parameters calculated and used for the simulations are:
``` python
# S0 corresponds to the starting price of the stock
# sigma is the daily volatility
# mu correponds to the mean daily returns
# T is the number of years for the simulation
# n_days is the number of days of the simulation
# dt corresponds to the timestep of 1 day
# n_ETF corresponds to the number of ETF held
S0 = ETF_data.close[-1]
sigma = annual_sigma
mu = annual_return
T = 10
dt = 1/trading_days_per_year
n_ETF = 10000 / S0

# num_iterations is the number of times the random process is repeated (Monte Carlo simulations)
num_iterations = 100
```

After all simulations have been run, different graphs are generated to analyse the return of investment, as well as its variance. The 2 images below show some of the plots generated by the code.

<p align="center">
<img src="https://github.com/DavidCico/Study-of-buy-and-hold-investment/blob/master/Example_Results/analytic_exp_gbm.png" width="500" height="350"> <img src="https://github.com/DavidCico/Study-of-buy-and-hold-investment/blob/master/Example_Results/Hists_fig2.jpg" width="512" height="512" >
</p>


## Contributing

Please read [CONTRIBUTING.md](https://github.com/DavidCico/Study-of-buy-and-hold-investment/blob/master/CONTRIBUTING.md) for details on our code of conduct, and the process for submitting pull requests to us.

## Versioning

We use [SemVer](http://semver.org/) for versioning. For the versions available, see the [tags on this repository](https://github.com/your/project/tags). 

## Authors

* **David Cicoria** - *Initial work* - [DavidCico](https://github.com/DavidCico)

See also the list of [contributors](https://github.com/DavidCico/Study-of-buy-and-hold-investment/graphs/contributors) who participated in this project.
