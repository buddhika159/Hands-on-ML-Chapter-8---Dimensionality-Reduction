# Hands-on-ML-Chapter-8---Dimensionality-Reduction

![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
![NumPy](https://img.shields.io/badge/numpy-%23013243.svg?style=for-the-badge&logo=numpy&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-%23F7931E.svg?style=for-the-badge&logo=scikit-learn&logoColor=white)

## Description:
This repository includes the dimensionality reduction techeniqes discussed in the book [Hands-On Machine Learning with Scikit-Learn and TensorFlow](https://www.knowledgeisle.com/wp-content/uploads/2019/12/2-Aur%C3%A9lien-G%C3%A9ron-Hands-On-Machine-Learning-with-Scikit-Learn-Keras-and-Tensorflow_-Concepts-Tools-and-Techniques-to-Build-Intelligent-Systems-O%E2%80%99Reilly-Media-2019.pdf) chapter 8. Brefly, they are:
- **PCA** - Principal Component Analysis
- **Kernel PCA** - Extension of PCA
- **LLE** - Locally-Linear Embedding
- Other Dimensionality Reduction Techniques with Scikit-Learn
    - **t-SNE** - t-distributed Stochastic Neighbor Embedding
    - **MDS**
    - **Isomap**
Each of them have their own advantages or disadvantages depending on the dataset. They are discussed in [The summary of Chapter 8](https://github.com/buddhika159/Hands-on-ML-Chapter-8---Dimensionality-Reduction/blob/d5e413bc21ac61e87c9f6d14838ca68c8bb9f60d/Dimensionality%20Reduction%20Techniques%20Comparison.ipynb). Overall, for class data visualization `t-SNE` technique shows much better results. 


[Exercise 9](https://github.com/buddhika159/Hands-on-ML-Chapter-8---Dimensionality-Reduction/blob/4d6a0af9781cd8aca0837c3195442fdbd128b3ec/Exercise%209%20Effect%20of%20using%20PCA%20in%20model%20training.ipynb) 
This discusses the effect of dimension reduciton in model training by using PCA for the MNIST handwritten digit dataset.
- Random Forest classifier was used on the dataset and achieved `97%` test accuracy.
- Then PCA was used to reduce dimensionality before training with a new Random Forest classifier. It slowed down training and reduced performance to `94.81%`.
- When using PCA with softmax regression, we saw a x2 speedup with an accuracy of `92.55%`.


[Exercise 10](https://github.com/buddhika159/Hands-on-ML-Chapter-8---Dimensionality-Reduction/blob/4d6a0af9781cd8aca0837c3195442fdbd128b3ec/Exercise%2010%20PCA+t-SNE%20to%20reduce%20the%20MNIST%20dataset.ipynb)
In this exercise we look at the MNIST handwritten digit dataset and use above techniques to visualize. Below shows the results of implementations. 

<p align="middle">
  <img src="images/MNIST PCA.png" width="49%" />
  <img src="images/MNIST LLE.png" width="49%" /> 
</p>

<p align="middle">
  <img src="images/MNIST LDA.png" width="49%" />
  <img src="images/MNIST MDS.png" width="49%" /> 
</p>

<p align="middle">
  <img src="images/MNIST t-SNE.png" width="49%" />
</p>

To speedup the process and reduce few missc-lassifiers, we can use a pipeline to combine them.

<p align="middle">
  <img src="images/MNIST Pipeline PCA + LLE.png" width="49%" />
  <img src="images/MNIST Pipeline PCA + MDS.png" width="49%" /> 
</p>

<p align="middle">
  <img src="images/MNIST Pipeline PCA + t-SNE.png" width="49%" />
</p>



## Prerequisites:
Below libraries are needed to execute this Python code.
- Python 3.9
- Keras 2.7.0
- NumPy
- Matplotlib



