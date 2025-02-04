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

# problem 4.1 Q/A
What patterns do you observe in the training and validation accuracy curves?
Early Training

Both accuracies increase fast Shows initial learning

Peak Performance

Improvement slows down Indicates learning plateau

Warning Signs

Training: 99% Validation: 89% Big gap = overfitting

Unstable Signs

Jumping validation accuracy suggests: ↑ Learning rate too high or ↓ Dataset too small

////////////////////////////////////////////////////////////////////////////////

How can you use TensorBoard to detect overfitting?
Here's a simpler breakdown of detecting overfitting using TensorBoard:

Monitor Accuracy

Use TensorBoard's Scalars tab
Warning sign: Training accuracy rises while validation stays flat Example: Training 99% vs Validation 85%
Fix: Add dropout layers or stop training earlier
Check Loss Values

Both losses should decrease together
Red flag: Training loss drops while validation loss grows Example: Training 0.01 vs Validation climbing (0.3 → 0.4 → 0.5)
Fix: Simplify model or add regularization
Watch Weight Patterns

Use Histograms tab
Problem: Extreme or concentrated weights
Fix: Add L2 regularization to control weight size
Key Steps:

Launch TensorBoard (tensorboard --logdir=logs/fit)
Compare training vs validation metrics
Adjust model based on patterns seen
///////////////////////////////////////////////////////////////////////////

3.What happens when you increase the number of epochs? Here's a simpler explanation of the three main phases in model training:

Learning Phase (Early)
Both accuracies improve
Loss decreases
Example: Training 70% → 85%
Good sign: Model is learning properly
Plateau Phase (Middle)
Improvements slow down
Little change in metrics
Example: Training ~95%, Val ~90%
Normal: Model has learned most patterns
Overfitting Phase (Late)
Training accuracy keeps rising
Validation accuracy drops
Training loss decreases while validation loss grows
Problem: Model is memorizing, not learning
Think of it like studying for a test:

First you learn quickly
Then progress slows as you master basics
Studying too long might make you memorize exact questions instead of understanding concepts
