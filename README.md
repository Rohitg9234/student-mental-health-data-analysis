

# Student Mental Health Data Analysis

This project is focused on analyzing the effects of mental health on students' academic performance, particularly their CGPA. Using data collected from a survey, the goal is to explore the relationship between mental health issues (like anxiety, depression, panic attacks) and academic performance, as well as other factors like attendance and satisfaction with the branch/career path.

### **Dataset**
The dataset contains responses to a survey about students' mental health and their academic status. It includes the following key features:
- **Gender**
- **Course of Study**
- **CGPA**
- **Satisfaction with chosen branch**
- **Attendance and associated stress**
- **Mental health factors**: Anxiety, Depression, Panic attacks, etc.
- **Whether the student sought professional treatment**

### **Objective**
The goal of this project is to:
1. Perform statistical analysis to find correlations between mental health and CGPA.
2. Visualize the distribution of responses for different factors like gender, depression, anxiety, and more.
3. Build predictive models to identify whether a student is likely to experience depression based on their responses.

---

### **Steps and Analysis**

1. **Data Cleaning**:
   - First, the data is read from a CSV file.
   - Any missing or incomplete data rows are removed to ensure clean data for analysis.

2. **Data Visualization**:
   - The data is visualized through various charts (pie charts, bar graphs) to understand the distribution of responses. For example:
     - Gender distribution of respondents.
     - Proportion of students satisfied with their branch.
     - The relationship between attendance and mental health (depression, anxiety).
   - Key insights from the visualizations:
     - Most students reported feeling tension related to the 85% attendance requirement.
     - First-year students are more likely to report depression, while third-year students tend to deny it.
     - A relationship is observed between CGPA and mental health, with students having CGPA in the 7-8 range reporting more panic attacks.

3. **Data Transformation**:
   - To prepare the data for machine learning models, categorical variables (e.g., gender, course, CGPA range) are encoded into numeric values using `LabelEncoder`.

4. **Modeling**:
   Three machine learning models were tested to predict whether a student might be experiencing depression based on the survey data:
   - **Decision Tree Classifier**: A simple and interpretable model.
   - **Logistic Regression**: Used for binary classification (depressed or not depressed).
   - **K-Nearest Neighbors (KNN)**: Another classification model that looks at the ‘nearness’ of data points to make predictions.
   
   The models are trained on 60% of the data and tested on 40%. The accuracy of each model is calculated to see which performs best.

   **Accuracy Scores**:  
   - Decision Tree Classifier: 0.527027027027027
   - Logistic Regression: 0.6351351351351351
   - KNN: 0.527027027027027

   The Logistic Regression model was selected for final predictions due to its highest accuracy.

5. **Prediction**:
   - After training the model, users can input their survey responses (gender, course, CGPA, anxiety, etc.) to predict if they are likely to experience depression.
   - Based on user input, the model will output a prediction, indicating whether the student is likely to be in depression or not.

---

### **How to Use**

1. **Setup**:  
   Clone the repository and install necessary libraries using:
   ```
   pip install pandas matplotlib seaborn scikit-learn
   ```

2. **Running the Code**:  
   Open the Python script or Jupyter Notebook and run the entire code in the sequence. The model will ask you for inputs (such as gender, CGPA, anxiety status, etc.), and then make a prediction about your mental health status based on the survey data.

   Example inputs:
   - Choose your gender (1 for male, 0 for female)
   - What is your course? (e.g., 0 for CSE, 1 for CSE-AI, etc.)
   - Current year of study (e.g., 0 for 1st year, 4 for 5th year, etc.)
   - CGPA range (e.g., 1 for CGPA 7-8, 2 for CGPA 8-9)
   - Whether you have anxiety or panic attacks
   - Whether you sought specialist treatment

   After entering your responses, the model will output a message indicating whether the student is likely to be depressed or not.

---

### **Key Findings**
- **Gender**: Males report higher levels of anxiety and depression compared to females, based on the available data.
- **Attendance Stress**: A significant portion of students reported feeling stressed over the 85% attendance rule, especially among students with lower CGPA.
- **Depression & CGPA**: Students with a CGPA in the 8-9 range are less likely to experience depression compared to those with CGPA below 7 or above 9.
- **Anxiety by Year of Study**: First-year students tend to openly acknowledge anxiety, whereas third-year students often deny it.

---

### **Conclusion**

This analysis provides valuable insights into how mental health affects students' academic performance, particularly their CGPA. The predictive models could potentially be expanded for real-world applications, such as helping universities identify students at risk of depression and offering appropriate support services.

### **Future Work**
- Incorporating more data features like study habits, social factors, and personal life events could improve the model's accuracy.
- Expanding the survey to a larger and more diverse student population would provide more reliable insights.
  
---

Let me know if you need any further modifications or additions to this README!
