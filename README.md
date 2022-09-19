# LP_takehome

To convince my friend that machine learning is not just a buzzword, I would like to suggest an example of how machine learning could be used for early diagnosis of Alzheimer’s.

#### Motivation
When I was in middle school, I volunteered in a nearby convalescent hospital and had an opportunity to see many patients suffering from Alzheimer's disease. From an old lady calling me a sister to a patient swearing and complaining to the nurse, Alzheimer’s gave significant stress to the workers at the hospital as well as the families of the patients. Doing some research on Alzheimer's, I found out that the earliest symptom of Alzheimer's is changes in voice(due to changes in vocal cords or throat muscles). Using patients’ voice data and analyzing with machine learning would enable early detection of Alzheimer and fast response to target the disease from the earliest stage. 

#### Solution
Characteristic speech features that can be used to draw an accurate distinction between healthy individuals and those with mild Alzheimer’s(cost-effective and reliable method) to detect which stage of Alzheimer’s the patient is in.

#### Techniques
1) CNN(Convolutional Neural Networks)
Use : Keras, Python
Generate sound data for Keras : convert the voice data into data format(spectrogram) suited for Keras
Train and validate : make a test set to train for voice classification
Build Voice Classification CNN : binary classification(stage 0 and stage 3 of Alzheimer’s) and set the validation data(patients with/without Alzheimer’s), train the model

2) WaveGAN
Use : Tensorflow, Python 
Voice and speech analysis : WaveGAN is a tool used for unsupervised synthesis of raw-waveform audio(https://github.com/chrisdonahue/wavegan)
Label and condition voice data(concatenate and condition scaling)
Train waveGan with given datasets

#### Challenges
First challenge would be issues with handling medical data. It will be difficult to obtain quality voice data from hospitals. Also, since the data is patients’ personal information, it should be securely managed. 
Another challenge is precision of the model. Wrong diagnosis of Alzheimer’s disease would give significant amount of stress to the patients and their family. Analyzing different voices(tone, volume, etc) to detect Alzheimer with high precision will also be challenge to this project.
