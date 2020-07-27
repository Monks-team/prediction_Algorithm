# Prediction Algorithim

## Problem Statement
> To predict the COVID-19 positive cases from the 25th of 27 July to 15 August.
## Data
> We collected the data from  [..]() 
#### The dataset contains the following features
- county
- state
- fips
- cases 
- deaths
- region
1. About the Covid 19: 
COVID-19 is an infectious disease caused by the recently found virus known as SARS-CoV-2 (or coronavirus). Before the outbreak originated in Wuhan, China on December 2019, there was no information about this virus
The COVID-19 disease has been reported in approximately 215 countries and territories worldwide.

2. US STATS ABOUT COVID-19: 
With about 2.5 million coronavirus cases, the US has the highest number of confirmed infections in the world - about a quarter of the global total.
The situation got really bad in late March but by May, cases were declining and most states had begun to ease restrictions put into place to halt the spread of the virus.

3. The goal of the project is to develop a predictive algorithm to predict the number of positive cases in the US between 7/27/20 - 8/15/20.

4. Conclusion of the actions we took

#### Modelling
We used an RNN model for this. We defined a class called RNN with specified parameters - input_size, output_size, hidden_di and n_layers.
Then we generate evenly spaced, test data points with about 30% size; which created our train and test tensors. 

- Input size: [1, 186, 3]
- Output size: [186, 1]
- Hidden state size: [2, 1, 10]

Then we instantiate an RNN after tuning its hyperparametes a little and we choose an MSE loss and Adam optimizer with a learning rate of 0.01.

#### Training
Then comes the training part. We trained our model with 100 epochs and printing the model every 15epochs which totals to about 5 graphs. 
Our loss started with 0.9663447141647339 and ended with a final loss % of 0.01163563597947359
