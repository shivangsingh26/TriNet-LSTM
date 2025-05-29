# TriNet-LSTM

3 different tasks(got dataset from kaggle)

NOTE : model will be trained individually on this dataset, we wont combine our datasets, also the output generated through it will also be seperate.

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