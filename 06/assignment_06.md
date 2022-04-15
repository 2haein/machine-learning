## Linear regression

### (1) Baseline notebook code

- notebook: [assignment_06.ipynb](https://gitlab.com/cau-class/machine-learning/2022-1/assignment/-/blob/main/06/assignment_06.ipynb) 

### (2) Data

- input data: [assignment_06_data.csv](https://gitlab.com/cau-class/machine-learning/2022-1/assignment/-/blob/main/06/assignment_06_data.csv)

### (3) Problem definition for the linear regression

- data

```math
\{ (x_i, y_i) \}_{i=1}^n = \{ (x_1, y_1), (x_2, y_2), \cdots, (x_n, y_n) \}, \quad x_i \in \mathbb{R}, \; y_i \in \mathbb{R}, \; \forall i
```

- model 

```math
\hat{f}(\theta ; x) = \theta_0 + \theta_1 x, \quad \theta_0, \theta_1 \in \mathbb{R}
```

- model parameters

```math
\theta = (\theta_0, \theta_1)
```

- residual 

```math
\gamma_{i}(\theta) = \hat{f}(\theta ; x_i) - y_i
```

- objective function

```math
\mathcal{L}(\theta) = \frac{1}{2 n} \sum_{i=1}^n \gamma_{i}^2(\theta) = \frac{1}{2 n} \sum_{i=1}^n (\hat{f}(\theta ; x_i) - y_i)^2 = \frac{1}{2 n} \sum_{i=1}^n (\theta_0 + \theta_1 x_i - y_i)^2 
```

- solution

```math
\theta^* = \arg\min_{\theta} \mathcal{L}(\theta)
```

### (4) Optimization by Gradient Descent

- iterative optimization with gradient descent for the model parameters

```math
\theta^{(t+1)} \coloneqq \theta^{(t)} - \eta \, \nabla \mathcal{L}(\theta^{(t)})
```
where $`\eta > 0`$ in $`\mathbb{R}`$ is called learning rate.

- gradient descent step for each model parameter

```math
\theta_0^{(t+1)} \coloneqq \theta_0^{(t)} - \eta \, \frac{\partial \mathcal{L}}{\partial \theta_0}(\theta^{(t)})
```

```math
\theta_1^{(t+1)} \coloneqq \theta_1^{(t)} - \eta \, \frac{\partial \mathcal{L}}{\partial \theta_1}(\theta^{(t)})
```

### (5) Loss Surface

- three dimensional surface of the loss values in terms of the model parameters

```math
(\theta_0, \theta_1, \mathcal{L}(\theta_0, \theta_1))
```

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
