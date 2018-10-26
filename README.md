# DeepLearningProject
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
</br> 

##Train Data Array Example

</br>
</br>

![Statistics](https://github.com/lereedjr/DeepLearningPracticum/blob/master/loaddataone.PNG?raw=true)

</br>
</br>

##Train Data Photo Example

</br>
</br>

![Statistics](https://github.com/lereedjr/DeepLearningPracticum/blob/master/loaddatatwo.PNG?raw=true)

</br>
</br>

##Test Data Photo Example

</br>
</br>

![Statistics](https://github.com/lereedjr/DeepLearningPracticum/blob/master/loadtestdata.PNG?raw=true)

</br>
</br>

The next section is where I began having issues.  At first my Anaconda installation began intermittently not recognizing that I had Keras installed in my Tensorflow environment. Then it went to not recognizing it at all.  I uninstalled Anaconda, which takes loonger than it dies to install it, then reinstalled it, hoping for something better, but no relief.  I uninstalled it again and tried to use my normally installed python3 adding jupyter notebook to it along with keras and tensorflow, but still no relief.  I changed to Google Colab, but the runtime would always time out on me, before reaching the end, not to mention what it took to learn to mount my Google drive to my Colab setup.  I then went the extra mile and tried with my AWS setup.  Same problem on the Deep learning machine and on a regular machine that I added Anaconda to, myself.  I went through about 4 of the AWS machines.

</br>
</br>

![Load Setup](https://github.com/lereedjr/DeepLearningPracticum/blob/master/setup.PNG?raw=true)

</br>
</br>

##Conclusion

</br>
</br>

After going through so much to get this going, I was extremely sad to have not been able to get this going, especially after having so many working examples, in class.  I am going to remove all installations of python from my computer and clean up my environment.  After that, I will reinstall Anaconda and try to go further with this run, until I get it to complete so that I can train the CNN. Only time constraints, not will, prevent this from happening now. 

</br>
</br>

![Load Setup](https://github.com/lereedjr/DeepLearningPracticum/blob/master/cnncode.PNG?raw=true)

</br>
</br>

To recap, I would have checked all learning rates from 0.01 to 0.0001 to learning where the best or lowest point is, or your could say the place where the validation loss does not rise or rises the latest and the least.  After that, I would apply loss, Batch normalization and other tools to get the model to the point where it does not over-fit, but it performs its best, relatively. Not overfitting is to ensure that the model can be used on datasets outside of the current dataset, upon which it was created.  This was quiet enjoyable.  Thank you.

##References
</br>
</br>
https://towardsdatascience.com/dog-breed-classification-hands-on-approach-b5e4f88c333e
</br>
</br>
https://towardsdatascience.com/image-classification-python-keras-tutorial-kaggle-challenge-45a6332a58b8
