# Image-captioning
A tensorflow 2.0 with keras implementation trained on MS COCO dataset.


# Introduction
The task of image captoning is the task of generating a sequence of words to descripe an encoded image.
It is done through the well known sequence-to-sequence architecture.
An encoder (of a mostly pretrained CNN model) encodes the image, then an RNN decoder outputs a word in each of its steps.


# Usage
You can either run image_captioning_train.ipynb for training the whole thing from the start while having the option of changing the hyper parameters or image_captioing.ipynb for captioing any image by giving its path.
In case you use the latter, make sure you have 'Encoder.hdf5','Decoder.hdf5' and 'tokenizer.pickle' downloaded. 


# Architecture
This is a seq2seq neural network that uses teacher-forcing.
Encoding is done through using inception_v3.
Feel free to change any of the parameters found in the configuration cell like LSTM_size, encoding_size or even the number of samples this network trains on.

# Example predictions
