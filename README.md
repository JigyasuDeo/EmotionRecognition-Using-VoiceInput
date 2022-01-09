# EmotionRecognition Using VoiceInput

## About :
I have to recognize the emotion of a person by taking his/her voice as the input. For this project the emotion doesn’t depend on the words of speaker it only depends on tone and pitch of what speaker spoke.
I am recognizing 7 emotions :- anger, disgust, fear, happiness, neutral, sadness, surprise.

## Methodologies :
Mel Scale, Spectrogram, CNN, Transfer Learning

## DATASET :
Link :- https://www.kaggle.com/barelydedicated/savee-database


## Process :
 # I.	Dataset Preparation
  -> As described above dataset is divided into 4 speakers each consisting 7 different emotions, so we need to filter the whole data to 7 different emotions. 
     It means 1 emotion is shown by 4 different actors having 15 tracks of each actor therefore total 60 tracks for one emotion. 

  -> As this project is purely based on pitch and tone of speaker therefore we have to extract them from the “.wav” file which we have.

  -> There are many ways to achieve that, I have use Mel-Spectrogram to extract the feature like frequency in the form of spectrogram so that I can use them in my CNN Model.
  
  ![image](https://user-images.githubusercontent.com/59115506/148681786-02ec05e0-8141-4902-8c7a-cb334df11cfe.png)

  
  
 # II.	Training Model
 -> I have used CNN and Transfer Learning for training my model.
 
 -> As CNN works on image architecture I have converted my “.wav” file into Mel-Spectrogram as stated in the data preparation step.
 ![image](https://user-images.githubusercontent.com/59115506/148681818-dfe71912-70e7-435c-a1eb-4ac2256411eb.png)

 
 -> As my dataset is small (consisting of only 480 tracks) I have used transfer learning, using Pre-trained weight of ImageNet models and adding my layers to it.

# III.	Testing of Model
 -> For testing input is given from my own side by recording the voice.
 
 -> After the voice get recorded I will convert it to “.wav” file with proper configuration.
 
 -> For recording the voice in Google Collab we use python with Java Script. 
 
 -> This “.wav” file is then converted into Mel-Spectrogram so that it can be passed to the model for prediction.
