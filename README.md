# dog_breeds
  This is a Colab notebook for transfer learning for classification of 120 dog breeds by using Keras. By adding the flat layers on the top of frozen InceptionV3, we construct a CNN neural network.

The structure of the network is:
 Frozen InceptionV3 + Dense(1204, relu) + Dropout(0.5) + Dense(120, softmax).

I use 80% for training, 10% for validation and 10% for test. I find that by adding dropout(0.5), the accuracy can be improved from 0.68 to 0.71 for image sizebeing 200. And it seems that regularizaiton almost has no help. But the  the image size has a significant effect on the accuracy. By using image size 400, I can get the log loss about 0.28 and accuracy above 0.91 on the test data.



Content:
1. Stratified split the images into train and test.
   -- 1.1 Train and test images data
   -- 1.2 Explore data
2. ImageDataGenerator
   -- 2.1 Output of the generator
   -- 2.2 Data generators (train, validation, test)
3. Construct model
   -- 3.1 One Cycle Policy
   -- 3.2 Train and test
