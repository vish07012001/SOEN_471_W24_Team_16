# SOEN_471_W24_Team_16

## Introduction
This project aims to determine whether to escalate detected vulnerabilities in source code by leveraging machine learning algorithms. Collaborating with a small company specializing in source code vulnerability detection, our team focuses on utilizing static code analysis reports generated by the company.

## Dataset Description
We have selected three reports in XML format to be our dataset:
- atom (30 May 2020).xml - containing 1144 samples and 50 features
- WhatsApp (03 May 2020).xml - containing 635 samples and 49 features
- codedx.xml - containing 620 samples and 46 features
We will be working with some categorical features that we deem impactful toward the predictions of the status indicator. These features include:
- Severity: Severity level of the vulnerability, such as “info”, “low”, “medium or “high”
- Common Weakness Enumeration (CWE) Identifiers: Integer that identifies common types of software weaknesses associated with the vulnerabilities
- Description: Detailed textual descriptions of the detected vulnerabilities, including their nature and potential impact
- Tool Category and Name: Category and name of the tool used (e.g., ESLint may fall under “xss” or “security”, PMD may fall under “Best Practices”, etc)
- Rule Name: Guideline violated by the detected vulnerabilities (e.g., “Using Components with Known Vulnerabilities”, “Undeclared variables are global by default”, etc)
Our model will have to predict the status indicator of binary variable type, classifying vulnerabilities as 1 or 0, representing “Escalated” and “False Positive” (not escalated).

## Research Questions
- How do different machine learning algorithms perform in terms of evaluation metrics?
- What are the key challenges in integrating machine learning models into the existing vulnerability detection framework?

## Model Design

### Machine Learning Algorithms
To address the research questions, we plan to implement and compare the following machine learning algorithms:
- Decision Tree: Decision Tree is chosen for its interpretability and ability to handle both categorical and numerical data effectively. It provides a clear representation of decision-making processes, which aligns well with the need to understand the underlying logic behind considering our various features. We will encode categorical variables into numerical format, using techniques like one-hot encoding. We will also preprocess the textual descriptions of vulnerabilities and convert them into numerical vectors.
- Random Forest: Random Forest is selected as an ensemble learning method based on decision trees. It offers improved robustness and accuracy by aggregating multiple decision trees' predictions. This ensemble approach helps mitigate the risk of overfitting associated with individual decision trees and generally results in better generalization performance.
  
### Model Training and Evaluation
We will conduct model training using the provided dataset and evaluate the performance of each algorithm through metrics such as accuracy, precision, recall, and F1 score.

## Project Goals
The primary focus of our project is to develop and refine the specified machine learning algorithms. Should time permit, we will also work towards improving the user interface functionalities.
