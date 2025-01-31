
## K-Nearest Neighbors (KNN)

### Overview:
K-Nearest Neighbors (KNN) is a simple, non-parametric, and lazy supervised learning algorithm. It is commonly used for classification and regression tasks. KNN classifies a data point based on the majority class (for classification) or average (for regression) of its 'K' nearest neighbors in the feature space.

### How KNN Works:
1. **Data Points & Distance Metric**: The algorithm starts by determining the 'distance' between the data points. Common distance metrics used are:
   - **Euclidean distance**: For continuous variables.
   - **Manhattan distance**: Based on the absolute differences in the feature values.
   - **Cosine similarity**: For text or vector data.

2. **Find the Neighbors**: After selecting a distance metric, the algorithm identifies the 'K' closest data points (neighbors) to the test instance from the training dataset.

3. **Voting (for Classification)**: 
   - In classification, KNN assigns the most common class (majority voting) among the K neighbors. 
   - For example, if K = 3 and two neighbors belong to Class A and one neighbor belongs to Class B, the test instance is classified as Class A.

4. **Averaging (for Regression)**: 
   - In regression, KNN computes the average of the values of the K nearest neighbors.
   - For example, if the K nearest neighbors have values of 2, 3, and 5, the prediction for the test instance would be (2 + 3 + 5) / 3 = 3.33.

### Choosing the Right 'K' Value:
The number of neighbors, 'K', is a key hyperparameter in KNN. The value of 'K' directly affects the model's performance:
- **Small 'K' values** (e.g., 1) can make the model more sensitive to noise and outliers, leading to overfitting.
- **Large 'K' values** (e.g., 15) can smooth out predictions and reduce overfitting, but they may lead to underfitting.

### Strengths of KNN:
- Simple and easy to implement.
- Non-parametric: Doesn't assume any underlying distribution of the data.
- Can be used for both classification and regression tasks.

### Weaknesses of KNN:
- **Computationally expensive**: As the algorithm requires calculating distances for every query point, the computation cost grows with the size of the dataset.
- **Memory-intensive**: The algorithm stores the entire training dataset, which can be problematic for large datasets.
- **Sensitive to irrelevant features**: KNN can be sensitive to high-dimensional data if irrelevant features are present.

### Key Considerations:
- **Feature scaling**: KNN is sensitive to the range of data values, and features with larger ranges can dominate the distance calculation. It is important to standardize or normalize features before applying KNN.
- **Curse of Dimensionality**: As the number of features increases, the effectiveness of KNN decreases, as distances between points become less meaningful in high-dimensional spaces.

### Applications of KNN:
- **Classification tasks**: Spam email classification, disease diagnosis (e.g., cancer detection).
- **Regression tasks**: Predicting house prices based on historical data.
- **Anomaly detection**: Identifying outliers in data.
- **Recommendation systems**: Based on similarity to other users.

