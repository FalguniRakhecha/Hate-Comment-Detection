#Hate-Comment-Detection

It is a deep learning project which is used to detect hate comments on social media. The model will predict if the comment you have entered is a hate comment or not.

#How I built it?

#DATASET The model uses a large dataset which is stored inside a CSV file. This is the link to download the dataset and understand how the dataset looks like. https://www.kaggle.com/competitions/jigsaw-toxic-comment-classification-challenge/data

#INPUT The input to our model are the comments or series of comments present in the dataset. i.e. input will be in string format.

#LABELS The csv file format or input in the string format is not very suitbale for processing our data so it is converted to binary format which is easy to process. The comments in dataset are associated with their binary labels attached to them. For example each comment have some attributes attached to them like moderately toxic, sevearly toxic, etc (for more detail understanding of how the dataset looks like check the link I have provided above.

#DATA PROCESSING For processing the data I have first converted it to tokens. Each word of comment in input are given an integer value. i.e. series of comments are converted to sequence of numbers like '1' for "is" '2' for "and", '3' for "hate" and so on. To take my model a step forward I have embedded these tokens. Embedding will represent certain attributed about each word. The deep neuron network learn the attributes itself and do the embedding.

#DEEP NEURON NETWORK Lastly, for DNN I have used LSTM layer since it is good with sequences. The labels which I created before are serialized using H5 format which helped me to save the trained DNN in the disk or hard-drive. The output of LSTM layer are a series of 0's and 1's which are mapped back to labels.

Taking it one step forward I have integrated the model into a gradio app.
