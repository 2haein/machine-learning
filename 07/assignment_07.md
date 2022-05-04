## Linear regression with multiple variables

### (1) Baseline notebook code

- notebook: [assignment_07.ipynb](https://gitlab.com/cau-class/machine-learning/2022-1/assignment/-/blob/main/07/assignment_07.ipynb) 

### (2) Data

- input data: [assignment_07_data.csv](https://gitlab.com/cau-class/machine-learning/2022-1/assignment/-/blob/main/07/assignment_07_data.csv)

### (3) Problem definition for the linear regression

- data

```math
\{ (x_i, y_i, z_i) \}_{i=1}^n = \{ (x_1, y_1, z_1), (x_2, y_2, z_2), \cdots, (x_n, y_n, z_n) \}, \quad (x_i, y_i, z_i) \in \mathbb{R}^3, \forall i
```

- model 

```math
f(\theta ; x, y) = \theta_0 + \theta_1 x + \theta_2 y, \quad (\theta_0, \theta_1, \theta_2) \in \mathbb{R}^3
```

- model parameters

```math
\theta = (\theta_0, \theta_1, \theta_2) \in \mathbb{R}^3
```

- residual 

```math
\gamma_{i}(\theta) = f(\theta ; x_i, y_i) - z_i
```

- objective function

```math
\mathcal{L}(\theta) = \frac{1}{2 n} \sum_{i=1}^n \gamma_{i}^2(\theta) = \frac{1}{2 n} \sum_{i=1}^n (f(\theta ; x_i, y_i) - z_i)^2 = \frac{1}{2 n} \sum_{i=1}^n (\theta_0 + \theta_1 x_i + \theta_2 y_i - z_i)^2 
```

- solution

```math
\theta^* = \arg\min_{\theta} \mathcal{L}(\theta)
```

### (4) Optimization by Gradient Descent

- iterative optimization with gradient descent for the model parameters $`\theta = (\theta_0, \theta_1, \theta_2)`$

```math
\theta^{(t+1)} \coloneqq \theta^{(t)} - \eta \, \nabla \mathcal{L}(\theta^{(t)})
```
where $`\eta > 0`$ in $`\mathbb{R}`$ is a learning rate.

- gradient descent step for each model parameter

```math
\theta_0^{(t+1)} \coloneqq \theta_0^{(t)} - \eta \, \frac{\partial \mathcal{L}}{\partial \theta_0}(\theta^{(t)})
```

```math
\theta_1^{(t+1)} \coloneqq \theta_1^{(t)} - \eta \, \frac{\partial \mathcal{L}}{\partial \theta_1}(\theta^{(t)})
```

```math
\theta_2^{(t+1)} \coloneqq \theta_2^{(t)} - \eta \, \frac{\partial \mathcal{L}}{\partial \theta_2}(\theta^{(t)})
```

### (5) Loss Surface

- multi-dimensional surface of the loss values in terms of the model parameters

```math
(\theta_0, \theta_1, \theta_2, \mathcal{L}(\theta_0, \theta_1, \theta_2))
```

### (6) Solution

- regression function $`\hat{z} = f(\theta^* ; x, y) `$  with optimal model parameters $`\theta^*`$ for input $`(x, y)`$ 

```math
(x, y, f(\theta^* ; x, y))
```

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
