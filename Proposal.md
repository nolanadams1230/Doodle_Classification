# Proposal
Computer Vision is a field of Artificial Intelligence and Computer Science that deals with how computers can be made to gain an understanding of digital images and videos. With the advances in machine learning technology, innovations in Image Processing are emerging rapidly and being leveraged by businesses all around the world. Applications of Computer Vision include:
1. Boredom killers such as your favorite [Snapchat filter](https://medium.com/@james_aka_yale/snapchats-filters-how-computer-vision-recognizes-your-face-9907d6904b91) that use facial recognition and image processing to distort your face and/or overlay images
2. Potential lifesaving uses such as [Medical startups](https://www.wired.com/2017/01/look-x-rays-moles-living-ai-coming-job/) that claim they’ll soon be able to use computers to read X-rays, MRIs, and CT scans more rapidly and accurately than radiologists.
3. And borderline unethical uses such as [Facial Recognition in police body cams](https://www.washingtonpost.com/news/the-switch/wp/2018/04/26/facial-recognition-may-be-coming-to-a-police-body-camera-near-you/?noredirect=on&utm_term=.1a5df1611adc)

With so many emerging and interesting uses of Computer Vision, my goal is to compare different machine learning algorithms from scikit-learn and Keras tasked with classifying drawings made from [Google's Quick Draw! dataset](https://quickdraw.withgoogle.com/data). By doing so I will showcase my abilities processing and analyzing the doodles through image classification and neural networks. This project is meant for companies that are interested in leveraging the Computer Vision methods used in my project in business.

## Data

Google has capitalized on the use of crowdsourcing to label over 50 million drawings with their online game "Quick Draw!". It gives its users 20 seconds to draw one of 345 different categories that range from an aircraft carrier to a zig-zag. Recently, they have [open-sourced all their data](https://console.cloud.google.com/storage/browser/quickdraw_dataset/full/numpy_bitmap?pli=1) and I will randomly select 10 images to build my classifier. Each image contains X and Y coordinates for each stroke, the time taken to draw each stroke, whether the image was recognized by Google’s classifier, a two-letter country code for where the player was from, and the label.


## Approach

My approach will begin with loading the data and performing feature engineering on the drawings in order to scale the vector drawings, filter out bad data, create new features through feature extraction, and prepare a dataset for the scikit-learn model and the neural networks. I will only use around 5000 doodles for each label, since the full dataset would be too much for my computer to handle. Then I will explore the drawings and graph random sketches of each category. Finally, I will test the dataset with Random Forest, Support-Vector Machine (SVM), K-Nearest Neighbors (KNN) and Multi-Layer Perceptron (MLP) classifiers in scikit-learn as well as a Convolutional Neural Network (CNN) in Karas.


## Deliverables
1. Code
2. Analysis Write-Up
3. Slide Deck
