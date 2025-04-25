## Arvato Customer Segmentation Report
### Project Overview

This project analyzes demographics data for Arvato Financial Services to identify which segments of the population are most likely to become customers. Using unsupervised and supervised learning techniques, I created customer segmentation models and a predictive classifier to optimize marketing campaign targeting.

[Blog post link: Demystifying Customer Data for Arvato Financial Services](https://medium.com/@emmaezenwere/introduction-demystifying-customer-data-for-arvato-financial-services-497fc3cf7086)

### Key Components

#### Data Cleaning & Preprocessing: 
- Implemented a structured two-stage cleaning approach to handle extensive missing data in the raw datasets.

#### Visualization
-  General population and customer demographic data were plotted using histogram and barcharts for deeper insight on the data.


#### Transformation
- A transformation pipeline was applied to uniformly clean and apply feature engineering steps to each dataset. This ensures that any downstream analyses, particularly clustering or supervised modeling, are based on directly comparable inputs.



#### Modelling
- Unsupervised Learning: Used K-means clustering and PCA to identify three distinct customer segments.
- Demographic Analysis: Discovered key characteristics of each segment, including age, financial behavior, and family status.
- Supervised Learning: Built a Random Forest classifier to predict which individuals are most likely to respond to marketing campaigns.
- Feature Enhancement: Added cluster membership as a feature to improve predictive performance.

#### Model Evaluation & Justification 

- Given the binary nature of the classification problem—predicting whether a person is likely to be a customer Accuracy and F1-Score were chosen to evaluate the performance of the model.

 
 - Accuracy: Measures the overall proportion of correct predictions. It is particulary useful when:
- -  classes are relatively balanced in the dataset but may be misleading with imbalanced classes.
- - The cost of misclassification is similar across different customer classes.

- - For our model it answers the question, what percentage of customers did we classify correctly?.

- The accuracy score is calculated by comparing the predicted values (y_val_pred) against the true values (y_val_split). 

- F1-Score: This harmonic mean of precision and recall is more appropriate when :
	- Classes are imbalanced as is the case with our data (more non-customers than customers)
    - A balance is needed between false positives and false negatives
    - Different types of errors have different business impacts.

- The F1 score is calculated as follows:
F1 Score = 2 * (Precision * Recall) / (Precision + Recall)

- The model’s performance is evaluated using these two primary metrics, Accuracy and F-Score.

- Using both metrics together provides a more comprehensive evaluation of our classification model. Giving insight on whether it succeeds and where it needs improvements.


- Scikit Learn's classification_report function provides a comprehensive view of these metrics, including precision, recall, and F1-score for each class, along with the overall accuracy.




#### Results

- Identified that Cluster 2 represents the company's primary customer base (67.7% representation vs 45.6% in general population)
- Found that Cluster 1 (minimalist consumers, ages 30-45) is dramatically underrepresented in the customer dataset
- Achieved a classification accuracy of 98.7% using a Random Forest model with optimal hyperparameters

Files

- Arvato Project Workbook.ipynb: Main project notebook with complete analysis and helper functions for data cleaning, visualization and preprocessing

- requirements.txt: Required packages

Libraries Used

- pandas, 
- numpy
- scikit-learn
- matplotlib, 
- seaborn




## Quick Start

### Prerequisites

- Python 3.6+
- pip package manager

### Installation

1. **Create and activate a virtual environment**
   ```bash
   # Create virtual environment
   python3 -m venv myenv
   
   # Activate virtual environment
   # On Unix/macOS:
   source myenv/bin/activate
   # On Windows:
   myenv\Scripts\activate
   ```

2. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

3. Run all cells in the `Arvato Project Workbook.ipynb` Jupyter Notebook 
or execute cells from the begining sequentially.

Acknowledgments

- Data provided by Bertelsmann Arvato Analytics as part of the Udacity Data Science Nanodegree program.
- Udacity
- All my amazing tutors from the Udacity Data Science Nanodegree