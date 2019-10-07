# GABBE
A tool for explaining convolutional neural network classifications

Gabbe workflow:
1. If necessary create local clone of model in question
2. Obtain model's Jacobian matrix per class
3. Apply relevant Jacobian matrix to individual input and (if necessary) aggregrate output to create interpretable results.

This method relies on process of substitute model training through Jacobian-based dataset augmentation described in Papernot, Goodfellow et al's paper, Practical Black-Box Attacks against Machine Learning.

Finding the Jacobian matrix per class represents a compromise between specificity and computational intensity: the results will be more precise than with an overall Jacobian matrix, while also offering a globally applicable tool.

Papernot, Nicolas & McDaniel, Patrick & Goodfellow, Ian & Jha, Somesh & Celik, Z. Berkay & Swami, Ananthram. (2017). Practical Black-Box Attacks against Machine Learning. 506-519. 10.1145/3052973.3053009. 
