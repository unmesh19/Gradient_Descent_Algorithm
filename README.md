# Gradient_Descent_Algorithm

## Overview

This Python program performs gradient descent optimization for functions of one or more variables. It uses symbolic mathematics via the `sympy` library to compute gradients and optimizes a given function by iteratively updating the points until convergence.

### Features:
- Supports functions of any number of variables.
- Visualizes the optimization process for 1D and 2D functions.
- Takes user input for the function, starting points, and learning rate.
- Automatically stops once the gradient norm is sufficiently small (using a tolerance of `epsilon = 0.01`).

## Requirements

To run the code, ensure you have the following libraries installed:

- **SymPy**: for symbolic differentiation.
- **NumPy**: for numerical computations.
- **Matplotlib**: for plotting the gradient descent process.
- **Python 3.x**: for running the script.

You can install these dependencies using pip:

```bash
pip install sympy numpy matplotlib
```

## How to Use

1. **Run the Program**: Execute the script in a Python environment.

   ```bash
   python gradient_descent.py
   ```

2. **Input the Function**: When prompted, input the number of variables (`n`), and then input your function in terms of the variables `x0, x1, ..., xn-1`. For example, for a two-variable function, you might enter something like `x0**2 + x1**2`.

3. **Input the Starting Point**: Provide a starting point for the gradient descent algorithm as a comma-separated list. For example, for a two-variable function, you could input `1,1`.

4. **Input the Learning Rate**: Specify the learning rate `alpha`. A typical choice is a small positive number, such as `0.01` or `0.1`.

5. **Observe the Output**:
   - For 1D functions, the program will generate a 2D plot of the function and the optimization path.
   - For 2D functions, a 3D plot of the function's surface and the path taken by the gradient descent algorithm will be displayed.
   - For functions with more than 2 variables, the final optimized point will be printed, but no visualization will be provided.

### Example Usage:

For a 2D function:

- **Input**:
  ```
  Enter the number of variables: 2
  Enter your function in terms of x0, x1: x0**2 + x1**2
  Enter your starting point (comma-separated for 2 variables): 1, 1
  Enter the learning rate (alpha): 0.1
  ```

- **Output**:
  - A 3D plot of the function with the descent path.
  - The final optimized point, e.g., `[0.0, 0.0]`.

### Stopping Criterion:

The algorithm will stop when the norm of the gradient vector is less than `0.01`, which signifies that the descent has converged to a local minimum.

## Customization

- **Learning Rate (`alpha`)**: The learning rate determines the step size at each iteration. If the algorithm converges too slowly, try increasing `alpha`. If it oscillates or diverges, reduce `alpha`.
  
- **Epsilon**: The stopping criterion (set to `0.01` by default) can be adjusted to stop the algorithm earlier or allow it to run longer for more precision.

- **Starting Point**: The initial starting point can be critical for functions with multiple local minima, as gradient descent can get stuck in the nearest minimum.

## Plotting Behavior

- **1D Functions**: The script will generate a simple 2D plot of the function and the points visited by gradient descent.
  
- **2D Functions**: A 3D plot of the function surface and the descent path will be displayed using Matplotlib's `plot_surface`.

## Limitations

- **Multi-modal functions**: The gradient descent algorithm may not find the global minimum if the function has multiple local minima. The result depends on the starting point.
- **3D+ Visualization**: Visualization is currently limited to 1D and 2D functions. For higher dimensions, only the final optimized point is printed.

## License

This project is open source and licensed under the MIT License.
