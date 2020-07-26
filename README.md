# Prediction Algorithim

##Problem Statement
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

#### Modelling
We used an RNN model for this. We defined a class called RNN with specified parameters - input_size, output_size, hidden_di and n_layers.
Then we generate evenly spaced, test data points with about 30% size; which created our train and test tensors. 

- Input size:  torch.Size([1, 186, 3])
- Output size:  torch.Size([186, 1])
- Hidden state size:  torch.Size([2, 1, 10])

Then we instantiate an RNN after tuning its hyperparametes a little and we choose an MSE loss and Adam optimizer with a learning rate of 0.01.

#### Training
Then comes the training part. We trained our model with 100 epochs and printing the model every 15epochs which totals to about 5 graphs. 
Our loss started with 0.9663447141647339 and ended with a final loss % of 0.01163563597947359
