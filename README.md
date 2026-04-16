# PREDICTING STUDENTS' ACADEMIC PERFORMANCE USING BEHAVIORAL DATASET

## The objectives of this project work are as follows:
1. Predict Student Academic Performance based on some behavior data of the student
2.	Find out behavior that affect student academic performance the most
3.	Evaluate the machine learning prediction used for accuracy and precision

In this project the machine learning algorithm used for predicting student academic performance form behavioral dataset is Random Forest classifier which involves leveraging the power of ensemble learning and decision trees. Random Forest is an ensemble of decision trees, where each tree is constructed using a random subset of features and a random subset of the training data. The predictions from multiple trees are then aggregated to make a final prediction.


1.	Dataset Preparation:
   - Features: The behavioral dataset contains features related to student behavior. These include attributes like attendance scores, study habits, hobbies, family issues.
   - Target Variable: The target variable is the student academic performance (student grades)
The figure below shows the entire features in our dataset.  
Figure 0.1Raw dataset
2.	 Data Preprocessing:
   - Handle missing values, if any.
   - Convert categorical variables into a suitable format (e.g., one-hot encoding).
   - Split the dataset into training and testing sets.
- The column labels from the dataset were renamed

 
Figure 0.2Data preparation for model prediction
The figure above depicts the raw dataset as collected from our survey

3.	Making meaning from the dataset
 
Figure 0.3Bar graph of CGPA to by student numbers

 
Figure 0.4Pie chart of student grade distribution

In the above figure, we can deduce that 46.1% of student in the dataset are very good academically, 34% are Good, 18.4% are Fair, and the weak and poor students are negligible.


 
Figure 0.5: Correlation of student performance

The correlation heat map above shows behavior that affect student positively the most are Study habit, Family issues, Attendance and Financial stability while habits that affect students negatively are Accommodation (distance from school), Distractions (hobbies or addiction), and Impact of extracurricular activities.
 
Figure 0.6Score map of students with grade
  
Figure 0.7Study habit of students

We can conclude from the graph above that very good student study hard with their percentage being the highest as 80%
 
Figure 0.8Performance by class attendance
The figure above shows that top students attend class regularly
 
Figure 0.9family issues
Family issues affect all students. A stable home impact students psychology and concentration in school.
 
Figure 0.10financial stability
From the above figure, financial stability moderately affects students performance
 
Figure 0.11accommodation issues

Accommodation issues affect students negatively the most, students that stay on campus do perform better than those that live outside the school campus.

 
Figure 0.12Impact of distractions on students
Addictions or engagement with hobbies affect students the most after accommodation issues

4.	Building the Random Forest Model:
   - Import the `RandomForestClassifier` from scikit-learn.
   - Create an instance of the classifier.
   - Train the model using the training dataset.

 
Figure 0.13import libraries


 
Figure 0.14model trained
5.	Save the model
- From the figure below, we saved the trained model so that we can use it in a webapp without retraining the model every time we need it.
 
Figure 0.15save the model

6.	Testing the model
-	For first candidate
-	For second canditat
-	For third candidate
 
Figure 0.16student1 result
 
Figure 0.17student 2 result
 
Figure 0.18student 3 result
7.	Model Evaluation:
   - We evaluate the model using metrics such as accuracy, precision, recall, F1-score an confusion matrix

 
Figure 0.19model accuracy
The model accuracy is 82.8%
 
Figure 0.20Model evaluation metrics
 
Figure 0.21confusion matrix
8.	Tuning Hyperparameters:
We can further experiment with hyperparameter tuning to optimize the model's performance. Parameters like `n_estimators`, `max_depth`, and others can be fine-tuned.

CONCLUSION
Random Forest classifiers are robust, handle non-linear relationships well and are less prone to overfitting compared to individual decision trees. They are suitable for classification tasks, especially when dealing with complex datasets with multiple features. However, it's essential to interpret the results carefully and consider the context of the specific educational scenario. In this project, we conclude that habits that affect students academic performance positively are Study habit, Family support, Class attendance. Student financial stability moderately impacts students performance. Some negative habits that affect student academic performance the most are Accommodation(nearness to school), distractions and impact of extracurricular activities. The use of machine learning(AI) in this project is to predict student academic potential by given behavior metrics such as study habit, Class attendance and other metrics used for our model training.

