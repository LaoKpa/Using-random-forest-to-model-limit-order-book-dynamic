# Using random forest to model limit order book dynamic
I use the random forest algorithm to forecast mid price dynamic over short time horizon i.e. a few seconds ahead. This is of particular interest to market makers to skew their bid/ask spread in the direction of the most favorable outcome. Most if not all the literature on the topic focuses on applying straight out of the box algorithm to create forecast at any point in time. The problem in a real life environment is different. A market maker can provide a standard bid/ask spread most of the time and only when she/he has a statistical hedge she/he can skew the spread in the direction given by the model. This is what I try to do here: creating a forecast only when a statistical hedge exists

I used Python scikit-learn library implementation of random forest. This GitHub repo contains the code, some sample data and the associated explanations (code comments). This repo is also associated to a post on my [blog](https://www.thertrader.com/). I'm happy for anyone to re-use my work as long as proper reference to it is made.

I wanted to thank [LOBSTER](https://lobsterdata.com/) for providing the dataset used here

## Code structure

The code is organised around 4 files. In each file there is a detailled explanation and what is done along with some commented lines of code.

**rf.labels.py**: Definition of labels used in the Random Forest model

**rf.features.py**: Definition of features used in the Random Forest model

**rf.calibration.py**: Calibration and test of the Random Forest model

**useful.py**: Various useful functions used in the other 3 files (work in progress)

