# DeepLearningPracticum
Dog Breed Identification
Initial Preparation
	Initially, I downloaded the files that I would need for Dog Breed Identification from Kaggle.  I extracted each of the files, as they were archived.  I then placed the files in the folders from which they would soon be accessed.  With everything in place, I was able to begin the first procedure.  This section of code would take in the label of the labels.csv and read them into a python dictionary.  These were the serial numbers as keys and their corresponding names of dog breeds. The serial numbers were also the names of the pictures.  Below is an image of the python dictionary.
	
</br>

![Python Dictionary](https://github.com/lereedjr/DeepLearningPracticum/blob/master/pydict.PNG?raw=true)
      
</br>      

The next section of code took the name values of breeds and appended a number to the name to signify the number of times any one breed was represented.  So it was Bassett Hound – 1,2 or 29 if the name appeared that many times.  The python dictionary that was created is called the breed set.  A representation of it is below.

</br>
  
![Python Dictionary](https://github.com/lereedjr/DeepLearningPracticum/blob/master/breedset.png?raw=true) 

</br>

After the breed set was created, the set could be used with the initial python dictionary to take the serial number names from the pictures, associate the breed that corresponds to the stripped serial number, then affix the breed name from the breed set to the pictures.  This resulted in pictures that were properly named and ready for further processing.  The difference in the photos is shown below.

## Before
![Before Assembly](https://github.com/lereedjr/DeepLearningPracticum/blob/master/beforepic.PNG?raw=true)
</br>
## After
![After Assembly](https://github.com/lereedjr/DeepLearningPracticum/blob/master/afterpic.PNG?raw=true)

</br>
With the pictures being properly labeled and numbered, we needed to one hot encode the values for each breed as classes.  So I One hot encoded 115 classes, one for each breed of dog included in this challenge.  This one hot encoding is what assists the CNN in categorizing the dog breeds.  There is a brief example, shown below.

</br> 

![One Hot Encoding](https://github.com/lereedjr/DeepLearningPracticum/blob/master/onehot.PNG?raw=true)

</br> 

Next, we have over 10,000 photos and they are all of differing sizes. We cannot feed the photos to the CNN with those differences, because all of the photos must be of the same dimensions.  So we added a function that allows us to examine the size statistics of the photos.  From reading the information, we can decide the best size to load the photos to the CNN.  Below is a sample of the size statistics.

</br>
![Statistics](https://github.com/lereedjr/DeepLearningPracticum/blob/master/statistics.PNG?raw=true)
</br>

After the statistics we need to actually change the size of the photos, so we use a function that does that and more.  It also reduces the color spectrum to grey scale, which will help our model to train a bit faster.  With all of the photos for training prepared, we also have to do the same for the test data, because they are being evaluated by the same CNN, at the same time. Below are one example of the data formations that make up the photos and two examples of the photos that made it into train and test data loads.

</br> 
##Train Data Array Example
![Statistics](https://github.com/lereedjr/DeepLearningPracticum/blob/master/loaddataone.PNG?raw=true)
</br>

##Train Data Photo Example
</br>
![Statistics](https://github.com/lereedjr/DeepLearningPracticum/blob/master/loaddatatwo.PNG?raw=true)

</br>
##Test Data Photo Example
</br>
![Statistics](https://github.com/lereedjr/DeepLearningPracticum/blob/master/loadtestdata.PNG?raw=true)


