## Arvato Customer Segmentation Report
### Project Overview

This project analyzes demographics data for Arvato Financial Services to identify which segments of the population are most likely to become customers. Using unsupervised and supervised learning techniques, I created customer segmentation models and a predictive classifier to optimize marketing campaign targeting.

[Blog post link: Demystifying Customer Data for Arvato Financial Services](https://medium.com/@emmaezenwere/introduction-demystifying-customer-data-for-arvato-financial-services-497fc3cf7086)

### Key Components

#### Data Cleaning & Preprocessing: 
- Implemented a structured two-stage cleaning approach to handle extensive missing data in the raw datasets.
- Unsupervised Learning: Used K-means clustering and PCA to identify three distinct customer segments.
- Demographic Analysis: Discovered key characteristics of each segment, including age, financial behavior, and family status.
- Supervised Learning: Built a Random Forest classifier to predict which individuals are most likely to respond to marketing campaigns.
- Feature Enhancement: Added cluster membership as a feature to improve predictive performance.

#### Evaluate Model

The model’s performance is evaluated using two primary metrics: Accuracy and F-Score.

Accuracy: This metric is used to determine the proportion of correct predictions made by the model. It is a straightforward measure. The accuracy score is calculated by comparing the predicted values (y_val_pred) against the true values (y_val_split). 

F-Score (or F1-Score): The F-Score is particularly useful when dealing with imbalanced datasets. It is the harmonic mean of precision and recall, balancing the trade-off between them. It provides a more nuanced measure of a model’s performance in classifying minority classes, which can be crucial in real-world applications where the cost of false negatives or false positives can vary.

The classification_report provides a comprehensive view of these metrics, including precision, recall, and F1-score for each class, along with the overall accuracy.



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