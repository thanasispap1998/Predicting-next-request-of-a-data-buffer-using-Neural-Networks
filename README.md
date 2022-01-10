# Predicting-the-next-request-of-a-data-buffer-using-Neural-Networks

This project aims to show how to predict the next request of memory inside a buffer by using any Neural Network. In our case we will use an LSTM model.

First of all, all files mentioned below, except the report of course, must be placed in the same folder for the notebooks to properly work. In the GitHub repository they are separated in different folders only for the purposes of clarification and order.

This GitHub repository contains all the Jupyter Notebooks and any additional necessary files for this project to work. More specifically it contains:

1) a folder named "Notebook" containing the "Prediction" notebook

2) a folder named "Datasets" containing all two datasets used for the training and testing of the LSTM model

3) a folder named "Report" containing the report of this project

Here is a quick summary of the notebook:

The main idea is to build correctly the LSTM model so it can predict the next request of memory in the buffer. We import our training dataset, split it into training and testing parts, pick a smaller portion of data because my computer cannot handle the whole dataset, transform it to decimal from hexadecimal and instead of feeding it like that into the model we transform it even more. More specifically instead of using each data instance we use the difference between each consecutive number and finally "one-hot" code it in order to turn this problem into a classification prediction and not a regression one. The last part is necessary as we do not want the prediction to be a decimal number as close as possible to what we want but to either get the correct one or not. After that its just about tweaking the model itself with its layers and parameters in order to achieve the best possible accuracy and the least amount of error and shaping the data accordingly. After that we let it work and predict some numbers, change them back from the one hot coding to decimals, change them back to the original memory spots, because we used the difference between consecutive numbers, and finally compare them with the testing part. In the last part we just make new predictions using the testing dataset.

And here is a quick summary of the datasets:

Both datasets are full of hexadecimal numbers representing different spots of memory in the buffer.

The whole process for my computer lasted multiple hours for me. My hardware consists of 8 gigabytes of ddr3 ram and the first generation of i7 processor. They are undoubtedly very old components that are operating really slow and can easily terminate the execution when they reach their limits. In a newer and faster computer with ddr4 ram of 8 or more gigabytes and a faster newer processor this project should be executed much faster and give the opportunity to the user to use more data in the model.

Feel free to experiment with any algorithm, any process or even use totally different datasets from what I used!
