# TriNet-LSTM

3 different tasks(got dataset from kaggle)

NOTE : model will be trained individually on this dataset, we wont combine our datasets, also the output generated through it will also be seperate.
But a single model will be trained and inference also will be done using that model only.

emotion detection :

0:sadness
1:joy
2:love
3:anger
4:fear
5:surprise

violence : 

0:harmful_traditional_practice
1:physical_violence
2:economic_violence
3:emotional_violence
4:sexual_violence

hate:

0: hate_speech
1:offensive_speech
2:neither

Load and Analyze dataset.
1.head(), shape()

Data Preprocessing
1.removed unnecessary columns from dataset.
2.maintain consistent column names
3.check for missing values.
4.rows among all 3 datasets are highly scattered(emotion-4lakhs, violence - 39k, hate - 24k)
SO We create a balanced dataset by keeping ratio of all classes consistent.(Well we improvised it a bit)
5.Reset indices(as we created dataset by randomly picking samples)

Label Encoding
1. in violence_dataset label names are categorical so we need to encode them.

Stop Words Removal

Tokenization,
Padding
(Here text got converted to numpy arrays(because output hi vaisa hai))

Converting labels to numpy arrays as well


MODEL DEFINITON:
1.seperate input layers for all tasks
2.core layers remains the same and are shared(lstm+embeddings+pooling+dropout)
3.seperate output layers

MODEL ARCHITECTURE:

1.SEPERATE INPUT LAYERS
2.SHARED EMBEDDING LAYER
3.SHARED LSTM LAYER
4.SHARED GLOBAL AVERAGE POOLING LAYER
5.SHARED DROPOUT LAYER

PREDICTIONS(plotted confusion matrix and looked model performance)

MANUAL INFERENCE