## Logistic Regression for a binary classification 

### (1) Baseline notebook code

- notebook: [assignment_08.ipynb](https://gitlab.com/cau-class/machine-learning/2022-1/assignment/-/blob/main/08/assignment_08.ipynb) 

### (2) Data

- input data: [assignment_08_data.csv](https://gitlab.com/cau-class/machine-learning/2022-1/assignment/-/blob/main/08/assignment_08_data.csv)

### (3) Problem definition for the logistic regression

- data

    The training dataset consists of a set of point in 2-dimensional Euclidean space and its label as follows:

```math
\{ (x_i, y_i, l_i) \}_{i=1}^n = \{ (x_1, y_1, l_1), (x_2, y_2, l_2), \cdots, (x_n, y_n, l_n) \}
```
where $`(x_i, y_i) \in \mathbb{R}^2`$ represents a point in Eclidean space and $`l_i \in \{0, 1\}`$ represents the class label of point $`(x_i, y_i)`$ 

- linear regression function

    The linear regression function $`f(\theta ; x, y)`$ associated with a set of model parameters $`\theta = (\theta_0, \theta_1, \theta_2) \in \mathbb{R}^3`$ for a given point $`(x, y) \in \mathbb{R}^2`$ is defined by:

```math
f(\theta ; x, y) = \theta_0 + \theta_1 x + \theta_2 y
```

- Sigmoid function

    The sigmoid function $`\sigma(z)`$ for $`z \in \mathbb{R}`$ is defined by:

```math
\sigma(z) = \frac{1}{1 + \exp(-z)}
```

- Derivative of Sigmoid function

    The derivative of the sigmoid function $`\sigma'(z)`$ is defined by:

```math
\sigma'(z) = \sigma(z) (1 - \sigma(z))
```

- Logistic regression function

    The logistic repression function is defined by:

```math
h(\theta ; x, y) = \sigma( f(\theta ; x, y) ) = \sigma( \theta_0 + \theta_1 x + \theta_2 y )
```

- residual 

    The residual $`\gamma_{i}(\theta)`$ associated with model parameter $`\theta`$ for data $`(x_i, y_i, l_i)`$ is defined based on the cross-entropy as follows:

```math
\gamma_{i}(\theta) = \gamma(\theta ; x_i, y_i, l_i) = - l_i \log(h_i) - (1 - l_i) \log(1 - h_i)
```
where $`h_i = h(\theta ; x_i, y_i)`$ represents the logistic repression function of data point $`(x_i, y_i)`$

- objective function

    The objective function $`\mathcal{L}(\theta)`$ associated with model parameter $`\theta`$ for training dataset $`\{ (x_i, y_i, l_i) \}_{i=1}^n`$ is defined by:

```math
\mathcal{L}(\theta) = \frac{1}{n} \sum_{i=1}^n \gamma_{i}(\theta) = \frac{1}{n} \sum_{i=1}^n \left( - l_i \log(h_i) - (1 - l_i) \log(1 - h_i) \right)
```

### (4) Solution

The optimal classifier $`\hat{h}(x, y)`$ for point $`(x, y)`$ is obtained by the logistic regression function $`h(\theta^* ; x, y)`$ with an optimal set of model parameters $`\theta^* = (\theta_0^*, \theta_1^*, \theta_2^*)`$ as follows:

```math
\hat{h}(x, y) \coloneqq h(\theta^* ; x, y) = \sigma( f(\theta^* ; x, y) ) = \sigma( \theta_0^* + \theta_1^* x + \theta_2^* y )
```
where optimal model parameters are obtained by:
```math
\theta^* = \arg\min_\theta \mathcal{L}(\theta)
```

### (5) Optimization using the gradient descent algorithm

The optimal set of model parameters $`\theta = (\theta_0, \theta_1, \theta_2)`$ is obtained by the gradient descent algorithm as follows:

```math
\theta^{t + 1} \coloneqq \theta^{t} - \eta \nabla \mathcal{L}(\theta^{t})
```
where $`t`$ denotes algorithm iteration and $`\eta`$ denotes a learning rate

## [Submission]

### (1) jupyter notebook file in `ipynb` format 

- download the baseline jupyter notebook to your local folder
- complete the jupyter notebook in `ipynb` format
- submit the `ipynb` file

### (2) jupyter notebook file in `PDF` format

- export the completed jupyer notebook to `PDF` format
- submit the `PDF` file

### (3) GitHub history page in `PDF` format

- make `git add` the jupyter notebook file to the repository for the assignment at your github
- make `git commit -m "initial commit"` at the beginning of coding
- make `git commit -m "final commit"` at the completion of coding
- make `git commit -m "your own message"` at least 10 times in such a way that your coding procedure is effectively demonstrated
- the number of `git commit` for the jupyter notebook should be at least 12
- export the GitHub history page for the jupyter notebook to `PDF` format
- submit the `PDF` file
