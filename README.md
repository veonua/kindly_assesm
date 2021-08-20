# Introduction

Intent classification is one of the main NLP tasks when building chatbots, or dialogue
management systems more generally. An intent in this context refers to the intention of the end
user. The goal of an intent classifier is to predict the user’s intent given a user generated
message and a predefined finite set of intents. As such, intent classification can be seen as a
text classification task in which the classes are the intents and the text is the user chat
messages, which tend to be short.
Whenever a user sends a message to one of our chatbots, the message is preprocessed,
encoded and sent to our intent classification service to predict the user's intent. If the 1
confidence score of the top prediction is greater than a predefined confidence threshold, the top
intent’s response will be presented to the user. Otherwise, the chatbot will default to a so-called
fallback message expressing that the chatbot was not able to find a satisfactory reply.

# Task

Given a set of training data, consisting of messages (i.e. strings) labelled with their ‘gold’ intents
(see the Data section below), your task is to design and implement an intent classifier where the
input is a message (i.e. text) and the output is the user’s intent (in the input message). Note that
only one intent (class) can be assigned to a given input message.
You are free to represent/encode the input text in whichever form or model you see fit—and you
can, of course, use pre-trained word- and sentence-embedding models if you wish.
Furthermore, you can use any neural network architecture(s) to implement the actual intent
classification model, but we would like to hear your thought process as to why you decided on
the final architecture, what are the benefits of your architecture and what problems you foresee
along the way, etc...
Note that we are not after the ‘perfect’ model, but during the interview we would like to learn
more about your reasoning, how to further improve your architecture and what you would like to
experiment with if you had more time (and data). Furthermore, we do not expect an exhaustive
(hyper)parameter tuning, but would like to hear your thoughts on why you decided on the
parameters and how you would tune them if you had the chance.

# Data

Attached is a JSON file called train_data.json which includes the intent IDs and a list of so-called
samples for each intent. Your model’s input X is the samples and your model output is intent
IDs.
You can either split the data in the file into training/development splits or run cross validation,
this is completely up to you; just make sure to explain this in your submission. We do have a
separate set of test data that we will use to evaluate your model.

# Submission

Please write your intent classifier using Python and Tensorflow and provide descriptive
comments where needed. In addition, please include a README file describing how to run your
code and detailing any assumptions you make about the data. The README file should also
include your evaluation results (e.g. precision, recall, F1 score) and training time. If you train
several models using different architectures or representations, please make sure to include
their results as well.
