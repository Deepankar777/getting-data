{\rtf1\ansi\ansicpg1252\cocoartf1265\cocoasubrtf210
{\fonttbl\f0\fnil\fcharset0 HelveticaNeue;\f1\fnil\fcharset0 Consolas;}
{\colortbl;\red255\green255\blue255;\red38\green38\blue38;\red255\green255\blue255;\red245\green245\blue245;
\red52\green110\blue183;}
\paperw11900\paperh16840\margl1440\margr1440\vieww10800\viewh8400\viewkind0
\deftab720
\pard\pardeftab720\sl500\sa320

\f0\fs32 \cf2 \cb3 The original dataset included the following data files:\
\pard\pardeftab720\sl400

\f1\fs28 \cf2 \cb4 'features.txt': List of all features.\
\
'activity_labels.txt': List of class labels and their activity name.\
\
'train/X_train.txt': Training set.\
\
'train/y_train.txt': Training labels.\
\
'train/subject_train.txt': ID's of subjects in the training data\
\
'test/X_test.txt': Test set.\
\
'test/y_test.txt': Test labels.\
\
'test/subject_test.txt': ID's of subjects in the training data\
\pard\pardeftab720\sl500\sa320

\f0\fs32 \cf2 \cb3 For more information about the "Human Activity Recognition Using Smartphones Dataset Version 1.0" contact:\'a0{\field{\*\fldinst{HYPERLINK "mailto:activityrecognition@smartlab.ws"}}{\fldrslt \cf5 activityrecognition@smartlab.ws}}\'a0A brief description of the script:\
The run_analysis.R script merges data from a number of .txt files and produces a tidy data set which may be used for further analysis.\
\pard\pardeftab720\sl400

\f1\fs28 \cf2 \cb4 First it checks to see if the required "reshape2" has been installed and then loads the "reshape2" package.\
\
It then reads all required .txt files and labels the datasets\
\
Consquently the appropriate "activity_id"'s and "subject_id"'s are appended to the "test" and the "training" data, which are then combined into one single data frame\
\
Using the "grep" function, all the columns with mean() and std() values are extracted and then a new data frame, including only the "activity_id", the "subject_id" and the mean() and std() columns, is created\
\
Using the "merge" function, descriptive activity names are merged with the mean/std values dataset, to get one dataset with descriptive activity names\
\
Lastly, with the help of the "melt" and "dcast" functions of the "reshape2" package, the data is converted into a table containing mean values of all the included features, ordered by the activity name and the subject id, and the data is written to the "tidy_movement_data.txt" file.\
}