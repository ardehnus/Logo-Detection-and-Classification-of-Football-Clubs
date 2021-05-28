# Football Club Logo Detection and Classification

## Dataset:
The dataset consists of a total of 300 images. 50 images per class.
The classes are:

1. Barcelona
2. Real Madrid
3. Manchester United
4. Borussia Dortmund
5. Inter Milan
6. Chelsea

Images souce: Google

## Data processing:
The model takes image of a fixed dimension. The image_Preprocessing.py file resizes each image to 224X224 dimensions. It converts the dataset to a numpy array and saves it in data.npy file. It also generates a labels.npy file consisting of target labels for each image in the dataset.

## Model:
The model makes use of the MobileNet_v2 architecture trained on the ImageNet dataset. The MobileNet_v2 model is smaller compared to other models. This helps in ease of training and the model can be used in android applications due to its relatively smaller size. The Dense layer of the model is replaced by our custom dense layer to classify 6 classes. The classifierLogo.ipynb generates a model.h5 file which cotains the trained model.


## Prediction:
The prediction.py file takes in images of club logos as input, resizes it to 224X224 to feed it to the trained model and outputs the target logo present in the image. The extra_images folder consists of some additional images for testing the model. 
