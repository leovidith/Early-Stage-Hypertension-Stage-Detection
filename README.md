# Early stage Hypertension Stage Prediction 

## Overview
The **Hypertension Stage Prediction Project** utilizes a decision tree classifier (DTC) trained on a comprehensive hypertension dataset. This dataset includes critical features such as blood pressure readings, BMI, cholesterol levels, and lifestyle indicators. The primary objective is to predict hypertension stages, enabling early identification and intervention for individuals at risk. 

The dataset includes preprocessed features such as:
- **Age (years)**: Converted from raw 5-digit age format.
- **BMI**: Calculated using height and weight.
- **Blood Pressure Categories**: Encoded for efficient processing.

**Model**: The project uses a **DecisionTreeClassifier**, achieving **100% accuracy** on the test dataset after normalization using `MinMaxScaler`. This ensures feature scaling for optimal model performance.

## Agile Features (Implemented in Sprints)

### Sprint 1: Data Collection and Preprocessing
- Dataset cleaning: Removed irrelevant columns (`id`, `bp_category`).
- Applied **Ordinal Encoding** to categorical variables (e.g., `bp_category_encoded`).
- Feature engineering: Added `age_years` and `bmi`.

### Sprint 2: Model Training and Evaluation
- Split dataset: 80-20 training-test split with a fixed random state (101).
- Applied `MinMaxScaler` for feature scaling.
- Achieved **100% test accuracy** using a **DecisionTreeClassifier**.

### Sprint 3: Integration and Deployment
- Developed an interactive HTML form for feature input.
- Backend implementation in Flask to handle predictions and return results in real-time.


## Results
The model categorizes hypertension into the following stages:
1. **Elevated**
2. **Hypertension Stage 1**
3. **Hypertension Stage 2**
4. **Normal**

Results are delivered with near-instantaneous processing, providing actionable insights to users. Testing demonstrated **flawless stage prediction** on unseen data.


## Conclusion
### Use Cases:
1. **Clinical Decision Support**: Assists healthcare providers in classifying hypertension stages for diagnosis and treatment planning.
2. **Health Monitoring Apps**: Integration into wearable devices or mobile applications for proactive health management.
3. **Public Health Analytics**: Enables trend analysis in population health studies.
