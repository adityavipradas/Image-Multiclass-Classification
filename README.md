# Image Multiclass Classification using Ensemble (ResNet50 + InceptionV3 + EffNetB7)

<b>Dataset used:</b> [Intel Image Classification](https://www.kaggle.com/datasets/puneet6060/intel-image-classification) </br>
This data contains natural scene images classified under 6 categories ['buildings', 'forest', 'glacier', 'mountain', 'sea', 'street'] </br>
<b>Training size:</b> 14000 </br>
<b>Testing size:</b> 3000 </br>

## Synopsis
1. <b>ResNet50</b> - Data augmentation, batchnormalization, dropout with 0.3 rate, learning_rate = 0.0001 (Adam)
2. <b>InceptionV3</b> - Data augmentation, batchnormalization, dropout with 0.3 rate, learning_rate = 0.0001 (RMSprop)
3. <b>EfficientNetB7</b> - Data augmentation, GlobalAveragePoolong2D, batchnormalization, dropout with 0.3 rate, learning_rate = 0.0001 (Adam)
4. <b>Ensemble Model</b> - Test classification accuracy: <b>0.9297</b></br>

It is observed that the ensemble of the three CNN architectures mentioned above performs better than each individual architecture. The Jupyter notebook provides step-by-step implementation of the classification pipeline right from importing the libraries to assessing the ensemble model's performance on the test dataset.</br>

<b>Loss function used:</b> Categorical cross-entropy</br>
<b>Performance metrics used:</b> Accuracy, precision, recall and f1-score</br>
<b>Optimization algorithms used:</b> Adam performed well for the ResNet50 and EfficientNetB7 architectures whereas RMSprop performed better on InceptionV3</br>

The notebook can also be implemented on Kaggle [here](https://www.kaggle.com/code/adityavipradas/ensemble-93-acc-resnet50-inceptionv3-effnetb7).</br>

I have used <b>TensorFlow 2.10.1</b> to enable GPU acceleration on my windows machine.</br>

Here are a few inferences of the ensemble model on the test data along with the confusion matrix.</br>

![download](https://user-images.githubusercontent.com/3115883/229651169-5eab629c-c0c8-434c-b13b-7a3a023bd034.png)</br>
![download](https://user-images.githubusercontent.com/3115883/229651058-8c7a9daf-f4e1-4029-9687-d2170500f505.png)</br>
![download](https://user-images.githubusercontent.com/3115883/229651075-d8c1ffca-abac-49a8-9c2f-c29038d93535.png)</br>
![download](https://user-images.githubusercontent.com/3115883/229651099-faf9dbdf-7e2d-4aea-949c-f307a965403e.png)</br>
![download](https://user-images.githubusercontent.com/3115883/229651103-15805114-6a80-4de4-a300-07276af0da6f.png)</br>
![download](https://user-images.githubusercontent.com/3115883/229651115-f8f18864-e582-4e01-8380-80441307044f.png)</br>
![download](https://user-images.githubusercontent.com/3115883/229651119-b2cfbec8-b87a-4a4e-86c8-ab1bb661eb8c.png)

