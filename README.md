GridNM
======

Grid-Restrained Nelder-Mead Algorithm

## Description

Python implementation of grid-restrained variant of the Nelder-Mead algorithm, a derivative-free, unconstrained optimization algorithm that provably converges to a stationary point. See [1] for details.

This implementation has minimal dependencies and integrates well with the SciPy library. The code is fully typed, passes mypy, and comes with basic unit tests.

The MATLAB implementation [2] by the authors of [1] and the PyOPUS implementation [3] were used for reference. Variable names and default parameter were mostly taken from [1]. The adaptive parameters are as suggest in [4]. 

[1] Bűrmen, Árpád & Puhan, Janez & Tuma, Tadej. (2006). Grid Restrained Nelder-Mead Algorithm. Computational Optimization and Applications. 34. 359-375. 10.1007/s10589-005-3912-z.

[2] https://fides.fe.uni-lj.si/~arpadb/software-grnm.html

[3] http://spiceopus.si/pyopus/doc/optimizer.grnm.html?highlight=grnm#module-pyopus.optimizer.grnm

[4] Gao, F. and Han, L. Implementing the Nelder-Mead simplex algorithm with adaptive parameters. 2012. Computational Optimization and Applications. 51:1, pp. 259-277

## Installation

GridNM can be installed from this repository. For example, using pip:
```
pip install git+https://gitlab.ets.org/rms/pdsm/testsecurity/gridnm
```

## Getting Started

Here is an example of how to use gridnm to minimize the 2D rosenbrock function:

```python
from gridnm import GridNM
from scipy.optimize import rosen

# initial point
x0 = np.array([-1.2, 1])

# create solver instance
gridnm = GridNM(rosen, x0)

# run solver
sol = gridnm.solve()

# print solution
print(f"x_opt = {sol.x}")
```

See the comments in `src/gridnm/gridnm.py` for options and parameters.