# Language modeling for mobile devices
### Introduction. 
It is a neural language model embedded into a mobile application. <br/>
### Poetry generation. 
Essentialy it is a AI-bot, which generates poetry given an arbitrary input from the user <br/>
### On-device. 
The model is built into mobile application, therefore it does inference offline, operates with low latency and does not require an Internet connection. 
<br> This was the hardest part to do because: <br>
- the size of the model had to be really small to work on a mobile device. I managed to downsize the model by the factor of 14 by using characters (not words) as input and character embeddings; <br>
- there were no mobile APIs to use for LSTM/RNN networks for inference on a mobile device; 
- a mobile environment did not have any pre-built functionalities for statistical distributions (I had to write it myself), which were needed as a final step after softmax activation.
### Inference. 
UPDATE: The inference time is 1.2 sec for 300 text characters.
### Model: Character-level model and char-embeddings. 
The model is LSTM network with some additional fully-connected layers. It works on character-level and uses character embeddings derived from GloVe word embeddings to capture semantical meaning of the individual characters.
### Evaluation. 
The BPC (bits per character) metric on the test set is rather high since the model is really small (800k parameters), otherwise, it would not work on a mobile device. Still, it produces syntatically correct text and sometimes is rather coherent. <br/>
UPDATE: The same model gives a good result on the Penn TreeBank dataset with BPC score of 1.42, which is not bad at all for this tiny model.
### Working. 
The project is in working condition as you can see from the screenshot. Code for this project is private.

![Alt Text](images/ai-shakespeare.gif)

<img src="images/ai-shakespeare.png" width="350">


