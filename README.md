<!-- Python -->

# MNIST Digit Classification

Comparing three classic scikit-learn classifiers on the MNIST handwritten-digit dataset: **Logistic Regression**, a **Support Vector Machine** and a **Multi-Layer Perceptron**.

![Python](https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?logo=scikitlearn&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626?logo=jupyter&logoColor=white)

## Results

| Model | Configuration | Test accuracy |
| --- | --- | --- |
| Logistic Regression | multinomial, `saga` solver, 1,000 iterations | 92.3% |
| **SVM** | `SVC` with default RBF kernel | **97.9%** |
| MLP | one hidden layer of 128 units, 20 epochs | 95.9% |

The RBF-kernel SVM gives the best accuracy. The MLP gets close in only 20 epochs and would likely improve with more training; logistic regression is limited by its linear decision boundaries.

## Dataset

The notebook expects MNIST in CSV format next to the notebook:

- `mnist_train.csv` – 60,000 images
- `mnist_test.csv` – 10,000 images

Each row is a label followed by 784 pixel values (28×28). A CSV version is available on Kaggle (search for "MNIST in CSV").

## Run it

```bash
git clone https://github.com/alisedighmoghadam/MINST-classify.git
cd MINST-classify
pip install pandas scikit-learn jupyter
# add mnist_train.csv and mnist_test.csv to this folder
jupyter notebook MINST-classify.ipynb
```

Built as part of DPS920 coursework at Seneca Polytechnic.
