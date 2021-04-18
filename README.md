# Automated Machine Learning Pipeline Class

- [Session 1 - From Modelling to Production](#session1)
- [Session 2 - Software Engineering for ML](#session2)
- [Session 3 - Toolkit: Git](#session3)
- [Session 4 - Toolkit: Colab & Python](#session4)
- [Session 5 - Toolkit: Python Environments & Visual Studio & Health Infomatics](#session5)
- [Session 6 - Data Set, Data Sample, Data Issues](#session6)
- [Session 7 - Create Fake Data (is Fun!)](#session7)
- [Session 8 - Linear Regression with Fake Data](#session8)
- [Session 9 - Deeplearning Scenario, intro to tensorflow, data Preparation](#session9)
- [Session 10 - Data Augmenting](#session10)

---

<a id=session1></a>
### Session 1 - From Modelling to Production
Intro to ML modelling

- DS Modelling
- DS Life Cycle
- DS principles
- ML pipeline
- Production of ML - ML development
- Production of ML - tasks for apply
- ML Pipeline - Target
- Directed Acyclic Graph
- ML Pipeline - Production ML Infrastructure
- Orchestration References:

  - Executive Data Science: A Guide to Training and Managing the Best Data Scientists (Brian Caffo, Jeff Leek, Roger Peng)
  - The Practical Guide to Managing Data Science at Scale (Domino)
  - Executive Data Science: Coursera-Johns Hopkins University
  - Building Machine Learning Pipelines by Hannes Hapke, Catherine Nelson


:diamond_shape_with_a_dot_inside: [**From Modelling to Production Video**](https://www.youtube.com/watch?v=qFJNkuBRytY)

---

<a id=session2></a>
### Session 2 - Software Engineering for ML

- Application Life Cycle
  - Software Development Life Cycle
-  Data Science Life Cycle

:diamond_shape_with_a_dot_inside: [**Software Engineering for ML Video**](https://www.youtube.com/watch?v=ARUyqRHupMc)

---

<a id=session3></a>
### Session 3 - Toolkit: Git

- Github
- Gitbash

:diamond_shape_with_a_dot_inside: [**Toolkit Git Video**](https://www.youtube.com/watch?v=IcTj5sek30g)

---

<a id=session4></a>
### Session 4 - Toolkit: Colab & Python

- Google Colab
- Install Python

:diamond_shape_with_a_dot_inside: [**Toolkit: Colab & Python Video**](https://www.youtube.com/watch?v=qOHHVdSA8qk)

---

<a id=session5></a>
### Session 5 Toolkit: Python Environments
In this session Thom Ives will explain how to build python virtual environment ... 

- Python 3.x
- Virtual environment wrapper
- System Variables
- Health Informatics Intro *(starts 36:14)*

:diamond_shape_with_a_dot_inside: [**Toolkit: Python Environments & Health Informatics Intro (starts 36:14) Video**](https://www.youtube.com/watch?v=qOHHVdSA8qk)

Ghaith Sankari will show one example about integrating Python project with .net core web api project using vitual studio.

[**VS Video 1**](https://www.youtube.com/watch?v=2dLjHUJ3lZE) | [**VS Video 2**](https://www.youtube.com/watch?v=IZOVSFwIpGo) | [**VS Video 3**](https://www.youtube.com/watch?v=BM3e0p0Iv7w)

---

<a id=session6></a>
### Session 6: Data Set, Data Sample, Data Issues
What is the importance of Data in ML process, what is the sampling and why issues might appears and what is the most important issues

- Feature Space
- Data Samples
- Data Issues
- Data Drift
- Concept Drift

**Assignment**: just explanation based: You take random samples of the same size from a large population and compute the mean of those samples and distribute those samples,
what will form from that distribution?

[Central Limit Theorem](https://www.statisticshowto.com/probability-and-statistics/normal-distributions/central-limit-theorem-definition-examples/)

**Resource**: [ML Data and Concept Drift](https://towardsdatascience.com/machine-learning-in-production-why-you-should-care-about-data-and-concept-drift-d96d0bc907fb)


:diamond_shape_with_a_dot_inside: [**Data Issues Video**](https://www.youtube.com/watch?v=FBivOf73kvw?t=67)

---

<a id=session7></a>
### Session 7 - Create Fake Data (is Fun!)
How to create fake data with Python.

**Assignment**: what is heteroskedasticity. Why is it a challenge, illustrate in notebook.
  - Send DM to Thom, correct answers can share with group.


`import matplotlib.pyplot as plt`<br>
`import random`<br>

`X = [x/10.0 for x in range(100)]` <br>

`Y = [2.0 * x + (random.random() - 0.5) * 0 + 5 for x in X]`<br>

`plt.scatter(X, Y)` <br>
``plt.title('This Is The Title')``<br>
``plt.xlabel('These Are The X Values')``<br>
``plt.ylabel('These Are The Y Values')``<br>
`plt.show()`<br>


added Colab Workbook for heterskedasticity [here](assignment_heteroskedasticity.ipynb)

:diamond_shape_with_a_dot_inside: [**Fake Data is Fun Video**](https://youtu.be/wfc4tNt8ZY8?t=137)

---

<a id=session8></a>
### Session 8 - Linear Regression with Fake Data

**Assignment** Play with the models, ❗ (Please repull the repo)

 1. First run the Fake Data Creations .py.
    1. Fake_Single_Feature_Linear_Data.py
    2. Fake_Single_Feature_NonLinear_Data.py
    3. Fake_Double_Feature_Linear_Data.py
    4. Fake_Double_Feature_NonLinear_Data_with_Functional_Noise.py
 2. Thise will create 5 different .csv files of data
 3. Next run each of the files, in the folder *Intro_to_Regression_Modeling*  and explore and play and understand the functionality of the script. look at the fake data creation.
 
 💡 you can `import sys`, and enter the follow code `sys.quit()` in the script to force stop, so you not running the complete script.
 
 <img src="/images/sys_quite.png" height="380" width="450">
 
 4. General_Toolls.py: this file is a module that you can call from with your scirpt, has function to calculate:
    1. print('Mean Square Error       --> [MSE](https://www.statisticshowto.com/probability-and-statistics/statistics-definitions/mean-squared-error/)
    2. print('Root Mean Square Error  --> [RMSE](https://www.statisticshowto.com/probability-and-statistics/regression-analysis/rmse-root-mean-square-error/)
    3. print('Mean Absolute Error     --> [MAE](https://www.statisticshowto.com/absolute-error/)
    4. print('Median Absolute Error   --> [MeDAE](https://www.statisticshowto.com/median-absolute-deviation/)
    5. print('R^2                     --> [r2](https://statisticsbyjim.com/regression/interpret-r-squared-regression/)
    6. print('Adjusted R^2            --> [r2_adj](https://www.statisticshowto.com/probability-and-statistics/statistics-definitions/adjusted-r2/)
  

[Regression Analysis](https://statisticsbyjim.com/regression/when-use-regression-analysis/)

[Regression Statistics](https://www.statisticshowto.com/probability-and-statistics/regression-analysis/)


:diamond_shape_with_a_dot_inside: [**Linear Regression with Fake Data Video **](https://youtu.be/vr1tFEtlv9A)

---

<a id=session9></a>
### Session 9 - Deeplearning Scenario, intro to tensorflow, data Preparation
#### Convolutional neural networks (CNN)

##### Summary of session

- Convolutional Layer
- Effect of Filter Size (Kernel Size)
- Max Pool
- Average Pool
- Batch Sizing
- Padding
- Epochs


👇 Here are some links that have some visual explanations and a playground to experiement.


- [Tinker With a Neural Network](https://playground.tensorflow.org/#activation=tanh&batchSize=6&dataset=circle&regDataset=reg-plane&learningRate=0.03&regularizationRate=0&noise=0&networkShape=1,1&seed=0.77132&showTestData=false&discretize=false&percTrainData=50&x=true&y=false&xTimesY=false&xSquared=false&ySquared=false&cosX=false&sinX=false&cosY=false&sinY=false&collectStats=false&problem=classification&initZero=false&hideText=false)
- [Convolution visualizer](https://ezyang.github.io/convolution-visualizer/index.html)
- [What is a Neural Network](https://towardsdatascience.com/what-is-a-neural-network-6010edabde2b)
- [Convolutional Nearual Network Python](https://www.datacamp.com/community/tutorials/convolutional-neural-networks-python)
- [Convolutional Neural Networks cheatsheet](https://stanford.edu/~shervine/teaching/cs-230/cheatsheet-convolutional-neural-networks?fbclid=IwAR0qn8GjS7fUjexad0GCjXYchU3kqHZOQC3n1Z1bhCw9hFDy3X_FxFoev_8)
- [Convolutional Neural Networks (CNNs) explained Video](https://www.youtube.com/watch?v=YRhxdVk_sIs)
- [A deeper understanding of NNets (Part 1) — CNNs](https://towardsdatascience.com/a-deeper-understanding-of-nnets-part-1-cnns-263a6e3ac61)
- [Difference Between a Batch and an Epoch in a Neural Network](https://machinelearningmastery.com/difference-between-a-batch-and-an-epoch/)
- [Epoch vs Iterations vs Batch size](https://towardsdatascience.com/epoch-vs-iterations-vs-batch-size-4dfb9c7ce9c9)
- [Padding and Stride](https://machinelearningmastery.com/padding-and-stride-for-convolutional-neural-networks/)
- [Avinash repo; opencv tutorials](https://github.com/AVI18794/OPENCV_TUTORIALS)



**RegeX** : Regular Expression `import re`  [What is regex?](https://regexone.com/)


:diamond_shape_with_a_dot_inside: [**Deeplearning Scenario, intro to tensorflow, data Preparation Video**](https://www.youtube.com/watch?v=_4sjZBacaDM)


<a id=session10></a>
### Session 10 - Data Augmenting

**Data Augmenting Techniques**

- Mirroring
  - Flip Horizontal / Vertical
  - Flip Random
  
- Cropping
- Rotate
- Recolor

- PCA, Principal Component Analysis (topic for later lesson)

*Ghaith*

Here is some notes about data augmenting session: 


Data augmentation techniques used in deep learning, but it is still part of data preparation. according to this fact, data augmentation mechanisms will be customized to create important part of ML pipeline.

I wanted to start with data quantity issues solving then we will back to the more fancy and funny part related to data quality.
the assignment for next week is answering the following questions:

- how to perform customized rotation(any value of degree not only 90), code in python is required, and i wish to find presenting volunteers, this task can be performed is many ways and cooperation with other family members to cover many ways to solve the assignment is allowed and appreciated.

- is it possible to re-color the grayscale image, and how: for this question we are not looking for coding examples, we are just looking for explaining and proofing about the answer, you can consider as research task, also brave presenter are highly appreciated.


:diamond_shape_with_a_dot_inside: [**Data Augmenting Video**](https://youtu.be/qwsQvRy5aDI?t=127)

