Steps to clean the data:

1. Read train data from the "./train" folder and store them in appropraiate data frames.

2. Read test data from the "./test" folder and store them in appropraiate data frames.

3. Concatenate testData to trainData to generate a 10299x561 data frame, joinData; concatenate testLabel to trainLabel to generate a 10299x1 data frame, joinLabel; concatenate testSubject to trainSubject to generate a 10299x1 data frame, joinSubject.

4. Read the features.txt file from the "./" folder and store the data in a variable called features. We only extract the measurements on the mean and standard deviation. We get a subset of joinData with the corresponding columns.

5. Clean the column names of the subset.

6. Read the activity_labels.txt file from the "./"" folder and store the data in a variable called activity.

7. Clean the activity names in the second column of activity. We first make all names to lower cases. If the name has an underscore between letters, we remove the underscore and capitalize the letter immediately after the underscore.

8. Transform the values of joinLabel according to the activity data frame.

9. Combine the joinSubject, joinLabel and joinData by column to get a new cleaned 10299x68 data frame, cleanedData. Properly name the first two columns, "subject" and "activity".

10. Write the cleanedData out to "merged_data.txt" file in current working directory.

11. Finally, generate a second independent tidy data set with the average of each measurement for each activity and each subject. We have 30 unique subjects and 6 unique activities, which result in a 180 combinations of the two. Then, for each combination, we calculate the mean of each measurement with the corresponding combination. So, after initializing the result data frame and performing the two for-loops, we get a 180x68 data frame.

12. Write the result out to "tidy_dataset_with_means.txt" file in current working directory.