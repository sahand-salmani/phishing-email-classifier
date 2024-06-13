# Phishing Email Detection

This repository contains a project aimed at detecting phishing emails using a Naive Bayes classifier. The dataset consists of emails with various attributes, and the project involves several preprocessing steps and model training.

## Dataset

The dataset contains the following columns:

- `sender`: Email sender
- `receiver`: Email receiver
- `date`: Date of the email
- `subject`: Subject of the email
- `body`: Body of the email
- `label`: Label indicating if the email is phishing (1) or not (0)
- `urls`: Number of URLs in the email

## Steps Performed

### 1. Loading the Dataset

The dataset is loaded into a pandas DataFrame for processing.

### 2. Data Preprocessing

#### Combining Subject and Body

The `subject` and `body` columns are combined into a single column to create a unified text input for the model.

#### Removing Extra Columns

Columns like `receiver`, `date`, `sender`, `subject`, and `body` are removed as they are not needed after combining the `subject` and `body`.

#### Text Processing Methods

- **Lowering the Emails**: Convert all text to lowercase.
- **Removing Extra Spaces and Break Lines**: Remove unnecessary spaces and line breaks.
- **Removing Special Characters**: Remove non-alphanumeric characters.
- **Removing Short Emails**: Remove emails with a text length of less than 100 characters.

### 3. Model Training

#### Splitting Data into Train and Test Sets

The data is split into training and testing sets.

#### Training with Naive Bayes Algorithm

A Naive Bayes classifier is trained on the dataset.

### 4. Model Evaluation

The model is evaluated using accuracy score and classification report.

### 5. Testing with Custom Input

Custom inputs can be tested to check if the model correctly identifies phishing emails.

## Results

The performance of the model is evaluated using metrics such as accuracy score and classification report. 

## Contributing

Feel free to submit issues or pull requests if you have any improvements or bug fixes.
