# Lab-6
This is the final Lab for the class Introduction to Machine Learning DIT 45100 AIW01

Install the following python packages needed for this Lab. I would advice that as practice for industry, you install these packages in a virtual environment.

`pip install jupyterlab` `pip install matplotlib` `pip install seaborn` `pip install pandas` `pip install sklearn`

You will be provided with some sample code in sample_code.ipynb that will provide you information that should be enough for you to complete the labs. The following tasks below are our objectives for the lab

You will be implementing the following algorithms we discussed in class:

Classification with SVM's (100 marks)
  - Download the Iris dataset from sklearn
  - Prepare data for 2d experiments and plots (5 marks)
    - Split your data into a training and test set using train_test_split from sklearn and set stratify=y
    - You will be grabbing 2 features from the dataset (You can use any of the feature selection methods you learnt in class)
       - Hint: I used chi-square feature selection because it is easy, fast and gave the same results as recursive feature elimination in previous labs
       - Show which features were selected 
    - Use StandardScaler to feature scale your data (If you are using chi-squared, you will want to do this after you have selected your features)

  - Prepare data for 3d experiments and plots (5 marks)
    - You will be grabbing the first 3 features from the dataset 
      - You will have to make the problem a binary classifiation problem
        - This will be done by grabbing Only labels with 0 or 1. We will be completely ignoring class 2
      - Split the data into a training and testing dataset using train_test_split from sklearn and set stratify=y (In this case remember y is your binary version of y which has only 2 labels 0 and 1) 

  - Train, predict and plot svm on 2d prepared data with the following configuration: (10 marks)
    - kernel="linear", C=1.0
        - Calculate the accuracy and hinge loss on the training set
        - Calculate the accuracy and hinge loss on the testing set
        - Plot the decision boundary with each point colored with its groundtruth class in 2D
          - encircle your support vectors 

  - Train, predict and plot svm on 3d prepared data with the following configuration: (10 marks)
    - kernel="linear", C=1.0
      - Plot 3D graph using binary training data with hyperplane separating the 2 points
        - Hint: You should have the plane perfectly seperating 2 classes 
      - Get the accuracy and hinge loss of the testing set

  - Train, predict and plot svm on 2d prepared data with the following configuration: (10 marks)
      - kernel="linear", C=100000
        - Calculate the accuracy and hinge loss on the training set
        - Calculate the accuracy and hinge loss on the testing set
        - Plot the decision boundary with each point colored with its groundtruth class in 2D
          - encircle your support vectors 

  - Train, predict and plot svm on 3d prepared data with the following configuration: (10 marks)
    - kernel="linear", C=100000
      - Plot 3D graph using binary training data with hyperplane separating the 2 points
        - Hint: You should have the plane perfectly seperating 2 classes (Our data is easily linear seperable so overfitting is not affecting us harshly)
      - Get the accuracy and hinge loss of the testing set

  - Train, predict and plot svm on 2d prepared data with the following configuration: (10 marks)
    - kernel="linear", C=0.0001
       - Calculate the accuracy and hinge loss on the training set
       - Calculate the accuracy and hinge loss on the testing set
       - Plot the decision boundary with each point colored with its groundtruth class in 2D
         - encircle your support vectors

  - Train, predict and plot svm on 3d prepared data with the following configuration: (10 marks)
    - kernel="linear", C=0.0001
      - Plot 3D graph using binary training data with hyperplane separating the 2 points
        - Hint: You will not have a plane perfectly seperating the data because it is underfit
      - Get the accuracy and hinge loss of the testing set

  - Train, predict and plot svm on 2d prepared data with the following configuration: (10 marks)
    - kernel="poly", C=1.0, degree=2, coef0=0.0, gamma="scale"
        - Calculate the accuracy and hinge loss on the training set
        - Calculate the accuracy and hinge loss on the testing set
        - Plot the decision boundary with each point colored with its groundtruth class in 2D
          - encircle your support vectors

  - Train, predict and plot svm on 2d prepared data with the following configuration: (10 marks)
    - kernel="poly", C=1.0, degree=3, coef0=0.0, gamma="scale"
        - Calculate the accuracy and hinge loss on the training set
        - Calculate the accuracy and hinge loss on the testing set
        - Plot the decision boundary with each point colored with its groundtruth class in 2D
          - encircle your support vectors

  - Train, predict and plot svm on 2d prepared data with the following configuration:(10 marks)
    - kernel="rbf", C=1.0, gamma="scale"
        - Calculate the accuracy and hinge loss on the training set
        - Calculate the accuracy and hinge loss on the testing set
        - Plot the decision boundary with each point colored with its groundtruth class in 2D
          - encircle your support vectors
