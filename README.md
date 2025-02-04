# Name : kalyan Guntuka
# 700# : 700757036

# Problem -1 

Step 1: Create a random tensor of shape (4, 6)
Step 2: Find its rank and shape
Step 3: Reshape to (2, 3, 4)
Transpose to (3, 2, 4)
Step 4: Broadcast a smaller tensor (1, 4) to match the larger tensor and add them
Step 5: Explanation of broadcasting
 Broadcasting in TensorFlow:
- Allows tensors of different shapes to be used in element-wise operations.
- The smaller tensor (4,1) expands its second dimension to match (4,6).
- This process avoids unnecessary memory duplication.


# problem -2
Explanation:
Mean Squared Error (MSE):

Used for regression tasks.
Penalizes larger errors more heavily.

Categorical Cross-Entropy (CCE):

Used for classification tasks.
Measures how well predicted probabilities match actual labels.
Lower values mean better predictions.

Observations:

When predictions become less confident, MSE and CCE increase.
CCE is more sensitive to incorrect class probabilities than MSE.


# problem -3

Adam (Adaptive Moment Estimation):

Uses momentum to speed up learning.
Fast convergence but can sometimes overfit.

SGD (Stochastic Gradient Descent):

Slower but can generalize well.
More stable and avoids sharp oscillations.


# problem -4

The model trains for 5 epochs and logs data to "logs/fit/".
In TensorBoard, you will see:
Accuracy and loss trends for both training and validation.
Histograms of weights and biases (if enabled).
Graph of the model architecture.
