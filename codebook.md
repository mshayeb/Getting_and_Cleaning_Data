Code Book
=========================

### 1. Processing data

This is a description of the [run_analysis.R][analysis]-script

1. `activity_labels.txt` and `features.txt`is loaded
2. `X_test.txt`, `y_test.txt` and `subject_test.txt` is loaded. respectively with train.
3. subject_test/train describes the IDs, y_test/train the activity labels and x_test/train the features.
4. appending the three train files
5. appending the three test files
6. appending the whole train and test file to get the merged test file
7. ordering via the ID column
7. labeling the activity column with the labels of `activity_labels.txt`
8. extracting all columns with `"mean"` and `"std"` via the `grep` function and
making first tidy data set [tidy_dataset1.txt][tidy1].
10. with help of the `plyr`-package calculating means for each ID and activity for 
all the columns.
11. adding `_mean` at the end of every column-name
11. result is the second tidy dataset [tidy_dataset2.txt][tidy2]

### 2. dataset description

[tidy_dataset1.txt][tidy1] is of dimension `10299x81` with `;`-seperation, `.`-decimals, header and no row.names
and [tidy_dataset2.txt][tidy2] is of dimension `180x81` with `;`-seperation, `.`-decimals, header and no row.names.
The second one has a mean of all the columns for every *ID* and *activity* combination.

The variables are as follows ([tidy_dataset2.txt][tidy2] has an `_mean` appended to every columname)
- "ID"                              
- "activity"                                                      
- "tBodyAcc.std...X"                                        
- "tBodyAcc.std...Y"                               
- "tBodyAcc.std...Z"                                              
- "tGravityAcc.std...X"                              
- "tGravityAcc.std...Y"                                           
- "tGravityAcc.std...Z"                                           
- "tBodyAccJerk.std...X"                              
- "tBodyAccJerk.std...Y"                                          
- "tBodyAccJerk.std...Z"                                          
- "tBodyGyro.std...X"  
-  "tBodyGyro.std...Y"                                             
- "tBodyGyro.std...Z"                                             
- "tBodyGyroJerk.std...X"          
-   "tBodyGyroJerk.std...Y"                                         
- "tBodyGyroJerk.std...Z"                                         
- "tBodyAccMag.std.."              
-   "tGravityAccMag.std.."                                          
- "tBodyAccJerkMag.std.."                                         
- "tBodyGyroMag.std.."             
-   "tBodyGyroJerkMag.std.."                                        
- "fBodyAcc.std...X"                                              
- "fBodyAcc.std...Y"               
-   "fBodyAcc.std...Z"                                              
- "fBodyAccJerk.std...X"                                          
- "fBodyAccJerk.std...Y"           
-  "fBodyAccJerk.std...Z"                                          
- "fBodyGyro.std...X"                                             
- "fBodyGyro.std...Y"              
-   "fBodyGyro.std...Z"                                            
-  "fBodyAccMag.std.."                                             
- "fBodyBodyAccJerkMag.std.."      
-   "fBodyBodyGyroMag.std.."                                       
-  "fBodyBodyGyroJerkMag.std.."                                   
-  "tBodyAcc.mean...X"              
-   "tBodyAcc.mean...Y"                                            
-  "tBodyAcc.mean...Z"                                             
- "tGravityAcc.mean...X"           
-   "tGravityAcc.mean...Y"                                         
-  "tGravityAcc.mean...Z"                                          
- "tBodyAccJerk.mean...X"          
-   "tBodyAccJerk.mean...Y"                                        
-  "tBodyAccJerk.mean...Z"                                        
-  "tBodyGyro.mean...X"             
-  "tBodyGyro.mean...Y"                                           
-  "tBodyGyro.mean...Z"                                            
- "tBodyGyroJerk.mean...X"         
-   "tBodyGyroJerk.mean...Y"                                       
-  "tBodyGyroJerk.mean...Z"                                        
- "tBodyAccMag.mean.."             
-   "tGravityAccMag.mean.."                                         
- "tBodyAccJerkMag.mean.."                                        
- "tBodyGyroMag.mean.."            
-   "tBodyGyroJerkMag.mean.."                                      
-  "fBodyAcc.mean...X"                                             
- "fBodyAcc.mean...Y"              
-   "fBodyAcc.mean...Z"                                            
-  "fBodyAcc.meanFreq...X"                                        
-  "fBodyAcc.meanFreq...Y"          
-   "fBodyAcc.meanFreq...Z"                                        
-  "fBodyAccJerk.mean...X"                                         
- "fBodyAccJerk.mean...Y"          
-   "fBodyAccJerk.mean...Z"                                        
-  "fBodyAccJerk.meanFreq...X"                                     
- "fBodyAccJerk.meanFreq...Y"      
-   "fBodyAccJerk.meanFreq...Z"                                    
-  "fBodyGyro.mean...X"                                            
- "fBodyGyro.mean...Y"             
-   "fBodyGyro.mean...Z"                                           
-  "fBodyGyro.meanFreq...X"                                        
- "fBodyGyro.meanFreq...Y"         
-   "fBodyGyro.meanFreq...Z"                                       
-  "fBodyAccMag.mean.."                                            
- "fBodyAccMag.meanFreq.."         
-   "fBodyBodyAccJerkMag.mean.."                                   
-  "fBodyBodyAccJerkMag.meanFreq.."                                
- "fBodyBodyGyroMag.mean.."        
-   "fBodyBodyGyroMag.meanFreq.."                                  
-  "fBodyBodyGyroJerkMag.mean.."                                   
- "fBodyBodyGyroJerkMag.meanFreq.."




[analysis]: https://github.com/Schlusie/GettingAndCleaningData/blob/master/run_analysis.R
[tidy1]: https://github.com/Schlusie/GettingAndCleaningData/blob/master/tidy_dataset1.txt
[tidy2]: https://github.com/Schlusie/GettingAndCleaningData/blob/master/tidy_dataset2.txt
