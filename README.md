# Predicting Image captions for assisting Blind Persons
According to the World Health Organization (WHO), it has been reported that there are around 285 million visually impaired people worldwide and out of these 285 million, 39 million are totally blind. It becomes really tough for these people to go through daily lifestyle work, one of which is reading. From reading a newspaper or a magazine to reading an important text message from your bank, it becomes tough for these blind people to go through the text written in it.


Imagine you went trekking recently with your family and enjoyed it a lot there. You clicked thousands of pictures there, pictures of nature, hills, forests, etc. You want to share your experience with a friend but unfortunately, he is not able to see the photos as he is blind. But you really want to make him realize what exactly the place looks like up there as it is one of his favorite trekking places. How will you be able to share your experience with him then?



Have you ever seen a blind person operate Facebook, Youtube, etc on his/her phone? Have you ever wondered how blind people can easily scroll through the news feed and understand what other people have shared across their timeline?



In 2010 Facebook launched a special feature that can help blind people operate Facebook on their respective mobile phones. The feature helped the blind person understand what he/she is typing. With the help of this feature, whenever the person tapped on a particular alphabet on the keypad, the application responded by speaking out that particular alphabet. Also, the feature could explain the blind person the contents of an image that their friends have posted on Facebook. So if someone posted a picture with their dog, the Facebook application would speak out the contents.


In this project, I understood how a blind person is able to overcome all these problems and how they are able to go along with normal people when it comes to seeing. I created a model similar to what Facebook made, specifically making the blind person know the contents of an image in front of them with the help of a CNN-RNN based model. The model will convert the contents of an image and will give the output in the form of audio output.

## Dataset
I have used Flickr8 dataset from Kaggle for reference here. It can be downloaded from below link:

`https://www.kaggle.com/shadabhussain/flickr8k`

## Attention Model
A “classic” image captioning system would encode the image, using a pre-trained Convolutional Neural Network that would produce a feature vector. This feature vector would remain the same while decoding the caption using RNN. However, with Attention model, we get a varying feature vector based on the previously generated word. This helps us to look on different parts of the image for better captioning.

 

When the RNN is generating a new word, the attention mechanism is focusing on the relevant part of the image, so the decoder only uses specific parts of the image.

## Model Prediction
- We use the BLEU, **BiLingual EvalUation Strategy**, measure to evaluate the result of the test set generated captions. The BLEU is simply taking the fraction of n-grams in the predicted sentence that appears in the ground-truth.
- BLEU is a well-acknowledged metric to measure the similarity of one hypothesis sentence to multiple reference sentences. Given a single hypothesis sentence and multiple reference sentences, it returns a value between 0 and 1. The metric close to 1 means that the two are very similar.