# A repository to demonstrate a simple MINLP in Pyomo

This repository demonstrates a simple mixed-integer nonlinear optimization problem (MINLP), its modeling and solution in Pyomo.
The problem is modeled both with a `NonNegativeIntegers` domain for the elements of the vector variable and with mixed domains of the vector variable (`NonNegativeIntegers` and `NonNegativeReals`).

The following files are included:

- `MINLP_description.pdf` - a mathematical description of the MINLP optimization problem;

- Jupyter Notebooks:
1. `clean_opt_integer.ipynb` - the optimization problem with a `NonNegativeIntegers` domain for the elements of the vector variable `z`; solved with a locally installed [*Couenne*](https://projects.coin-or.org/Couenne) solver, gives identical results as the [*BARON*](https://minlp.com/baron) solver;
1. `clean_opt_integer-neos.ipynb` - the same optimization problem, but solved with the [*NEOS server*](https://neos-server.org/neos/) and *Couenne* solver, *slightly* different results;
1. `clean_opt_mixed.ipynb` - the optimization problem with mixed domains (`NonNegativeIntegers` and `NonNegativeReals`) for the elements of the vector variable `z`; solving with a locally installed *Couenne* solver does **not** converge;
1. `clean_opt_mixed-neos.ipynb` - the same mixed optimization problem, but solved with the *NEOS server* and *Couenne* solver, **different** (presumably incorrect) results than the *BARON* solver.

- NL model files:
1. `mymodel-couenne-integer.nl` - model file for notebook **1**;
1. `mymodel-couenne-integer-neos.nl` - model file for notebook **2**;
1. `mymodel-couenne-neos.nl` - model file for notebook **4**.
