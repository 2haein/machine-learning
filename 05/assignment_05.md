## Polynomial regression by least square problems 

### (1) Baseline notebook code

- notebook: [assignment_05.ipynb](https://gitlab.com/cau-class/machine-learning/2022-1/assignment/-/blob/main/05/assignment_05.ipynb) 

### (2) Data

- input data: [assignment_05_data.csv](https://gitlab.com/cau-class/machine-learning/2022-1/assignment/-/blob/main/05/assignment_05_data.csv)

### (3) Problem definition for the polynomial regression

- data

```math
\{ (x_i, y_i) \}_{i=1}^n = \{ (x_1, y_1), (x_2, y_2), \cdots, (x_n, y_n) \}
```

- model 

```math
\hat{f}(\theta ; x) = \theta_0 x^0 + \theta_1 x^1 + \cdots + \theta_{p-1} x^{p-1}
```

- model parameters

```math
\theta = (\theta_0, \theta_1, \cdots, \theta_{p-1})
```

- residual 

```math
\gamma_{i}(\theta) = y_i - \hat{f}(\theta ; x_i)
```

- objective function

```math
\mathcal{L}(\theta) = \frac{1}{2 n} \sum_{i=1}^n \gamma_{i}^2(\theta)
```

- solution

```math
\theta^* = \arg\min_{\theta} \mathcal{L}(\theta)
```

### (4) Matrix representation for the polynomial regression

- problem definition in matrix representation

```math
A \, \theta = y
```
where 
```math
A = 
\begin{bmatrix}
x_{1}^{0} & x_{1}^{1} & \cdots & x_{1}^{p-1} \\
x_{2}^{0} & x_{2}^{1} & \cdots & x_{2}^{p-1} \\
\vdots & \vdots & \ddots & \vdots \\
x_{n}^{0} & x_{n}^{1} & \cdots & x_{n}^{p-1}
\end{bmatrix},
\quad
\theta =
\begin{bmatrix}
\theta_{0} \\
\theta_{1} \\
\vdots \\
\theta_{p-1}
\end{bmatrix},
\quad
y = 
\begin{bmatrix}
y_{1} \\
y_{2} \\
\vdots \\
y_{n}
\end{bmatrix}
```

- objective function

```math
\mathcal{L}(\theta) = \frac{1}{2 n} \| A \, \theta - y \|_2^2 = \frac{1}{2 n} ( A \, \theta - y )^T ( A \, \theta - y ) = \frac{1}{2 n} ( \theta^T A^T - y^T ) ( A \, \theta - y ) 
```

- solution

```math
\nabla \mathcal{L}(\theta^*) = \frac{1}{n} ( A^T A \theta^* - A^T y) = 0 
```

```math
\theta^* = ( A^T A )^{-1} A^T y  
```

### (5) Matrix representation for the polynomial regression with regularization

- objective function

```math
\mathcal{L}(\theta) = \frac{1}{2 n} \| A \, \theta - y \|_2^2 + \frac{\alpha}{2} \| \theta \|_2^2 = \frac{1}{2 n} ( A \, \theta - y )^T ( A \, \theta - y ) + \frac{\alpha}{2} (\theta^T \theta) = \frac{1}{2 n} ( \theta^T A^T - y^T ) ( A \, \theta - y ) + \frac{\alpha}{2} (\theta^T \theta)
```

- solution

```math
\nabla \mathcal{L}(\theta^*) = \frac{1}{n} ( A^T A \theta^* - A^T y) + \alpha \theta^* = 0\\
```

```math
\theta^* = ( A^T A + n \alpha I )^{-1} A^T y  
```
where $`I`$ denotes the identity matrix

## [Submission]

### (1) jupyter notebook file in `ipynb` format 

- download the baseline jupyter notebook to your local folder
- complete the jupyter notebook in `ipynb` format
- submit the `ipynb` file

### (2) jupyter notebook file in `PDF` format

- export the completed jupyer notebook to `PDF` format
- you can try to first convert jupyter notebook `ipynb` to `HTML` and then convert `HTML` to `PDF`
- submit the `PDF` file

### (3) GitHub history page in `PDF` format

- make `git add` the jupyter notebook file to the repository for the assignment at your github
- make `git commit -m "initial commit"` at the beginning of coding
- make `git commit -m "final commit"` at the completion of coding
- make `git commit -m "your own message"` at least 10 times in such a way that your coding procedure is effectively demonstrated
- the number of `git commit` for the jupyter notebook should be at least 12
- export the GitHub history page for the jupyter notebook to `PDF` format
- submit the `PDF` file
