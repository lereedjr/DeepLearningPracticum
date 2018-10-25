# DeepLearningPracticum
Dog Breed Identification
Initial Preparation
	Initially, I downloaded the files that I would need for Dog Breed Identification from Kaggle.  I extracted each of the files, as they were archived.  I then placed the files in the folders from which they would soon be accessed.  With everything in place, I was able to begin the first procedure.  This section of code would take in the label of the labels.csv and read them into a python dictionary.  These were the serial numbers as keys and their corresponding names of dog breeds. The serial numbers were also the names of the pictures.  Below is an image of the python dictionary.
	


![Python Dictionary](https://github.com/lereedjr/DeepLearningPracticum/blob/master/pydict.PNG?raw=true)
      
      

  The next section of code took the name values of breeds and appended a number to the name to signify the number of times any one breed was represented.  So it was Bassett Hound – 1,2 or 29 if the name appeared that many times.  The python dictionary that was created is called the breed set.  A representation of it is below.
 
  After the breed set was created, the set could be used with the initial python dictionary to take the serial number names from the pictures, associate the breed that corresponds to the stripped serial number, then affix the breed name from the breed set to the pictures.  This resulted in pictures that were properly named and ready for further processing.  The difference in the photos is shown below.
Before
 
After
 
	
