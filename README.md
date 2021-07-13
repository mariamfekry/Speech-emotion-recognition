# Speech-emotion-recognition
This is an assignment for Pattern Recognition Course taught at Alexandria University, Faculty of Engineering offered in Spring 2021. We intend to perform Speech emotion recognition . speech emotion recognition means that we can classify the speaker's emotion from their voice this is implemented using CNN model on CREMA dataset ,hoping to get the best accuracy possible .
# CREMA-D DATASET
the dataset can be obtained from the following link
https://www.kaggle.com/ejlok1/cremad
# Loading the audio files
the audio wav files were uploaded using Librosa with sample rate 16,000 , some preprocessing was done on the audio before feature extraction and augmentation , scielnce was trimmed and padding was added to make all audio files 3s

# Feature extraction 
for the 1D model features as zero crossing rate , energy , rms , mfcc(Mel Frequency Cepstral Coefficients) and cstft ( Chroma short time frequency transform) are extracted,
while for 2D model the feature space is Mel spectrogram of the audio.
# Augmentation
some audio augmentation was done for the feature space of 1D model : shift and noise were added
while for 2D model: frequency mask for the mel spectrogram was added , augmentation could have been done before generation of the mel spectrogram such as adding noise , pitch or other features.
# 1D model Results 
Multiple trials were done but the best results were obtained using 80:20 splitting ratio for training set and test set respectively , validation is 10% , the results obtained for the final model are 
validation Accuracy : 50.5%
test accuracy : 51.2%
# 2D model Results 
After several ttrials batch size 16 and 1000 epoch using RMSprop optimizer produced the best results on the current model with splittig ratio 70:30 for the training and testing with 5% validation set
the following results where obtained 
Validation Accuracy: 56.3%
Test Accuracy: 57.09%
# further Improvements 
1.The architectures of the models could be more complex adding more layers

2.Experimenting with adding more features for the 2D model dataset 
