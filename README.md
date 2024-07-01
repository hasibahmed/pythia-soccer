# Installation 
The package dependencies are maintained by `poetry`. To install all the packages and dependencies: 

```
> pip install poetry
> poetry install 
```

# Task discussion & explanation

### Season 1: implemented in `01-S1-analysis.ipynb`

### Season 2 Predictions:

I approached the problem as I would approach any problem, systematically implement more complex solutions to make sure the results make sense and to compare the performance. 

I used simple feature selection: 
* Used only home and away goal scored and conceded information.
* Not using information about the players position, game week, shots. More complex features can be designed using these information. 

Prediction models:
* Frequentist method: implemented in `02-S2-Pred-Frquentist.ipynb`. Uses frequentist probability and models the goal scores as a poisson distribution. 
`Correctly predicts 323 match outcomes but gets 433 match outcomes wrong`. 

* Simple Bayesian method: implemented in `03-S2-Pred-Bayesian.ipynb`. Implements a simple Bayesian model using `numpy`, useful for quick calculations of simple models. Even this simple approach improved the prediction compared to the frequentist method.
`Correctly predicts 461 match outcomes but gets 295 match outcomes wrong`.

* Bayesian with MCMC: implemented in `04-S2-Pred-BayesianMC.ipynb`. Uses `PyMC` for modeling. Complex models can be implemented using this approach. This is the tool and method of choice. It improves over the previous method. 
`Correctly predicts 474 match outcomes but gets 282 match outcomes wrong`. Uses more features as discussed before the performance can be improved. 
