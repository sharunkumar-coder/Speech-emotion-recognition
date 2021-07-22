# Speech-emotion-recognition

## Project Description

Detecting emotions is one of the most important marketing strategy in today’s world. 
For this reason, i have decided to do a project where we could detect a person’s emotions just by their voice .
 A example smart car slowing down when one is angry or fearful. As a result this type of application has much potential in the world that would benefit companies and also even safety to consumers

## Data sets used

 We got audio datasets with around 3000 audio files which were in the wav format from the following websites:
http://neuron.arts.ryerson.ca/ravdess/?f=3, <br>
http://kahlan.eps.surrey.ac.uk/savee/Download.html  <br>
The first website contains speech data which is available in three different format. <br>
1.Audio Visual – Video with speech <br>
2.Speech – Audio only <br>
3.Visual – Video only <br>

We went with the Audio only zip file because we are dealing with finding emotions from speech. 
The zip file consisted of around 2500 audio files which were in wav format.
The second website contains around 500 audio speeches from four different actors with different emotion

## Labelling

The next step involves organizing the audio files.
Each audio file has a unique identifier at every position , at  the 3rd position of the file name which can be used to determine the emotion the audio file consists. 
We have 8 different emotions in our dataset.
(e.g., 01-01-05-01-02-01-12.mp4) then this audio contain angry speech

Labels	emotion
0	Neutral
1	Calm
2	Happy
3	Sad
4	Angry
5	Fearful
6	Disgust
7	Surprised

## Feature Extraction
I used Librosa library in Python to process and extract features from the audio files
 Using the librosa library I was able to extract features i.e MFCC(Mel Frequency Cepstral Coefficient)

## Models Used

The next steps involve shuffling the data, splitting into train and test and then building a model to train our data.<br> 
I had built 3 types of model: <br>
1.MLP Classifier <br>
2.SVM  Classifier <br>
3.Convolutional Neural Network(CNN) <br>
 The MLP and SVM were not suitable as it gave me low accuracy. As My project is a classification problem where were categorize the different emotions, CNN worked best for me. 
 <br>
 ## working of model
 
 ![Blank diagram.jpeg](https://github.com/sharunkumar-coder/Speech-emotion-recognition/blob/103141390295c3aa0a110a2738484dfa14c63b84/Blank%20diagram.jpeg)
 
 
 ## classification report
 ![classification report.jpeg](https://github.com/sharunkumar-coder/Speech-emotion-recognition/blob/103141390295c3aa0a110a2738484dfa14c63b84/classification%20report.jpeg)

## Result and conclusion

After building numerous different models, I have found My best model as CNN model for our emotion classification problem. 
I achieved a validation accuracy of <b> 88% </b> with my existing model. <br>
Combining the two datasets, RAVDESS & TESS, increased accuracy
Further Improvement:<br>
More data can be collected to increase model accuracy and performance on all emotion classes.<br>
 Also can incorporate other learning mechanisms to compute the percentage of emotions for audio with mixed emotion.
 ![conclusion.jpeg](https://github.com/sharunkumar-coder/Speech-emotion-recognition/blob/2a3a10876a8e4a44dc9a2d8424f10310677ee0f2/conclusion.jpeg)
