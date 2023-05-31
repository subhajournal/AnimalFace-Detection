# AnimalFace-Detection
Transfer Learning model to detect (classify) Animal Face
The classification of wild animals has been done with the implication of a deep learning model. Primarily, the number of image files in the database has been in both the train segment and validation segment.  
The numerical counts and the visualization to show the file distribution in train and valid data segments have been shown above. It can be seen from the distribution that the database is imbalanced as the number of files is not equal for all classes.    
Now, to classify the images, image augmentation has been done by rescaling the images by a factor of 1/255 so that the images will be normalized and prohibits overfitting. Additionally, the 50° image rotation has been applied with height & width shifting by 15% and zoom range by 30%. After preparing the train and validation augmented database. 
Next, the VGG Network has been prepared to classify the images. The reasons behind the use of VGG Network (VGG19) are discussed below:
	VGG19 has been built on convolutional layers using a small kernel size of 3x3 and are followed by max-pooling layers of 2x2. This simple yet effective structure has allowed VGG19 to achieve state of the art results in various image classification benchmarks. So, one of the advantages of VGG19 is its high accuracy. 
	VGG19 has been able to achieve higher classification accuracies than previous CNN architectures such as AlexNet and GoogLeNet. This high accuracy is due to the deep structure of VGG19, which allows the network to learn more complex and abstract features from the input images. 
	VGG19 has good features such as modularity and transferability. VGG19 can be used as a feature extractor where the convolutional layers are used to extract features from the input images, and then fed into a different classifier. 
	VGG19 can be fine-tuned on smaller datasets by freezing the first few layers and training the last layers on the target task. This transfer learning approach has proven to be effective in cases where there is limited training data. 
	VGG19 has been shown to have better generalization capability than other CNN models. Generalization refers to the ability of a model to perform well on new and unseen data, and VGG19 achieves this by having a more stable hyperparameter optimization process during training.
So, the VGG19 Model has been prepared and the model outcome has been shown below with the operational flow of the model to classify the images:
       
So, the model contains 20159639 total parameters where 20158103 are non-trainable and the rest 1536 are trainable. After compiling and training the model, the outcomes have been achieved by visualizing the loss & accuracy graphs for training and the confusion matrix for validation which are shown below:
   
Finally, to observe the accuracy of training and validation separately., the model has been evaluated. It has been observed that the training accuracy & loss values are 97.5% & 0.06. On the other hand, the validation accuracy & loss values are 97.8% & 0.07. So, the overfitting is very and so, it can be said that the model is performing well to classify animal images.
 

