# Customer-Analytics-Preparing-Data-for-Modeling

# Overview/Introduction

This project focuses on preparing a large customer dataset for efficient storage and modeling. The dataset, provided by Training Data Ltd., contains anonymized information about students enrolled in data science training programs. The goal is to clean and optimize the dataset to predict whether students are looking for a new job, which will help direct them to prospective recruiters. Efficient data storage and preprocessing are crucial for reducing model training times and improving scalability.

# Objectives

1. Clean and optimize the dataset for efficient storage and faster model training.
2. Identify and transform categorical, ordinal, and two-factor variables into appropriate data types.
3. Filter the dataset to focus on students with 10+ years of experience working at companies with 1,000+ employees.
4. Prepare the dataset for predictive modeling to determine if students are seeking new job opportunities.

# Data Source

The dataset, customer_train.csv, contains the following columns:
   - student_id: A unique ID for each student.
   - city: A code for the city the student lives in.
   - city_development_index: A scaled development index for the city.
   - gender: The student's gender.
   - relevant_experience: Indicates if the student has relevant work experience.
   - enrolled_university: The type of university course enrolled in (if any).
   - education_level: The student's education level.
   - major_discipline: The educational discipline of the student.
   - experience: The student's total work experience (in years).
   - company_size: The number of employees at the student's current employer.
   - company_type: The type of company employing the student.
   - last_new_job: The number of years between the student's current and previous jobs.
   - training_hours: The number of hours of training completed.
   - job_change: Indicates whether the student is looking for a new job (1) or not (0).

# Tools Used

- Python Libraries: Pandas, NumPy
- Data Types: Efficient data type conversion (e.g., int32, float16, category).
- Data Transformation: Mapping ordinal and two-factor categories to optimize storage and analysis.

# Insights

1. Categorical Variables:
    - The dataset contains several categorical variables, such as gender, relevant_experience, enrolled_university, and education_level.
    - These variables were converted to category or boolean data types to optimize memory usage.
2. Ordinal Variables:
    - Variables like education_level, experience, company_size, and last_new_job were mapped to ordered categories for better analysis.
3. Two-Factor Variables:
    - Variables like relevant_experience and job_change were converted to boolean values (True/False) for simplicity and efficiency.
4. Filtered Dataset:
    - The dataset was filtered to include only students with 10+ years of experience working at companies with 1,000+ employees.

# Key Findings

1. Dataset Size Optimization:
    - By converting columns to efficient data types (int32, float16, category), the dataset size was significantly reduced, improving storage and processing efficiency.
2. Relevant Experience:
    - The majority of students (13,792 out of 19,158) have relevant work experience.
3. Education Level:
    - Most students are Graduates (11,598), followed by Masters (4,361) and High School graduates (2,017).
4. Company Size:
    - The dataset includes students working at companies of various sizes, with a focus on larger companies (1,000+ employees) for the filtered subset.

# Recommendations

1. Further Data Exploration:
    - Explore correlations between variables (e.g., training_hours and job_change) to identify key predictors of job-seeking behavior.
2. Feature Engineering:
    - Create new features, such as years_since_last_job, to improve model performance.
3. Modeling:
    - Use the cleaned and optimized dataset to build predictive models (e.g., logistic regression, decision trees) to identify students likely to seek new jobs.
4. Scalability:
    - Apply similar data optimization techniques to the full dataset to ensure scalability for future modeling efforts.

# How to Use This Repository
1. Clone the repository.
2. Install the required Python libraries (pandas, numpy).
3. Run the Jupyter Notebook (Customer Analytics Preparing Data for Modeling.ipynb) to reproduce the data cleaning and optimization steps.
4. Explore the dataset and modify the code to conduct further analysis or prepare the data for modeling.
