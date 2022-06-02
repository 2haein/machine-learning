## K-means clustering

### (1) Baseline notebook code

- notebook: [assignment_11.ipynb](https://gitlab.com/cau-class/machine-learning/2022-1/assignment/-/blob/main/11/assignment_11.ipynb) 

### (2) Data

- input data: [assignment_11_data.csv](https://gitlab.com/cau-class/machine-learning/2022-1/assignment/-/blob/main/11/assignment_11_data.csv)

### (3) Problem definition

- data

    The input dataset consists of a set of point in the 2-dimensional Euclidean space as follows:

```math
\{ (x_i, y_i) \}_{i=1}^n = \{ (x_1, y_1), (x_2, y_2), \cdots, (x_n, y_n) \}
```
where $`z_i = (x_i, y_i) \in \mathbb{R}^2`$ represents a point in the 2-dimensional Eclidean space

- objective

    The K-means clustering algorithm aims to partition input data into its subsets in such a way that the statistical homogeneity of each subset is maximized by minimizing an objective function
    
- notation

    - $`\ell(z) \in \{ 0, 1, 2, \cdots, K-1 \}`$ denotes the cluster label of point $`z`$
    - $`C_k = \{ z \mid \ell(z) = k \}`$ denotes a set of points with cluster label $`k`$
    - $`\mu_k`$ denotes the centroid of cluster $`C_k`$

### (4) Objective function

```math
\begin{align}
    \mathcal{L}( \{ C_k \}_{k=0}^{K-1}, \{ \mu_k \}_{k=0}^{K-1} ) &= \frac{1}{n} \sum_{i=1}^n \| z_i - \mu_{\ell(z_i)} \|_2^2 \\
    & = \frac{1}{n} \sum_{k=0}^{K-1} \sum_{z \in C_k} \| z - \mu_k \|_2^2
\end{align}
```

### (5) Optimization

Optimization algorithm aims to assign cluster label to each point and approximate centroid for each cluster in an alternatively way

- label $`\ell(z)`$ for each point $`z`$ is determined by:

```math
\ell(z) = \arg\min_k \| z - \mu_k \|_2^2
```

- centroid $`\mu_k`$ of cluster $`C_k`$ is determined by:

```math
\mu_k = \frac{1}{| C_k |} \sum_{z \in C_k} z
```

- Note that the value of centroid at the previous iteration should be used when its associated cluster is empty

### (6) Initialization

- assign random cluster label to each point for the initial condition

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

### (4) grading

- the scores are given by the final loss
    - rank 001 - 010 : 6
    - rank 011 - 030 : 5
    - rank 031 - 060 : 4
    - rank 061 - 100 : 3
    - rank 101 -     : 2
