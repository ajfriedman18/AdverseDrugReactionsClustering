### Authors
* Ujjwal Ratan (ujjwalr@amazon.com)
* Aaron Friedman (ajfriedm@amazon.com)

This workshop was presented at AWS Re:invent 2019.

### Adverse Drug Reaction Clustering
A method to cluster drugs based on reactions reported in reviews. Amazon comprehend medical is used to generate a list of terms that consist of adverse reactions for the drugs generated from the reviews. Then Amazon Sagemaker is used to create a custom clustering model to cluster the drugs based on those reactions. Finally, Sagemaker Hyperparameter optimization is used to get the approriate number of clusters for the drugs.

### Dataset

We will be using the Drug Review Dataset (Drugs.com) for this workshop.
Felix Gräßer, Surya Kallumadi, Hagen Malberg, and Sebastian Zaunseder. 2018. Aspect-Based Sentiment Analysis of Drug Reviews Applying Cross-Domain and Cross-Data Learning. In Proceedings of the 2018 International Conference on Digital Health (DH '18). ACM, New York, NY, USA, 121-125. DOI: [https://dl.acm.org/citation.cfm?doid=3194658.3194677]

It is a part of the UCI machine learning repository.
Dua, D. and Graff, C. (2019). UCI Machine Learning Repository. Irvine, CA: University of California, School of Information and Computer Science.

### Steps
1. Use the file AE_clustering_sagemaker.yaml template to create an AWS cloudformation stack. The stack creates the IAM role and Sagemaker notebook instance and clones this repository on the instance. It also intalls all dependencies.
2. Navigate to Sagemaker -- Notebook instances and launch the jupyter notebook in your local browser.
3. Go to the artifacts directory and run through the notebooks starting with 0,1 and 2 in order.

### Cleanup
Go to AWS cloudformation and delete the stack to clean up the resources.
