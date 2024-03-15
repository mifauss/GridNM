Grid-Restrained Nelder-Mead Algorithm
=====================================

Python implementation of grid-restrained variant of the Nelder-Mead algorithm, a derivative-free, unconstrained optimization algorithm that provably converges to a stationary point. See [1] for details.

This implementation has minimal dependencies and integrates well with the SciPy library. The code is fully typed, passes mypy, and comes with basic unit tests.

The MATLAB implementation [2] by the authors of [1] and the PyOPUS implementation [3] were used for reference. Variable names and default parameter were mostly taken from [1]. The adaptive parameters are as suggest in [4]. 

[1] Bűrmen, Árpád & Puhan, Janez & Tuma, Tadej. (2006). Grid Restrained Nelder-Mead Algorithm. Computational Optimization and Applications. 34. 359-375. 10.1007/s10589-005-3912-z.

[2] https://fides.fe.uni-lj.si/~arpadb/software-grnm.html

[3] http://spiceopus.si/pyopus/doc/optimizer.grnm.html?highlight=grnm#module-pyopus.optimizer.grnm

[4] Gao, F. and Han, L. Implementing the Nelder-Mead simplex algorithm with adaptive parameters. 2012. Computational Optimization and Applications. 51:1, pp. 259-277
