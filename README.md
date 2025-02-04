#Name : kalyan Guntuka
#700# : 700757036

#Tensorflow-assignment

#Step 1: Create a random tensor of shape (4, 6)
#Step 2: Find its rank and shape
#Step 3: Reshape to (2, 3, 4)
#Transpose to (3, 2, 4)
#Step 4: Broadcast a smaller tensor (1, 4) to match the larger tensor and add them
#Step 5: Explanation of broadcasting

#Broadcasting in TensorFlow:
- Allows tensors of different shapes to be used in element-wise operations.
- The smaller tensor (4,1) expands its second dimension to match (4,6).
- This process avoids unnecessary memory duplication.
