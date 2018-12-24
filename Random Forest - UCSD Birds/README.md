# Bird Classification Using Random Forest

### I. Project Overview
Though automated bird classification is not a major issue in the world today, the information that we gather by solving datasets such as these can be very valuable. In this project, I used Random Forest to classify birds from the Caltech-UCSD Birds-200 2011 dataset[^1]. In classifying this dataset, I also wanted to show how changing parameters and data affects performance and accuracy of the results from Random Forest. The project was inspired by Dr. Caliskan’s lecture on bagging.

### II. Problem Statement
The goal is to create a Random Forest classifier using Matlab and the tasks involved are as follows:
1. Download and process the Caltech-UCSD Birds dataset
2. Train a random forest classifier on the binary attributes
3. Measure performance including accuracy, misclassifications, and runtime
4. Optimize data and classifier parameters
5. Measure performance again and analyze results

### III. Related Work
There have been many projects which aim to classify birds, for example Vidaña-Vila and Navarro aimed to classify birds from recordings[^2] of their songs and were quite successful. Later on, there’s been research on classifying birds solely on color features[^3]. Many have used random forest for similar classification problems.

### IV. Metrics
For this classifier, accuracy is measured in termsi of "estimated out-of-bag" error. This means that for each bootstrap sample taken from the data, the mean prediction error is measured in each tree made not using the given bootstrap sample. This can be written as:

[![N|Formula](https://github.com/connorkutz/Machine-Learining/raw/master/Random%20Forest%20-%20UCSD%20Birds/formula.png)]

Where 𝑡 is a terminal node, and 𝑞 ∗ (𝑡) = 𝑃(𝑋 ∈ 𝑡) is the chance that a bird is gets into that node of the tree. 

[![N|Formula](https://github.com/connorkutz/Machine-Learining/raw/master/Random%20Forest%20-%20UCSD%20Birds/formula.png)]

[^1]: https://pdfs.semanticscholar.org/c069/629a51f6c1c301eb20ed77bc6b586c24ce32.pdf
[^2]: https://www.mdpi.com/2306-5729/2/2/18/htm
[^3]: https://pdfs.semanticscholar.org/c069/629a51f6c1c301eb20ed77bc6b586c24ce32.pdf
