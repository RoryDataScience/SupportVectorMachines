## Project Title
Project One: Application of Linear and RBF Support Vector Machines to MNIST Dataset

## Motivation
- Set up a SVM for and evaluation of performance
- Data Cleaning for Computer Vision (sparse data, zero-variance predictors, imbalanced datasets, column mismatches in test and train, sub-sampling requirements)
- Implement a seris of potential benchmark "dummy" models (including a SGD Classifier)
- Use grid search for hypter parameter optimisation of the cost function C (and kernel decision boundary gamme for RBF)
- Presentation of Results for Classification (Confusion Matrix / Precision-Recall Curves / RoC Curve / Hyperparameter Optimisation Plots / Decision-Boundary Plots)

# Support Vector Machines
What are Support Vector Machines?  <br>
An SVM maps training examples to points in space so as to maximise the width of the gap between the two categories. New examples are then mapped into that same space and predicted to belong to a category based on which side of the gap they fall.
In addition to performing linear classification SVMs can efficiently perform a non-linear classification using what is called the kernel trick, implicitly mapping their inputs into high-dimensional feature spaces.
When data are unlabeled, supervised learning is not possible, and an unsupervised learning approach is required, which attempts to find natural clusters of the data to groups, and then map new data to these formed groups. The support-vector clustering algorithm, applies the statistics of support vectors, developed in the support vector machines algorithm, to categorize unlabeled data, and is one of the most widely used clustering algorithms in industrial applications
Useful when the decision boundary is non-linear and complex
Usually used for binary classification but can be extended to multiclass (supporting both one-versus-one and one-versus-all)
Parameters: C and Sigma (Gamma)
- C = 1/lambda (where lambda is the regularisation term)  <br>
	Large C = small lambda --- Lower bias and high variance --- More prone to overfit <br>
	Small C = large lambda --- High bias and Low variance --- More prone to underfit <br>
- Sigma = This determines the smoothness of the kernel function <br>
	Determines the smoothness of the feature vector when kernels are implements  <br
	If sigma**2 is small --- Features vary less smoothly --- Low bias and High variance --- More prone to overfit <br>
	If sigma**2 is large --- Features vary more smoothly --- High bias and Low variance --- More prone to underfit <br>

**What are the types of SVM?**
- Linear SVM
- Polynominal SVM 
- (Gaussian) Radial Basis Function SVM
- Sigmoid SVM

**Features of Support Vector Machine Models** <br>
- The cost function is known as Hinge Loss 
- Results do no output a probability
- Large Margin Classifier and seen as 'Robust' as it aims to separate the data with as high a margin as possible <br>
- Insensitive to outliers but performance is normally improved should feature scaling be implemented 
- May use kernels to:
	- Permit learning complex, non-linear decision boundaries and overcome the complexity of deriving multiple polynomial/interaction features
	- Kernels are similarity functions - Similarity is measure based on how close data point x is to the location of 'landmarks' 
	- The data points themselves can be used as the location of landmarks. This means that each feature will measure the locations/similarity between all data points (or those
	data points considered as landmarks) 

**Kernel Types**
- Gaussian: Variance controls the slope of the kernel function, determining how quickly the similarity can reach 1 or 0
- Polynomial: Two additional parameters (a constant plus the polynomial degree --- performance generally worse than gaussian kernal --- deal with data where the data points x and landmarks, l are strictly non-negative 
- Esoteric Kernels: String Kernel/Chi-Square Kernel/Histogram Intersection Kernel --- Limited use and are just different ways to determine the similarity between data points and respective landmarks  <br>

**SVM versus Logistic Regression** <br>
- If the number of features is large and the number of data points is small use logistic regression or SVM without a Kernel. No need for complex boundary for small number of data points <br>
- If the number of features is large and the number of data points is moderate use SVM with a Gaussian Kernel <br>
- If the number of features is small and the number of data points is large: Add more features then use logistic regression or SVM without Kernel <br>
Note: Linear SVM and Logistic Regression will commonly give similar results <br>

## Build Status
PoC project complete with clear extra work defined 

## Getting Started
Python version: 3.6.5
Notebooks: 20212101_SupportVectorMachines_Classification.ipynb

Additional Notes:
There is a quick methods to save requirements from the notebook by running pip3 freeze > requirements.txt once the project has been completed

Support Vector Machine Model Libraries  <br>
- liblinear 
- libsvm

### Installing
cd Documents/GitHub/SupportVectorMachines/
source .svm_env/bin/activate
python -m pip install -r requirements.txt

### Running the tests
Not implemented

**Break down into end to end tests** 
## Deployment
Not implemented

## Screenshots
Not implemented

## Versioning
Not implemented
