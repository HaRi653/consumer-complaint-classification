Consumer Complaint Text Classification

The goal of this project is to classify consumer complaints into one of the following categories:
- 0 → Credit reporting, credit repair services, or other personal consumer reports  
- 1 → Debt collection  
- 2 → Consumer Loan  
- 3 → Mortgage

  Dataset: [Consumer Complaint Database](https://catalog.data.gov/dataset/consumer-complaint-database)

Steps Followed
1. Exploratory Data Analysis (EDA) 
   - Class distribution plot  
   - WordCloud of complaint narratives  

2. Text Preprocessing
   - Lowercasing, removing special characters  
   - Stopwords removal & Lemmatization  

3. Feature Engineering
   - TF-IDF vectorization with 5000 features  

4. Model Training
   - Logistic Regression  
   - Naive Bayes  
   - Random Forest  

5. Model Evaluation & Comparison  
   - Accuracy, Precision, Recall, F1-score  
   - Confusion Matrices for each model  

6. Prediction Examples
   - Tested sample complaints to predict category
  

 Results
Logistic Regression
- Accuracy: 72.6%  
- Strong performance in detecting **Credit reporting complaints (Recall ~98%)
- Struggles with Consumer Loan (Recall ~10%) and Mortgage (Recall ~29%)

Naive Bayes
- Accuracy:71.3%
- Similar trend as Logistic Regression, but slightly weaker overall  
- Performs better than Random Forest for smaller classes like Consumer Loan

Random Forest
- Accuracy: 70.9%  
- High recall for Credit reporting, but Consumer Loan (Recall = 0%) not captured at all

 ** Best Model: Logistic Regression **
  Balanced trade-off between accuracy and interpretability  
  Weighted F1-score ≈ 0.68 



Model Comparison
| Model              | Accuracy | Weighted F1-score |
|---------------------|----------|-------------------|
| Logistic Regression | 72.6%    | 0.68              |
| Naive Bayes         | 71.3%    | 0.67              |
| Random Forest       | 70.9%    | 0.65              |
  
