### Authors
* Ujjwal Ratan (ujjwalr@amazon.com)
* Aaron Friedman (ajfriedm@amazon.com)

This workshop was presented at AWS re:Invent 2019.

### Adverse Drug Reaction Clustering
A method to cluster drugs based on reactions reported in reviews. Amazon Comprehend Medical is used to generate a list of terms that consist of adverse reactions for the drugs generated from the reviews. Then Amazon SageMaker is used to create a custom clustering model to cluster the drugs based on those reactions. Finally, SageMaker Hyperparameter optimization is used to get the approriate number of clusters for the drugs.

### Dataset

We will be using the Drug Review Dataset (Drugs.com) for this workshop.
```
Felix Gräßer, Surya Kallumadi, Hagen Malberg, and Sebastian Zaunseder. 2018. Aspect-Based Sentiment Analysis of Drug Reviews Applying Cross-Domain and Cross-Data Learning. In Proceedings of the 2018 International Conference on Digital Health (DH '18). ACM, New York, NY, USA, 121-125. DOI: [https://dl.acm.org/citation.cfm?doid=3194658.3194677]
````
It is a part of the UCI machine learning repository.
```
Dua, D. and Graff, C. (2019). UCI Machine Learning Repository. Irvine, CA: University of California, School of Information and Computer Science.
```

### Steps
1. Use the template `AE_clustering_sagemaker.yaml` to create an AWS CloudFormation stack. You can do this via the AWS command line interface (CLI) using the follwoing command:

```
> aws cloudformation create-stack --template-body file://AE_clustering_sagemaker.yaml --stack-name adverse-reaction-git --capabilities CAPABILITY_IAM
```

Alternatively, you can log into the AWS console and navigate to the AWS CloudFormation console page, click on create stack and follow the prompts using the same CloudFormation YAML template that was previously mentioned.

For more details about
* AWS CLI: https://aws.amazon.com/cli/
* AWS CloudFormation creating a stack: https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-cli-creating-stack.html


The stack creates the IAM role, Sagemaker notebook instance and clones this repository on the instance. It also installs all dependencies.

2. Navigate to SageMaker -- Notebook instances. You will see the newly created instance in your list of instances. Launch the jupyter notebook in your local browser.
3. Go to the directory AdverseDrugReactionsClustering/artifacts/ and run through the notebooks starting with 0, 1, and 2 in order.

### Cleanup
Go to AWS CloudFormation and delete the stack to clean up the resources.
