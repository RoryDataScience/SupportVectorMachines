# Support Vector Machines
 For projects involving Support Vector Machine Classification & Regression

What are Support Vector Machines?  <br>
An SVM maps training examples to points in space so as to maximise the width of the gap between the two categories. New examples are then mapped into that same space and predicted to belong to a category based on which side of the gap they fall.
In addition to performing linear classification SVMs can efficiently perform a non-linear classification using what is called the kernel trick, implicitly mapping their inputs into high-dimensional feature spaces.
When data are unlabeled, supervised learning is not possible, and an unsupervised learning approach is required, which attempts to find natural clusters of the data to groups, and then map new data to these formed groups. The support-vector clustering algorithm, applies the statistics of support vectors, developed in the support vector machines algorithm, to categorize unlabeled data, and is one of the most widely used clustering algorithms in industrial applications
Useful when the decision boundary is non-linear and complex

Optimization Objective  <br>
The cost function is known as Hinge Loss <br>
Will not output a probability: Hypothesis will predict 1 if (theta times x greater than or equal 0, otherwise 0)  <br>
Symbol means much, much larger >>  <br> 
This is the shape of the cost function when y = 1 (theta times x >> 0) \_   <br>
This is the shape of the cost function when y = 0 (theta times x << 0)  _/   <br>

Large Margin Classifier  <br>
Distance between the dataset classes is separated from a perspective that the data points on each side of the decision boundary are as 'large' as possible  <br>
Robust as it aims to separate the data with as high a margin as possible <br>
Can be sensitive to outliers as these data points can impact the placement of the decision boundary <br>
We want the projections onto theta to be as large as possible which only occurs with large margin dividing positive and negative examples theta0 i.e. the interept terms is zero then the decision boundary will pass through the origin  <br>
 
 What are Kernels? <br>
Permit learning complex, non-linear decision boundaries and overcome the complexity of deriving multiple polynomial/interaction features <br>
Kernels are similarity functions - Similarity is measure based on how close data point x is to the location of 'landmarks' <br>
Each landmark is considered a new feature within the dataset <br>
Data point very close to the landmark then similarity = 1, and vice versa <br>
The data points themselves can be used as the location of landmarks. This means that each feature will measure the locations/similarity between all data points (or those data points considered as landmarks) <br>
Can take advantages of advances optimisation techniques which allow SVM and Kernels to be useful --- This capability is not available for Logistic Regression due to the extensive run time <br>
Not all similarity function will make valid kernels --- Kernels must support SVM must satisfy "Mercers Theorem" to permit optimisation and convergence  <br>
Types: <br>
	○ Gaussian: Variance controls the slope of the kernel function, determining how quickly the similarity can reach 1 or 0 <br>
	○ Polynomial: Two additional parameters (a constant plus the polynomial degree --- performance generally worse than gaussian kernal --- deal with data where the data points x and landmarks, l are strictly non-negative <br>
	○ Esoteric Kernels: String Kernel/Chi-Square Kernel/Histogram Intersection Kernel --- Limited use and are just different ways to determine the similarity between data points and respective landmarks  <br>
	
How does bias/variance impact SVM? <br>
Parameter C = 1/lambda (where lambda is the regularisation term)  <br>
	○ Large C = small lambda --- Lower bias and high variance --- More prone to overfit <br>
	○ Small C = large lambda --- High bias and Low variance --- More prone to underfit <br>
Parameter sigma = This determines the smoothness of the kernel function <br>
	○ Determines the smoothness of the feature vector when kernels are implements  <br>
	○ If sigma**2 is small --- Features vary less smoothly --- Low bias and High variance --- More prone to overfit <br>
	○ If sigma**2 is large --- Features vary more smoothly --- High bias and Low variance --- More prone to underfit <br>

SVM Multi-Class <br>
Some packages have built in functionality  <br>
Otherwise, one-vs-all approach should be used <br>

SVM versus Logistic Regression <br>
If the number of features is large and the number of data points is small use logistic regression or SVM without a Kernel. No need for complex boundary for small number of data points <br>
If the number of features is large and the number of data points is moderate use SVM with a Gaussian Kernel <br>
If the number of features is small and the number of data points is large: Add more features then use logistic regression or SVM without Kernel <br>
Note: Linear SVM and Logistic Regression will commonly give similar results <br>

What error measures are suitable for model performance? <br>
SVM will **not** return a probability  <br>

Support Vector Machine Model Libraries  <br>
liblinear 
libsvm
