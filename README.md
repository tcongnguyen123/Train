# Text Summarization
### What is text summarization ? 
Text summarization is the process of extracting the most important information from a text to create a short, concise version that provides the full amount of information of the original text along with grammatical correctness. and spelling.  
Two prominent approaches are extractive summarization (Extractive Summarization) and abstract summarization (Abstractive Summarization).
Extractive Summarization: is a summary whose output is a summary including all important parts extracted from the input text.
![image](https://github.com/tcongnguyen123/Train/assets/116703297/06498097-e605-4eef-8930-69df8956712d)

Abstract Summary (Abstractive Summarization): is a summary whose output is a summary that does not retain the components of the input text but relies on important information to rewrite a new summary text.
![image](https://github.com/tcongnguyen123/Train/assets/116703297/0d722256-29b9-4c29-817c-ecde2e711fae)

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


