# Indian-currency-predictor
This is a CNN model which is trained on Indian currency notes and is capable of classifying the image fed as input as 10 ,20 ,50 ,100 ,200 ,500 ,2000 rupees note.
In this model I've used ImageDataGenerator for data augmentation, uploading dataset from drive , creating batch size and target pixel x pixel size . Do same for the test size except the data augmentation because we dont have to do changes in our validation set.
After this I made a variable called 'cnn' and imported the sequential class of keras .
afterwards I used 2 convolution layer and applied maxpooling layer at the end of second layer , then apply the flattening layer and add a dense layer with 128 neurons.
The final layer is the output laye which contains the 7 nodes that is 1 for each class of note. In the final steps we compile the model with 'adam' optimizer and 'sparse_categorical_crossentropy' loss functon because this is multi class classification problem.
This is the last step in the model where I've trained the model for 25 epochs and gained 88.6% accuracy in test set.
If someone wants to make predictions of single image then in the last cell I've created a function which takes the input image from the drive , converts them into an array. and predicted value is stored in result variable the outcome with 1 shows that the input image belongs to that particular folder and rest all folder values are 0.
