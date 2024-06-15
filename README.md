# Text Summarization
### What is text summarization ? 
Text summarization is the process of extracting the most important information from a text to create a short, concise version that provides the full amount of information of the original text along with grammatical correctness. and spelling.  
Two prominent approaches are extractive summarization (Extractive Summarization) and abstract summarization (Abstractive Summarization).
Extractive Summarization: is a summary whose output is a summary including all important parts extracted from the input text.
![image](https://github.com/tcongnguyen123/Train/assets/116703297/b9afecb9-dcdc-4b84-a306-eab0b9c9aa77)


Abstract Summary (Abstractive Summarization): is a summary whose output is a summary that does not retain the components of the input text but relies on important information to rewrite a new summary text.
![image](https://github.com/tcongnguyen123/Train/assets/116703297/f7e7ca96-be56-457e-90b7-2dde5f32d3b4)


### Preprocessing 
![image](https://github.com/tcongnguyen123/Train/assets/116703297/1e9b5efe-1a1b-46cd-a3ef-4d2098969d5e)
![image](https://github.com/tcongnguyen123/Train/assets/116703297/1e7b6edb-afee-4977-b21f-46e3d9873021)

- Delete special characters
- Delete link
- Delete blank spaces
- Convert uppercase letters to lowercase
- Delete Vietnamese and English stopwords

![image](https://github.com/tcongnguyen123/Train/assets/116703297/c6a92cf8-5279-40ae-8174-823d0a61daae)
Split Vietnamese words using VnCoreNLP library

![image](https://github.com/tcongnguyen123/Train/assets/116703297/a94e80f8-f202-469a-b23c-4c0a63b22020)

### Build Model 
1. Text Summary model with just LSTM  
![image](https://github.com/tcongnguyen123/Train/assets/116703297/76429e17-721d-40a5-84c3-3c93685001c6)

Both encoder and decoder have LSTM only

_Result_
![image](https://github.com/tcongnguyen123/Train/assets/116703297/8d71fc88-cf5f-478a-8966-35f66b22622e)
![image](https://github.com/tcongnguyen123/Train/assets/116703297/c9e6540c-19b9-4f33-bd11-1ddb58fc7c79)

2. Text Summary model with Bidirectional LSTM
Bidirectional LSTM (BiLSTM) parallel long short memory neural network
Both encoder and decoder have Bidirectional LSTM

_Result_
![image](https://github.com/tcongnguyen123/Train/assets/116703297/3db8ba2f-8df5-4a4f-92f0-a2233db2359f)
![image](https://github.com/tcongnguyen123/Train/assets/116703297/7b6f13e3-14e1-4680-92c5-708734c64d68)

3. Text Summary model with Transformer :
![image](https://github.com/tcongnguyen123/Train/assets/116703297/15b4f25e-1678-4071-bf1f-7186a2d5c93c)

### Evaluate
To evaluate the accuracy of the models, the team ran the models with the test data set, and used the ROUGE method. ROUGE stands for Recall Oriented Understudy for Gist Evaluation, this is a method considered standard and widely used in research on text summarization.

![image](https://github.com/tcongnguyen123/Train/assets/116703297/1649dd7d-524d-4a4e-93e7-4c381bb8f17c)

### Improve in the future

To increase the accuracy of the model, an important condition is to build a better quality word2vec input data set, more accurately showing the correlation and relationship between words and tokens. Therefore, building a large and rich data set on topics and diverse vocabulary is essential for the Vietnamese text summarization model.
Or the group will focus on a certain topic such as: education, sports, entertainment... To increase the accuracy of the model.
