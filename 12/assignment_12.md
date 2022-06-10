## Principal Component Analysis (PCA)

### (1) Baseline notebook code

- notebook: [assignment_12.ipynb](https://gitlab.com/cau-class/machine-learning/2022-1/assignment/-/blob/main/12/assignment_12.ipynb) 

### (2) Data

- input data: [assignment_12_data.txt](https://gitlab.com/cau-class/machine-learning/2022-1/assignment/-/blob/main/12/assignment_12_data.txt)

### (3) Problem definition

- data

    The input dataset consists of a set of point in the 2-dimensional Euclidean space as follows:

```math
\{ (x_i, y_i) \}_{i=1}^n = \{ (x_1, y_1), (x_2, y_2), \cdots, (x_n, y_n) \}
```
where $`(x_i, y_i) \in \mathbb{R}^2`$ represents a point in the 2-dimensional Eclidean space

- normalization

    The data should be normalized in such a way that features $`x`$ and $`y`$ have mean zero and standard deviation 1

```math
\tilde{x} = \frac{x - \mu_x}{\sigma_x}, \quad \tilde{y} = \frac{y - \mu_y}{\sigma_y}
```
- where $`\tilde{x}`$ and $`\tilde{y}`$ are normalized data
    - $`\mu_x`$ denotes the mean of $`x`$
    - $`\sigma_x`$ denotes the standard deviation of $`x`$
    - $`\mu_y`$ denotes the mean of $`y`$
    - $`\sigma_y`$ denotes the standard deviation of $`y`$

- convariance matrix

    The covariance matrix is given by:

```math
\Sigma = \frac{1}{n} \sum_{i=1}^n z_i z_i^T = \frac{1}{n} Z^T Z
```

where $`n`$ denotes the number of data and $`Z`$ is defined by:

```math
Z = 
\begin{bmatrix}
z_1^T \\
z_2^T \\
\vdots \\
z_n^T \\
\end{bmatrix}
```

where $`z_i = (\tilde{x}_i, \tilde{y}_i)`$

### (4) Solution

- the principal components are obtained by the eigenvectors and eigenvalues of the covariance matrix

```math
\Sigma \, u = \lambda \, u
```

where $`u`$ denotes eigenvector and $`\lambda`$ denotes eigenvalue of matrix $`\Sigma`$

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
