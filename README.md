# AI-Shakespeare
### Introduction. 
This is an AI-Shakespeare project. It is a neural language model embedded into a mobile application. <br/>
### Poetry generation. 
Essentialy it is a AI-bot, which generates shakespeare-style poetry given an input from the user <br/>
### On-device. 
The model is built into mobile application, therefore it works offline and does not require an Internet connection.
### Inference. 
The inference time is 2 sec for 200 text characters.
### Char-embeddings. 
The model uses character embeddings derived from GloVe word embeddings to capture semantical meaning of the individual characters.
### Evaluation. 
The bpc (bits per character) metric on the test set is rather high since the model is really small (3m parameters, 3Mb after conversion), otherwise, it would not work on a mobile device. Still, it produces syntatically correct text and sometimes is rather coherent. 
### Working. 
The project is in working condition as you can see from the screenshot. Code for this project is not presented in this repo, but rather is private.


<img src="images/ai-shakespeare.png" width="250">
