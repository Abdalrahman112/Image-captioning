# Image-captioning
A tensorflow 2.0 with keras implementation trained on MS COCO dataset.


# Introduction
The task of image captoning is the task of generating a sequence of words to descripe an encoded image.
It is done through the well known sequence-to-sequence architecture.
An encoder (of a mostly pretrained CNN model) encodes the image, then an RNN decoder outputs a word in each of its steps.


# Usage
You can either run image_captioning_train.ipynb for training the whole thing from the start while having the option of changing the hyper parameters or image_captioing.ipynb for captioing any image by giving its path.
In case you use the latter, make sure you have 'Encoder.hdf5','Decoder.hdf5' and 'tokenizer.pickle' downloaded. 
the encoder and decoder can be found in release.


# Architecture
This is a seq2seq neural network that uses teacher-forcing.
This model doesn't use attention mechanism, which i might add later to another model
Encoding is done through using inception_v3.
Feel free to change any of the parameters found in the configuration cell like LSTM_size, encoding_size or even the number of samples this network trains on.

# Google colab links
You can get the notebooks uploaded here via google colab through these links:

[Training notebook](https://colab.research.google.com/drive/1VRQO7_r18a5rK68huvwKgNQOEGlzz3lm?usp=sharing)

[Prediction notebook](https://colab.research.google.com/drive/1OQEMKfT5BrTJpOwu__2u_tmNs8ADeQ6v?usp=sharing)

# Example predictions
![Prediction1](https://scontent.fcai1-2.fna.fbcdn.net/v/t1.15752-9/96286228_934101440372416_1710498101753544704_n.png?_nc_cat=100&_nc_sid=b96e70&_nc_ohc=v68QTdYdXxQAX_N0Mrt&_nc_ht=scontent.fcai1-2.fna&oh=d10c6903515d3e2539f903b2b1d4422d&oe=5EDD55AE)

![Prediction2](https://scontent.fcai1-2.fna.fbcdn.net/v/t1.15752-9/96266982_1181915348810137_520784176417341440_n.png?_nc_cat=102&_nc_sid=b96e70&_nc_ohc=YrZuEwnnEggAX-0IU7r&_nc_ht=scontent.fcai1-2.fna&oh=b74967c640a0bac85ac158464e186f4f&oe=5EDCEE2A)

![Prediction3](https://scontent.fcai1-2.fna.fbcdn.net/v/t1.15752-9/96392008_167857181290825_8070821355429298176_n.png?_nc_cat=103&_nc_sid=b96e70&_nc_ohc=XGWgpK512-4AX_fL2BW&_nc_ht=scontent.fcai1-2.fna&oh=54799acaf57e58c650a89a14a02f9d24&oe=5EDE45C8)


![Prediction4](https://scontent.fcai1-2.fna.fbcdn.net/v/t1.15752-9/96498039_2870854853005986_2413426455305256960_n.png?_nc_cat=106&_nc_sid=b96e70&_nc_ohc=RJCYRIdOLoAAX8rvjE4&_nc_ht=scontent.fcai1-2.fna&oh=7bb1ad4928a6a0a535e8b2836dfaa1a3&oe=5EDE868B)
