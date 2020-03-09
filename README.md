
## Basic Usage
To run the code, please go to folder src/
<br/>``cd src/``

### Attack
Running our social link inference attack on the New York data with each user having at least 20 check-ins:
<br/>``python main_attack.py ny 20``

### Defense
Hiding 60% of the check-ins for defense:
<br/>``python main_hiding.py ny 20 60``

Replacing 60% of the check-ins with a 15 step random walk for defense:
<br/>``python main_replace.py ny 20 60 15``

### Utility
Measuring the utility after hiding 60% of the check-ins:
<br/>``python main_utility_hiding.py ny 20 60``

Measuring the utility after replacing 60% of the check-ins with a 15 step random walk:
<br/>``python main_utility_replace.py ny 20 60 15``

## Requirements
* pandas
* numpy
* scipy
* scikit-learn

It is recommended to install [Anaconda](https://www.continuum.io/downloads), a python data science distribution, which includes all the above packages.
