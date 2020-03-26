# INTRODUCTION
Skin cancer is the most prevalent in humans amongst all other cancer types. One of the main
reasons for skin cancer is the exposure to harmful Ultra-Violet rays from the sun. Moreover,
according to the Government of Canada’s website, about one-third of all the new cases of cancer
in Canada are skin cancers and the trend is on the rise. Over 80,000 cases of skin cancer are
diagnosed in Canada each year, more than 5,000 of which are melanoma, the deadliest form
of skin cancer. Therefore, it is necessary to detect skin cancer so that it can be treated on time
and does not spread or become fatal.
In this project, we are working with cancer cells present in the skin. The main aim of the project
is to classify skin lesions from images into 7 different categories of skin lesion namely:
1. Melanocytic nevi
2. Melanoma
3. Benign keratosis-like lesions
4. Basal cell carcinoma
5. Actinic keratoses
6. Vascular lesions
7. Dermatofibroma
This project uses Convolutional Neural Networks to classify skin lesions into the various
categories of skin cancer. Firstly, the images are segmented so that only the significant parts of
the image are left. It is then passed through the model which classifies the image accordingly.
We have actually passed both segmented as well as unsegmented images and compared the
performance of the model in both the cases. Furthermore, we have used the segmented images
as the input for ResNet50 and compared its performance with that of CNN.

# OVERVIEW
![](model%20diag.jpg)
As you can see in the above figure,the original and the segmented images are passed
separately through the Convolutional Neural Network. The CNN consists of a convolutional layer
followed by a pooling layer, a dropout layer (to prevent overfitting) and finally a fully connected
layer.
The segmented images were also fed in as the input for the ResNet50 model. The ResNet50
model consists of ResNet block followed by a series of convolutional
blocks which have the same layers as mentioned above.
Both models classify the images into the different classes of cancer types
