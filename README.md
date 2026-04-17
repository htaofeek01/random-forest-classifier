# Predicting Students' Academic Performance Using Behavioural Dataset

## Objectives of The Project
   The objectives of this project work are as follows:
   1. Predict Student Academic Performance based on some behavior data of the student
   2. Find out behavior that affect student academic performance the most
   3. Evaluate the machine learning prediction used for accuracy and precision

## Project Overview
In this project the machine learning algorithm used for predicting student academic performance from behavioral dataset is *Random Forest Classifier* which involves leveraging the power of ensemble learning and decision trees. Random Forest is an ensemble of decision trees, where each tree is constructed using a random subset of features and a random subset of the training data. The predictions from multiple trees are then aggregated to make a final prediction.


## Dataset Preparation:
   - Features: The behavioral dataset contains features related to student behavior. These include attributes like attendance scores, study habits, hobbies, family issues, ...
   - Target Variable: The target variable is the student academic performance (student grades)
    
   The figure below shows the entire features in our dataset. 
   
   ![Figure 1: Raw dataset](https://github.com/htaofeek01/random-forest-classifier/blob/main/img/raw_data.JPG)
   
## Data Preprocessing:
   - Handling missing values, if any.
   - Converting categorical variables into a suitable format (e.g., one-hot encoding).
   - Spliting the dataset into training and testing sets.
   
     ![Figure 2: Data preparation for model prediction](https://github.com/htaofeek01/random-forest-classifier/blob/main/img/data_preprocess.JPG)
     
   The figure above depicts the raw dataset as collected from our survey.

### Making meaning from the dataset

   ![Figure 3: Bar graph of CGPA to by student numbers](https://github.com/htaofeek01/random-forest-classifier/blob/main/img/bargraph_cgpa.JPG) 
   
   ![Figure 4: Pie chart of student grade distribution](https://github.com/htaofeek01/random-forest-classifier/blob/main/img/pie_chart_stud.JPG) 

In the above figure, we can deduce that 46.1% of students in the dataset are very good academically, 34% are Good, 18.4% are Fair, and the weak and poor students are negligible.

 
   ![Figure 5: Correlation of student performance](https://github.com/htaofeek01/random-forest-classifier/blob/main/img/corr_stud.JPG)

The correlation heat map above shows the behavior that affect student positively the most are Study habit, Class attendance & Family issues. Financial stability moderately affects students performance while habits that affect students negatively are Accommodation distance from school, Distractions (hobbies or addiction), and Impact of extracurricular activities.
 
![Figure 0.6Score map of students with grade](https://github.com/htaofeek01/random-forest-classifier/blob/main/img/score_map.JPG)
  
![Figure 0.7Study habit of students](https://github.com/htaofeek01/random-forest-classifier/blob/main/img/study_habit.JPG)

We can conclude from the graph above that very good student study hard with their percentage being the highest as 80%
 
![Figure 0.8Performance by class attendance](https://github.com/htaofeek01/random-forest-classifier/blob/main/img/attendance.JPG)

The figure above shows that top students attend class regularly
 
![Figure 0.9family issues](https://github.com/htaofeek01/random-forest-classifier/blob/main/img/fam_issues.JPG)

Family issues affect all students. A stable home impact students psychology and concentration in school.
 
![Figure 0.10financial stability](https://github.com/htaofeek01/random-forest-classifier/blob/main/img/Finance.JPG)

From the above figure, financial stability moderately affects students performance
 
![Figure 0.11accommodation issues](https://github.com/htaofeek01/random-forest-classifier/blob/main/img/accomm.JPG)

Accommodation issues affect students negatively the most, students that stay on campus do perform better than those that live outside the school campus.

 
![Figure 0.12Impact of distractions on students](https://github.com/htaofeek01/random-forest-classifier/blob/main/img/perf_distract.JPG)

Addictions or engagement with hobbies affect students the most after accommodation issues

### Building the Random Forest Model:
   - Import the `RandomForestClassifier` from scikit-learn.
   - Create an instance of the classifier.
   - Train the model using the training dataset.

 
![Figure 0.13import libraries](https://github.com/htaofeek01/random-forest-classifier/blob/main/img/libs.JPG)

 
![Figure 0.14model trained](https://github.com/htaofeek01/random-forest-classifier/blob/main/img/train_model.JPG)

### Save the model
- From the figure below, we saved the trained model so that we can use it in a webapp without retraining the model every time we need it.
 
![Figure 0.15save the model](https://github.com/htaofeek01/random-forest-classifier/blob/main/img/save_load_mod.JPG)

### Testing the model
- For first candidate
- For second canditat
- For third candidate
 
-[Figure 0.16student1 result](https://github.com/htaofeek01/random-forest-classifier/blob/main/img/stud1_result.JPG)
 
![Figure 0.17student 2 result](https://github.com/htaofeek01/random-forest-classifier/blob/main/img/stud2_result.JPG)
 
![Figure 0.18student 3 result](https://github.com/htaofeek01/random-forest-classifier/blob/main/img/stud3_result.JPG)

### Model Evaluation:
   - We evaluate the model using metrics such as accuracy, precision, recall, F1-score an confusion matrix

 
![Figure 0.19model accuracy](https://github.com/htaofeek01/random-forest-classifier/blob/main/img/accuracy.JPG)

The model accuracy is 82.8%
 
![Figure 0.20Model evaluation metrics](https://github.com/htaofeek01/random-forest-classifier/blob/main/img/class_report.JPG)
 
![Figure 0.21confusion matrix](https://github.com/htaofeek01/random-forest-classifier/blob/main/img/conf_matr.JPG)

### Tuning Hyperparameters
We can further experiment with hyperparameter tuning to optimize the model's performance. Parameters like `n_estimators`, `max_depth`, and others can be fine-tuned.

## Conclusion
Random Forest classifiers are robust, handle non-linear relationships well and are less prone to overfitting compared to individual decision trees. They are suitable for classification tasks, especially when dealing with complex datasets with multiple features. However, it's essential to interpret the results carefully and consider the context of the specific educational scenario. In this project, we conclude that habits that affect students academic performance positively are Study habit, Family support, Class attendance. Students' financial stability moderately impacts students performance. Some negative habits that affect student academic performance the most are Accommodation (nearness to school), distractions and impact of extracurricular activities. The use of machine learning(AI) in this project is to predict student academic potential by given behavior metrics such as study habit, Class attendance and other metrics used for our model training.

