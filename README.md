# Evaluating-Grammatical-error-corrrection
Using Deep Learning model and NLP to detect the grammatical errors and used to realize grammatical error detection and automatic correction.

# Project Description:
The main purpose of this task is to check out grammatical errors in English sentences and correct them. Grammatical error detection and correction are important applications in the automatic proofreading of English texts and in the field of English learning aids. With the increasing influence of English on a
global scale, a huge breakthrough has been made in the task of detecting English grammatical errors. Based on machine learning, this paper designs a new method for detecting grammatical errors in English composition. First, this paper implements a grammatical error detection model based on Attention concat Model. Second, this paper implements a grammatical error detection and correction scheme based on the Benchmark char model. char model performs better than most grammar models. Third, this paper realizes the application of the Benchmark word model in grammar error detection and error correction tasks, and the generalization ability of the model has been significantly enhanced. This solves the problem that the forward and backward cannot be merged when the Benchmark trains the language model. Through the
combination of traditional model and deep model, the advantages are complemented to realize grammatical error detection and automatic correction.

# Attention concat model:
 It approaches the Encoder Decoder type mechanism was used in which the input sentence is passed to the encoder which outputs the fixed length of vectors.
The output of the encoder is passed to the decoder which provider the translated output.
 BLEU Score =  0.4344177372922657 is considered as average as it is not the best or worst fit for this data set

# Char level model:
 A encoder decoder model consists of LSTM or GRU cells, encoder reads input sequence and summarizes the information in the form of hidden and cell state which is used to initialize the decoder and pass the start of sentence token to decoder at initial word and we expect model to predict the next word in the sequence.
 BLEU score =  0.21056889515735847
 
# Word level model:
 So far none of model give satisfactory results, now let’s try some complex models which have already proven to be good in other similar NLP tasks like machine translation. For this I have tried with Luong attention with dot scoring function due to compute limitation, although you can try with bahdanu attention and general and concat scoring function. 
 Triain BELU Score =  0.4603018211234794 and this model has better score than other models 
 
 # Conclusion:
  ![image](https://user-images.githubusercontent.com/81823968/227157386-1f20b057-3248-43c1-878e-1e1a6f2e1b87.png)
 
from the above image we can understand that attention concat model is better than simple encode-decoder models as of the performance does not differ much from other models. We can also observe that the BLEU score for beam search is better than the greedy search as expected.
 
