# K-Nearest Neighbors

### Dataset

The MNIST dataset is a large grouping of handwritten numbers created to demonstrate machine learning capabilities by allowing a computer to classify any handwritten number after training on the MNIST images.

There are approximately 60,000 images of digits in this dataset, so split it up 80 percent was used to train the model, 10 percent was used to validate date during testing and the last 10 percent was used for labeling.

![N|Numbers](https://github.com/connorkutz/Machine-Learining/raw/master/K-Nearest%20Neighbors/numbers.png)

The Pima Indian Diabetes study is another historic dataset because this society has the highest rate of diabetes in the world. Studying this is useful because they are a homogeneous population meaning most other aspects of their lives and DNA are the same. This allows us to pinpoint specific variables like BMI and skin thickness to see their correlation with diabetes. 

![N|BMI vs Blood Pressure](https://github.com/connorkutz/Machine-Learining/raw/master/K-Nearest%20Neighbors/Example%20Correlation.jpg)

### Algorithm

K-Nearest Neighbors is one of the simplest machine learning algorithms. It creates a model based on measurements of many feature dimensions, then classifies an unlabeled data set as whichever label the k nearest data points are. The data in both the Pima Diabetes study and the MNIST images was very well organized and needed not processing or editing to be made useful, it was only divided into three pieces.

### Accuracy

To measure accuracy, the number of correct predictions was divided by the total number of predictions to give a percentage. For both data sets, the most accurate value for k was tested for by remodeling and testing on each value. In the case of the Pima Indian Diabetes set, the most accurate K number was 36 with Euclidian distance.

![N|accuracy](https://github.com/connorkutz/Machine-Learining/raw/master/K-Nearest%20Neighbors/Accuracy%20vs.%20K.jpg)

In the case of the Digit Identification, a K value of 3 was most successful. 

![N|K](https://github.com/connorkutz/Machine-Learining/raw/master/K-Nearest%20Neighbors/accuracy%20vs%20k.jpg)

Overall, the Pima Indian classifier was 76% accurate with very few false negatives (which is important when classifying for peoples’ health. 

![N|Confusion Matrix](https://github.com/connorkutz/Machine-Learining/raw/master/K-Nearest%20Neighbors/Confusion%20Matrix.jpg)

The Digit classifier was extremely accurate after ~30,000 data points to model on and the overall accuracy was 97%. 

![N|Confusion Matrix](https://github.com/connorkutz/Machine-Learining/raw/master/K-Nearest%20Neighbors/big%20Confusion%20Matrix.jpg)

### Runtime

Predictions using the KNN classifier take O(Nd) where d is the number of dimensions and N is number of neighbors. This is relatively fast and inexpensive. Training, on the other hand, is very expensive O(d^2) because every dimension of each instance needs to be processed and analyzed. For the Pima Diabetes dataset, creating the classifier took ~5 seconds and predictions were instant. The Digit recognition was much slower since the data set was so large and there were ~800 dimensions. “Wall time” was about 10 minutes to create the classifier and predictions were only a few seconds. 