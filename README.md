# Employee Salary Prediction

## Motivation

**People Analytics** is transforming workforce decisions, enabling businesses to leverage data to predict salaries and optimize compensation strategies. By analyzing trends in employee data, companies can offer competitive, fair salaries that attract and retain top talent. This project uses **Machine Learning** to uncover these salary trends, helping organizations make data-driven decisions about compensation.

With the power of **AWS SageMaker** and **AWS S3**, the project ensures scalability and efficient model deployment, empowering businesses to optimize their workforce strategies and drive growth.

## Project Flow

1. **Initiate AWS SageMaker Notebook**
   - Set up an AWS SageMaker notebook instance to work in a cloud environment with all the necessary computational power.
   - This allows for easy integration with other AWS services such as S3 for data storage and SageMaker for model training and deployment.

2. **Perform Exploratory Data Analysis (EDA)**
   - Load the dataset containing employee features (e.g., age, education, years of experience, etc.) and their corresponding salary.
   - Analyze data using visualizations (e.g., histograms, boxplots, correlation heatmaps) to uncover relationships, trends, and outliers.
   - Clean and preprocess the data, handling missing values, encoding categorical variables, and scaling numerical features.

3. **Train Regression Model Using Scikit-learn**
   - Split the data into training and testing sets.
   - Use Scikit-learn to train a **Linear Regression** model and evaluate its performance using metrics like **Mean Squared Error (MSE)**, **R-squared**, and **Mean Absolute Error (MAE)**.
   - Fine-tune the model if necessary by adjusting hyperparameters and improving feature engineering.

4. **Evaluate the Model**
   - Evaluate the trained model's performance on the testing data.
   - Compare different metrics to ensure the model performs well, and determine whether it is ready for deployment.

5. **Train Linear Learner Model in AWS SageMaker**
   - Use the **AWS SageMaker Linear Learner** algorithm to train the model on the dataset.
   - Configure the model, including setting hyperparameters such as learning rate, batch size, and optimization strategy.
   - Leverage the computational power of SageMaker to train the model at scale.

6. **Deploy Model**
   - Deploy the trained model to an AWS SageMaker endpoint for real-time predictions.
   - Create a RESTful API to interact with the deployed model, sending input data and receiving salary predictions.
   - Monitor and evaluate the deployed model's performance in a production environment.

## Requirements

- **AWS Account** with access to SageMaker and S3.
- Python 3.x
- Libraries: 
  - **boto3** (AWS SDK for Python)
  - **pandas**, **numpy** (for data manipulation)
  - **matplotlib**, **seaborn** (for visualization)
  - **sklearn** (for machine learning algorithms)
  - **sagemaker** (for using AWS SageMaker)

## Steps to Run the Project

1. **Create a SageMaker Notebook Instance**:
   - Navigate to the AWS SageMaker dashboard and create a new notebook instance. Attach an IAM role with the necessary permissions to access S3, SageMaker, and other required resources.
   - Open the notebook instance and clone this repository or upload the necessary notebooks.

2. **Upload Dataset to S3**:
   - Upload the employee salary dataset to an S3 bucket for easy access in your notebook instance.

3. **Execute Notebook for EDA**:
   - Run the cells in the notebook to perform the EDA, including data loading, data cleaning, and visualizations.

4. **Train and Evaluate the Model**:
   - Train the regression model using Scikit-learn and evaluate its performance.
   - Compare results and fine-tune the model if necessary.

5. **Train Linear Learner Model in AWS SageMaker**:
   - Set up the SageMaker training job to use the Linear Learner algorithm.
   - Monitor the training process and retrieve the trained model.

6. **Deploy the Model**:
   - Deploy the model to SageMaker for real-time predictions and test it using sample input data.
