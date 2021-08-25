# Machine Translation from English to Hindi
## Translate Texts from English to Hindi using sequence to sequence Model ##
### Data set ###
Text data is downloaded from(https://www.kaggle.com/aiswaryaramachandran/english-to-hindi-neural-machine-translation?select=Hindi_English_Truncated_Corpus.csv)

### Libraries used ###
Tensor Flow, Keras, NLTK, Regex, Sklearn, Matplotlib, Numpy and Pandas.

### Text Preprocessing ###
Both the texts are processed using regex to remove unwanted words. sentences with suitable maximum length are selected.

### Model ###
Sequence to Sequence model is used.

![alt text](https://blog.kakaocdn.net/dn/cByx3E/btqDyNiSnP2/GX8SnhRzTR8zRwTk2KBoJ0/img.png)
 
English text tokens are passed to Encoder Embedding layers. Final hidden and cell states of LSTM unit are passed in as initial states to Decoder LSTM units to generate Hindi text tokens. 
Teacher forcing method is used to train the model. 

### Evaluation ###
BLEU(Bilingual Evaluation Understudy) score is used as Evaluation metric
0.375 BLEU score is obtained on Train and CV dataset and 0.37 on Test set.
