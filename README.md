The run_analysis.R will generate a tidy_data for the project in Getting and Cleaning Data class.

First, a project folder was created to store the extracted file downloaded 
from the https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip 

The run_analysis.R script need to be stored in the project folder also.

In order to run the script in R, please set up this project folder as the current working directory in R.
Then copy the script file and paste it to the console window, and click "Enter", you will get the tidy_data.txt automatically.
The script running with take 2-3 seconds.

In the script, first a couple R packages which were used are installed.

Then the file downloaded were read into R sequencially. Only those file related to the project were read.
A test data set and a train data set were generated by merging the files in the test folder and the files in the train folder, respectively.
The complete data set was generated by stacking the test data set and train data set.

Also, a proper column namew were labled in the complete data set.

After generating the complete data, based on the labled column features, we extracted the mean() and std() columns only. And this is an
original tidy data set.

A descriptive activity label and descriptive column names were used accordingly in the tidy data.

In order to get the average of mean() and std() column features. the tidydata was reshaped into a long data format using melt() function. 
The averages per feature columns were calculated for each Suject and each activities. Then using dcast() function, the averages per 
features calculated were laid out together with Suject and activity. It was the final_tidy_data. 

Finally, the final tidy data was written into the tidy_data.txt file.


