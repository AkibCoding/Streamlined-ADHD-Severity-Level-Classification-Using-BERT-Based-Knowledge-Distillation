The study explores the use of knowledge distillation to develop a lightweight yet effective BERT-based model named LastBERT, optimized for natural language processing (NLP) tasks with a focus on classifying ADHD severity from social media text data. By distilling a large BERT model into LastBERT, a significant reduction in model parameters was achieved, resulting in a model 73.64% smaller than BERT-base-uncased. Despite the reduced size, LastBERT maintained robust performance across various tasks on the General Language Understanding Evaluation (GLUE) benchmark and achieved an 85% accuracy, F1 score, precision, and recall on the ADHD dataset. This indicates the model's potential as a tool for mental health diagnostics using NLP techniques in resource-constrained environments. The research underscores the viability of using free computational resources like Google Colab and Kaggle Notebooks for advanced NLP applications.

### Key Results
#### Performance on GLUE Benchmark Datasets
| Dataset | Epoch | Accuracy | Precision | Recall | F1 Score | Other Metric |
|---------|-------|----------|-----------|--------|----------|--------------|
| MRPC    | 2     | 71.08%   | 73.07%    | 91.40% | 81.21%   | -            |
| SST-2   | 2     | 82.11%   | 81.03%    | 84.68% | 82.82%   | -            |
| CoLA    | 10    | 69.13%   | -         | -      | -        | 0.1182 (Matthews Corr.) |
| QQP     | 3     | 82.26%   | 73.15%    | 81.87% | 77.27%   | -            |
| MNLI    | 3     | 70.45%   | -         | -      | -        | -            |
| STS-B   | 6     | -        | -         | -      | -        | 0.3374 (Pearson), 0.3429 (Spearman) |

#### Performance on ADHD Dataset
| Model         | Accuracy | F1 Score | Precision | Recall | Parameters |
|---------------|----------|----------|-----------|--------|------------|
| LastBERT      | 85%      | 85%      | 85%       | 85%    | 29M        |
| DistilBERT    | 87%      | 87%      | 87%       | 87%    | 66M        |
| ClinicalBERT  | 86%      | 86%      | 86%       | 86%    | 110M       |

#### Comparative Analysis of ADHD Text Classification
| Study                                           | Model Type                                  | Dataset           | Accuracy |
|-------------------------------------------------|---------------------------------------------|-------------------|----------|
| Andersson et al. (2020)                         | ML models with NLP features                 | Clinical Texts    | 78%      |
| Vasudevan et al. (2020)                         | SVM, Random Forests with NLP                | Text Messages     | 72%      |
| Mahmud and Hamza (2021)                         | LSTM, CNN with NLP                          | Chatbot Conversations | 75%  |
| Doshi-Velez et al. (2019)                       | Rule-based and ML methods with NLP          | Clinical Texts    | 82%      |
| Espinoza et al. (2021)                          | Topic modeling and classification algorithms| Social Media      | 79%      |
| Kumar et al. (2021)                             | Ensemble learning methods (ROBERTA)         | Social Media      | 76%      |
| **Our Study (LastBERT)**                        | **Student BERT**                            | **Reddit Posts**  | **85%**  |
| **Our Study (DistilBERT)**                      | **DistilBERT**                              | **Reddit Posts**  | **87%**  |
| **Our Study (ClinicalBERT)**                    | **ClinicalBERT**                            | **Reddit Posts**  | **86%**  |

### Conclusion
The research highlights the success of knowledge distillation in creating a compact, efficient model (LastBERT) that performs comparably to larger models (DistilBERT, ClinicalBERT) in NLP tasks and ADHD severity classification. This demonstrates the potential for deploying such models in resource-constrained environments, making advanced NLP techniques accessible for practical applications such as mental health diagnostics.

