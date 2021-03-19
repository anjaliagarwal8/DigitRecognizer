The dataset contains 28*28 pixel values for images of 0-9 digits. 


![image](https://user-images.githubusercontent.com/30053985/111805566-27be1380-88f7-11eb-926e-d2611eae3b77.png)

For preprocessing the images, I normalized them using formula:

Im = (Im - max(Im))/(max(Im) - min(Im))

I have used three methods for data augmentation:

Image Binarization - Converting the grayscale images to black and white,i.e having two values 0 and 1

![image](https://user-images.githubusercontent.com/30053985/111806103-a7e47900-88f7-11eb-886a-747f0bae69e4.png)


Image Rotation - Rotating the images by 20 degrees clockwise and anticlockwise

![image](https://user-images.githubusercontent.com/30053985/111806220-c64a7480-88f7-11eb-8c5e-c52938a1c802.png)


Image translation - Translating the images in the four orthogonal directions by 5 units.

![image](https://user-images.githubusercontent.com/30053985/111806240-ccd8ec00-88f7-11eb-94f6-629901f2c494.png)

Model


A CNN model has been trained to classify the test images. The CNN model is as follows: 

Conv2D2 --> MaxPooling2D --> Dropout --> Conv2D2 --> MaxPooling2D --> Flatten --> Dense --> Dropout --> Dense (output)

The model was optimized using NAdam optimizer and loss was calculated using KL_divergence function. 

NAdam optimizer - https://ruder.io/optimizing-gradient-descent/index.html#nadam
KL_divergence loss function - https://en.wikipedia.org/wiki/Kullback%E2%80%93Leibler_divergence

The kaggle notebook can be found here: https://www.kaggle.com/anjalia8/digitrecognizer-top-13

Thank you!
