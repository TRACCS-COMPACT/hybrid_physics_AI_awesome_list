# Hybrid Physic / AI methods : awesome list

List of exeisting solutions to create interface between low-level written physic codes and high-level written machine learning models.

All listed names have corresponding LaTeX reference for citation in [bibtex file](https://github.com/TRACCS-COMPACT/hybrid_physic_IA_awesmone_list/blob/main/bibtex.bib). Ex: ```\cite{neural-fortran}```

## 1. Neural Network in Fortran

- [neural-fortran](https://github.com/modern-fortran/neural-fortran) : Fortran library, allows creation of NN layers of arbitrary size and structure with several activation functions and stochastic gradient descent, uses Fortran 2018.
- [inference-engine](https://github.com/BerkeleyLab/fiats) : or ```Fiats```, as neural-fortran but leverage advanced Fortran 2023 features.
- [Fortran-Keras-Bridge](https://github.com/scientific-computing/FKB) : convert models built and trained in Keras (TensorFlow) to one usables in Fortran, also provide Fortran module to load and use converted model.
- [FNN](https://github.com/cerea-daml/fnn) : a Fortran module to implement simple, sequential neural network. Can also convert Keras model to FNN-useable model.


## 2. Python scripts from Fortran using Python bindings

- [forpy](https://github.com/ylikx/forpy) : do not mix up with fortpy ! Fortran module to wrapp and manipulate Python objects (list, dict, numpy arrays...). Allows to import and use Python package or user-defined Python functions. Requires to convert Fortran-variable to Python-variables by hand.
- [call_py_fort](https://github.com/nbren12/call_py_fort) : Fortran module to call Python functions written in a third Python script. Uses numpy to convert Fortran arrays passed as arguments.


## 3. Leverage C/C++ bindings of ML libraries




## 4. Leverage high-level couplers Fortran and Python APIs



