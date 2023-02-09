# Speech Emotion Recognition
[https://github.com/Naresh21061999/SPEECH-TO-EMOTION]

### INTRODUCTION
- This repository is made for handling model for Speech Emotion Recognition System.
- The main aim behind creating this project is to build a ML project that can detect emotions from the natural speech signal. The concept behind building this project is use Artificial Intelligence and Machine Learning Techniques to improve emotion recognition from speech interaction with computers. The Model is very useful for the industries working on products of HCI(Human Computer Interaction) Eg. Amazon Alexa, Google Assistant or other chatbots.

### ENVIRONMENT SETUP

Programming Language - Python3.8 (https://www.python.org/dev/peps/pep-0569/)

**(Setup pip command in python3.8 and then download below IDE's, Frameworks & Libraries|| Run all these pip commands in Command-prompt of windows or linux kernel)

IDE(Code Editor) - Jupyter notebook (pip install jupyter)

**Libraries -**

  	1.Tensorflow(pip install tensorflow)
  	2.Librosa(pip install librosa)
  	3.Keras (pip install keras)
	4.Pandas (pip install pandas)
	5.tqdm (pip install tqdm) --Download all other required libraries in similar way
  
  
### DATASET -
- 1.RAVDESS - Download all 24 Actors files(Speech+Song) of RAVDESS(https://zenodo.org/record/1188976) dataset and put all 24 actor folders in 'dataset_files/RAVDESS/' folder.
- 2.Download all files* from TESS(https://tspace.library.utoronto.ca/handle/1807/24487) dataset & put them in 'dataset_files/TESS/' folder.


### MERGING BOTH DATASETS (RAV-TESS) -
Now run the script 'Tess_Pipeline.ipynb' shell-by-shell.
This will create two additional folders Actor-25 and Actor-26 in 'dataset_files/RAVDESS/' and all files from 'dataset_files/TESS/' will be copied with renaming(according to RAVDESS naming convention) into 'dataset_files/RAVDESS/Actor-25or26'.

### DATA CLEANING - 
Now open the script 'Dataset_Cleaning.ipynb' and run it.
This process will take some time as it will clean each audio file from merged dataset by removing noise from it and  will save in '/Final_Cleaned_Dataset/' folder.

### Data AUGMENTATION - 
Data Augmentation is a way to represent available data in deferent ways so that we can have more data to work on.
We here varying two parameters of audio to generate around 30,000 files from available files.

Before running 'Data_Augmentation.ipynb' scripts, first copy emotion wise all files from 'Final_Cleaned_Dataset' folder and put in '/Augmentation/[emotion_name]' Folder.
After copying all files, run 'Data_Augmentation.ipynb' scripts.

### GENERATING MODEL -

[important] Now go to '/CNN Model/SpeechToEmotionRecognition.ipynb' and run all scripts(except previous merging,cleaning & Augmentation).
Now the final CNN model will be generated after running all shell-scripts and results will be saved in pictures folder & Accuracy will be displayed.


### TESTING MODEL - 
Now in order to test generated model for live predictions, open 'Live_Prediction.ipynb' and add path of your speech filenames at place of 'Recordings.wav' in bottom scripts.
	NOTE: If you are using the model directly and want to decode the output ranging from 0 to 9 then the following list will help you.
	'0': 'neutral'
	'1': 'calm'
	'2': 'happy'
	'3': 'sad'
	'4': 'angry'
	'5': 'fearful'
	'6': 'disgust'
	'7': 'surprised'

### Conclusion
Building the model was a challenging task as it involved lot of trail and error methods, tuning etc. The model is very well trained to distinguish between different emotions with overall accuracy of more than 90%. Accuracy can be increased by applying transfer-learning along with CNN algorithm wirh same model.
<br>
Thanks,

