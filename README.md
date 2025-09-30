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
 Dataset Description
 <img width="1176" height="698" alt="Screenshot 2025-09-30 192109" src="https://github.com/user-attachments/assets/a7679b0b-57bd-4cae-9042-3881e75d626c" />

Logistic Regression
<img width="1139" height="761" alt="Screenshot 2025-09-30 192132" src="https://github.com/user-attachments/assets/d7db3eb1-27f6-4a9a-8a4d-9d819573f784" />

- Accuracy: 72.6%  
- Strong performance in detecting **Credit reporting complaints (Recall ~98%)
- Struggles with Consumer Loan (Recall ~10%) and Mortgage (Recall ~29%)

Naive Bayes
<img width="1086" height="771" alt="Screenshot 2025-09-30 192153" src="https://github.com/user-attachments/assets/db42206c-b290-48da-a17c-8063d0d98180" />

- Accuracy:71.3%
- Similar trend as Logistic Regression, but slightly weaker overall  
- Performs better than Random Forest for smaller classes like Consumer Loan

Random Forest
<img width="1153" height="260" alt="Screenshot 2025-09-30 192234" src="https://github.com/user-attachments/assets/33c5a607-4fa7-4166-9129-2af96a2cec3b" />

<img width="1340" height="517" alt="Screenshot 2025-09-30 192255" src="https://github.com/user-attachments/assets/3fe33485-cf47-419c-ae15-8817888c014e" />

- Accuracy: 70.9%  
- High recall for Credit reporting, but Consumer Loan (Recall = 0%) not captured at all

Model Comparison and test results
<img width="1359" height="652" alt="Screenshot 2025-09-30 192316" src="https://github.com/user-attachments/assets/66f89fee-d3f2-4b2b-8c97-7154edfa80f0" />

 ** Best Model: Logistic Regression **
  Balanced trade-off between accuracy and interpretability  
  Weighted F1-score ≈ 0.68 



Model Comparison
| Model              | Accuracy | Weighted F1-score |
|---------------------|----------|-------------------|
| Logistic Regression | 72.6%    | 0.68              |
| Naive Bayes         | 71.3%    | 0.67              |
| Random Forest       | 70.9%    | 0.65              |
  
