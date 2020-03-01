# epilepsy_siezure_prediction

we used MIT CHB dataset for this project.

  1) Initially we applied random forest classifier after converting the EDF dataset to CSV. 
    This had problems because the dataset is heavily biased and only 1/80 of a dataset contibutes to siezure class.
    Amplitude information was not alone going to give any satisfactoy results eventhough we could see bump in the graph if plot the data.
    (we had 3 classes i) non siezure - ii) 4 minutes before siezure - iii) During siezure
  
  2) We also tried to use outlier detection method since the siezure part only contibuted very less to the data set.
    It did not work because amplitude information doesnt contibute any information to classifyi the data.
    
  3) We also tried using SMOTE to oversample the undersampled classes, which improved our F1 score but it was still not satisfactory.
  
  4) We took a different approach by applying CNN. We used screenshots of EEG plot - we assumed the frequency information can be found from the amplitude
     data by the closer edges if we plot the EEG data.
     
     i) We took same sampling frequency for all the classes and our F! score was still an improvement than previous cases.
     ii) We reduced the rate at which screenshots were taken for non-siezure than other two classes (4-min before siezure and during siezure) and
         highest frequency for during the siezure to balance the dataset to some extend.
     iii) In above two methods we used both our own CNN method and Transfer learning method with Resnet Backbone model(our own classifier layer)
          Resnet - gave better results.
     iv) We also tried 2- class classifire for detection- During siezure and non siezure. Which gave really satisfactory results.
   5) We build our own resnet network to train our dataset on it which gave us best results training accuracy-86% testing accuracy - 85.5%
   
   for dataset and questions mail me felixpv007@gmail.com
