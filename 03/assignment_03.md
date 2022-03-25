## 1. Image Gradient

### (1) Baseline notebook code

- notebook 1: [assignment_03_1.ipynb](https://gitlab.com/cau-class/machine-learning/2022-1/assignment/-/blob/main/03/assignment_03_1.ipynb) 

### (2) Data

- input image: [test.jpeg](https://gitlab.com/cau-class/machine-learning/2022-1/assignment/-/blob/main/03/test.jpeg)

### (3) Finte difference

- forward difference: 

    $`f'(x) = \frac{f(x+h) - f(x)}{h}`$

- backward difference: 

    $`f'(x) = \frac{f(x) - f(x-h)}{h}`$

- central difference: 

    $`f'(x) = \frac{f(x+h) - f(x-h)}{2 h}`$

## 2. First order Taylor approximation 

### (1) Baseline notebook code

- notebook 2: [assignment_03_2.ipynb](https://gitlab.com/cau-class/machine-learning/2022-1/assignment/-/blob/main/03/assignment_03_2.ipynb) 

### (2) Taylor approximation $`\hat{f}(x)`$ of function $`f(x)`$ at $`z`$

- $`\hat{f}(x) = f(z) + f'(z) (x - z)`$

## [Submission]

### (1) jupyter notebook files in `ipynb` format 

- download the baseline jupyter notebooks to your local folder 
- complete the jupyter notebooks in `ipynb` format
- submit the `ipynb` files

### (2) jupyter notebook files in `PDF` format

- export the completed jupyer notebooks to `PDF` format
- you can try to first convert jupyter notebook `ipynb` to `HTML` and then convert `HTML` to `PDF`
- submit the `PDF` files

### (3) GitHub history pages in `PDF` format

- make `git add` the jupyter notebook files to the repository for the assignment at your github
- for each jupyter notebook, make `git commit -m "initial commit"` at the beginning of coding
- for each jupyter notebook, make `git commit -m "final commit"` at the completion of coding
- for each jupyter notebook, make `git commit -m "your own message"` at least 10 times in such a way that your coding procedure is effectively demonstrated
- for each jupyter notebook, the number of `git commit` should be at least 12
- export the GitHub history page for each jupyter notebook to `PDF` format
- submit the `PDF` files
