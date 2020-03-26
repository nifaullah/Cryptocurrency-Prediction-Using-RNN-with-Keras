# Crytocurrency Prediction using Recurrent Neural Network (RNN)
In this exercise/project I am trying to predict if the value of a cryptocurrency will  increase / decrease in next 3 minutes based on the previous 60 minutes of data

**Goal:** 
1. Understand how RNN works for sequence data (i.e time series data in this case)
2. Use RNN to predict if prices will go up or down in the next 60 minutes

**Dataset:**

Data is downloaded from <a href="https://pythonprogramming.net/static/downloads/machine-learning-data/crypto_data.zip">Python Programming Tutorial </a>. It consists of 4 columns of data for each of the 4 cryptocurrency (Bitcoin, Bitcoin Cash, LiteCoin and Etherirum) being analyzed. Analysis is restricted to only 2 columns volume and close as these are the columns that are majorly used to figure if the currency is increasing or not

**Approach:**

In this excercise/project I am trying to reproduce the Cryptocurrency Prediction using RNN by the excellent <a href="https://www.youtube.com/channel/UCfzlCWGWYyIQ0aLC5w48gBQ">Harrison Kinsley</a> of <a href="https://pythonprogramming.net"> Python Programming Tutorial </a>. Here I am trying understand to how to use RNN practically on a proper sequential dataset. Initially data is loaded and processed such that we have a sequence of 60 minutes for each of 2 columns of 4 cryptocurrencies as 1 datapoint i.e 8 values corresponding to 2 columns(volume and close) of 4 crytocurrencies (bitcoin, bitocoin cash, litecoin and etherium) for 60 continuous minutes amount to 1 datapoint and the label is whether the currency will go up (1) or will go down(0) in next 3 minutes. After preprocessing the data I fit this data on a very general model with LSTM cells. 

<b>*</b>Although the code for the excercise is readily available, but I  have taken only the approach from the excercise and tried to code the whole excercise as per my understanding *(ofcourse there're some parts which will be similar due to the similarity of the operations but majorly this is an independent implementation accounting for some new upgrades and developments since the work was published.)*

**Results:**
In terms of train & validation accuracy, traditionally 50-60 % accuracy is a very subpar performance, but as per Harrison Kinsley this is good performance given the context of having to predict if the currency will go up or down in next 3 minutes based on previous 60 minutes worth of data. With this excercise I can now not only draw out the implementation in paper but also imagine the flow of data much quickly, all in all this was a good excercise to grasp how RNN implementation works with keras.

**Future Works:**
I believe one can further increase the accuracy by appropriately adjusting the model but even with the adjustments I don't believe the accuracy is going to shot up substantially but with increased data the results might be different.

**Citations/Acknowledgements:**

1. This is a reproduction of <a href="https://pythonprogramming.net/cryptocurrency-recurrent-neural-network-deep-learning-python-tensorflow-keras/">Crypotocurrency prediction with RNN, Deep Learning, Python, Tensorflow, and, Keras</a>  work  from  <a href="https://pythonprogramming.net"> Python Programming Tutorial </a>
2. This analysis or model building was done using <a href="https://colab.research.google.com/notebooks/intro.ipynb">Google Colab </a>
3. <a href="https://medium.com/@oribarel/getting-the-most-out-of-your-google-colab-2b0585f82403">Medium Post</a> on Google Colab By Ori Bar-El 
