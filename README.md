# Face-recognition-with-emotion-detection-and-music-recommender

This repository contains code for face recognition and corresponding emotion detection. After the emotion is detected, it makes song recommmendations based on that emotion. An external piece of code is provided to directly make a spotify playlist of the recommended songs. 

- In the face recognition, the faces are first detected using MTCNN and the images are then cropped according to the ROI. From these cropped images, embeddings are then created using the Face-net architecture. After that the embeddings are classified using SVM. If there is dearth of data then in that case instead of SVM, a on-shot learning approach can be used using the cosine similarity function. The dataset used is provided in the drive link below.
- For emotion detection a simple CNN architecture is used on the FER13 dataset which is also provided in the drive link.
- For Song recommendationm, the spotify data is used which contains the track names, ids, song features, artist names etc. The most general emotions are considered for recommendations, happiness and saddness because all other emotions overlap with these two in terms of music and therefore would lead to incorrect predictions. Simple kmeans clustering is implemented for the recommendation based on the song features and then ranked according to the popularity. Also the number of recommendations is controllable.
- Another amazing feature is provided using spotipy, which allows the user to directly create a spotify playlist from the recommendations.
Currently all the modules are in a single .ipynb file. All 3 are currently disjoint modules but can be connected into a pipeline simply by addig 1-2 lines of code.
All the weights and data files are provided in the drive link:
https://drive.google.com/drive/folders/1cPspeYF-pNeSrrG3wpfi90X5l2BSAwmc?usp=sharing

An end to end spotify based recommendation system coming up soon! Stay tuned

<p align='center'>Made with :heart: by Bhuvan Aggarwal </p>
