## Heat equation

### (1) Baseline notebook code

- notebook: [assignment_04.ipynb](https://gitlab.com/cau-class/machine-learning/2022-1/assignment/-/blob/main/04/assignment_04.ipynb) 

### (2) Data

- input image: [barbara_color.jpeg](https://gitlab.com/cau-class/machine-learning/2022-1/assignment/-/blob/main/04/barbara_color.jpeg)

### (3) Finte difference

#### Gradient operator

```math
\nabla f(x, y) = 
\begin{bmatrix}
\frac{\partial f}{\partial x}\\
\\
\frac{\partial f}{\partial y}
\end{bmatrix}
```

#### First order derivatives

- forward difference

```math
\frac{\partial f}{\partial x}(x, y) = \frac{f(x+h, y) - f(x, y)}{h}
```

```math
\frac{\partial f}{\partial y}(x, y) = \frac{f(x, y+h) - f(x, y)}{h}
```

- backward difference

```math
\frac{\partial f}{\partial x}(x, y) = \frac{f(x, y) - f(x-h, y)}{h}
```

```math
\frac{\partial f}{\partial y}(x, y) = \frac{f(x, y) - f(x, y-h)}{h}
```

#### Laplace operator

```math
\Delta f(x, y) = \nabla \cdot \nabla f(x, y) = \frac{\partial^2 f}{\partial x^2}(x, y) + \frac{\partial^2 f}{\partial y^2}(x, y)
```

```math
\Delta f(x, y) = \frac{f(x+h, y) + f(x-h, y) + f(x, y+h) + f(x, y-h) - 4 f(x, y)}{h}
```

#### Second order derivatives

```math
\frac{\partial^2 f}{\partial x^2}(x, y) = \frac{f(x+h, y) - f(x, y)}{h} - \frac{f(x, y) - f(x-h, y)}{h}\\
   = \frac{f(x+h, y) + f(x-h, y) - 2 f(x, y)}{h}
```

```math
\frac{\partial^2 f}{\partial y^2}(x, y) = \frac{f(x, y+h) - f(x, y)}{h} - \frac{f(x, y) - f(x, y-h)}{h}\\
   = \frac{f(x, y+h) + f(x, y-h) - 2 f(x, y)}{h}
```

### (4) Heat equation

Let $`u : \Omega \times \mathbb{N} \mapsto \mathbb{R}`$ be a function $`u(x, y ; t)`$where $`(x, y) \in \Omega`$ denotes its 2-dimensional spatial domain and $`N`$ denotes its 1-dimensional temporal domain. 

- Isotropic diffusion process


```math
\frac{\partial u}{\partial t} (x, y : t) = \Delta u(x, y : t)
```

- initial condition

```math
u(x, y ; 0) = f(x, y)
```

- Neumann boundary condition
  
```math
\frac{\partial u}{\partial n}(x, y ; t) = 0 
```

- discretisation

```math
\frac{u(x, y ; t + \delta t) - u(x, y ; t)}{\delta t} = \Delta u(x, y : t)
```

```math
u(x, y ; t + \delta t) - u(x, y ; t) = \delta t \left( \Delta u(x, y : t) \right)
```

```math
u(x, y ; t + \delta t) = u(x, y ; t) + \delta t \left( \frac{u(x+h, y ; t) + u(x-h, y ; t) + u(x, y+h ; t) + u(x, y-h ; t) - 4 u(x, y ; t)}{h} \right)
```

### (5) Algorithm

```python
delta_t           = 0.25
h                 = 1
number_iteration  = 100
u                 = f

for t in range(number_iteration):

   u_x_forward    = compute_derivative(data = u, direction = x, scheme = forward, boundary_condition = neumann)
   u_x_backward   = compute_derivative(data = u, direction = x, scheme = backward, boundary_condition = neumann)
   u_y_forward    = compute_derivative(data = u, direction = y, scheme = forward, boundary_condition = neumann)
   u_y_backward   = compute_derivative(data = u, direction = y, scheme = backward, boundary_condition = neumann)

   laplace_u      = (u_x_forward - u_x_backward + u_y_forward - u_y_backward) / h
   u              = u + delta_t * laplace_u 
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
