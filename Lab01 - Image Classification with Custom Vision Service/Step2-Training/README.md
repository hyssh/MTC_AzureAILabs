# Train
In this step you will train, evaluate, and fine tune a custom image classification model using Custom Vision Service Web GUI. It is also possible to script the modelling workflow using Custom Vision Service SDK. Refer to the below link for more information:

https://docs.microsoft.com/en-us/azure/cognitive-services/custom-vision-service/python-tutorial



## Upload and tag training images
1. Navigate to the project section of Custom Vision Service Web GUI.

https://customvision.ai/projects

2. Click on the project you created in the lab set up step.

![Select the project](images/img4.PNG)

3. To add the first set of images to your project, use the **Add images** button. Navigate to `<MTC_AzureAILabs root/Datasets/AerialSmall/train/Barren` and select and add all images.

![Add images](images/img5.PNG)


4. To set the tag, enter *Barren* in the **My Tags** field. 

5. Repeat for images in `Cultivated` and `Developed` subfolders, using the respective tags.

## Train and evaluate the first iteration of the model
1. To train the classifier, click on the **Train** button.

![Train](images/img6.PNG)

2. After training is completed you will see the screen with the evaluation metrics. Your instructor will explain how to interpret the metrics.

![Evaluate](images/img7.PNG)


## Test your model
1. You can perform a quick test of the model on unseen data by clicking the **Quick Test** button located to the right of the **Train**. This action opens a window labeled **Quick Test**.
2. In the **Quick Test** window, click in the Submit Image field and enter the URL of the image you want to use for your test. If you want to use a locally stored image instead, click the Browse local files button and select a local image file. The testing images for our lab can be found in `<MTC_AzureAILabs root>/Datasets/AerialSmall/test`

![TQuick est](images/img8.PNG)


## Improve the model
You can apply many strategies to improve performance of your model. Your instructor will elaborate on the most common techniques. In the following steps you will apply two approaches. First you will review your training data looking for potentially mislabeled instances. Second, you will add more samples of the class for which the classifier did not perform well.

1. Browse through the images labeled as *Developed*. You will notice some images with questionable tagging.

![Mislabeled](images/img9.PNG)
![Mislabeled](images/img10.PNG)



