# Named-Entity Recognition Using CRF and BERT

Named-entity recognition (NER) is a natural language processing technique. It is also called *entity identification* or *entity extraction*. It identifies named entities in text and classifies them into predefined categories. For example, extracted entities can be the names of organizations, locations, times, quantities, people, monetary values, and more present in text.

With NER, key information is often extracted to learn what a given text is about, or it is used to gather important information to store in a database.

#Problem Statement

My goal in this project is to extract named entities from movie trivia. For example, the tags could include movie names, actor names, director names, and movie plots. While general libraries might extract names, they don't typically differentiate between actors and directors, and it can be challenging to extract movie plots. Therefore, I need to build a custom model that predicts these tags for sentences about movies.

Essentially, I have a dataset that talks about movies. It consists of sentences or questions about movies, and each word in the sentence has a predefined tag. I need to build a Named Entity Recognition (NER) model to predict these tags.

Along the way, I found that to achieve this goal, I need to understand the following concepts:

1. Build the model using various algorithms.
2. Design a metric to measure the performance of the model.
3. Understand where the model fails and identify the reasons for the failures.
4. Fine-tune the model.
5. Repeat these steps until I achieve the best accuracy on the test data.

# BERT Transformer

BERT (Bidirectional Encoder Representations from Transformers) is a model that is trained on large data sets. This pretrained model can be fine-tuned as per the requirement and used for different tasks such as sentiment analysis, question answering system, sentence classification, and others. BERT transfers learning in NLP, and it is a state-of-the-art method.

BERT uses transformers, mainly the encoder part. The attention mechanism learns the contextual relationship between words and subwords. Unlike other models, Transformer's encoder learns all sequences at once. The input is a sequence of words (tokens) that are embed into vectors and then proceed to the neural networks. The output is the sequence of tokens that corresponds to the input token of the given sequence.

#CRF (Conditional Random Fields)
CRF is a conditional model class best suited to prediction tasks where the state of neighbors or contextual information affects the current prediction.

The main applications of CRFS are named-entity recognition, part of speech tagging,gene prediction, noise reduction, and object detection problems, to name a few.

In a sequence classification problem, the final goal is to find the probability of y(target) given input of sequence vector x.

Because conditional random fields are conditional models, they apply logistic regression to sequence data.

