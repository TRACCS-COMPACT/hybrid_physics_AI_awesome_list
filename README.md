# Awesome list of software solutions for hybrid ESMs

List of sofware solutions for interfacing physics based simulation codes with machine learning models for high performance computing in the context of Earth System Models (ESMs). 

All listed names have corresponding LaTeX reference for citation in [bibtex file](https://github.com/TRACCS-COMPACT/hybrid_physic_IA_awesmone_list/blob/main/bibtex.bib). Ex: ```\cite{neural-fortran}```

Follow [contriburing instructions](https://github.com/TRACCS-COMPACT/hybrid_physic_IA_awesome_list/blob/main/CONTRIBUTING.md) to complete the list with any item that appears relevant to you.

## 1. Neural Network in Fortran

- [neural-fortran](https://github.com/modern-fortran/neural-fortran) : Fortran library that allows the creation of NN layers of arbitrary size and structure with several activation functions and stochastic gradient descent, uses Fortran 2018.
- [inference-engine](https://github.com/BerkeleyLab/fiats) : or ```Fiats```, as neural-fortran but leverage advanced Fortran 2023 features.
- [Fortran-Keras-Bridge](https://github.com/scientific-computing/FKB) : converts models built and trained in Keras (TensorFlow) to ones usable in Fortran, also provides a Fortran module to load and use converted models.
- [FNN](https://github.com/cerea-daml/fnn) : a Fortran module to implement simple, sequential neural networks. Can also convert Keras models to FNN-usable model.
- [module_neural_net](https://github.com/ESCOMP/PUMAS) : Single Fortran module for fully connected neural network inference with input/output scaling and optimized matrix multiplications and activations. Depends on BLAS/MKL and NetCDF. Part of NCAR PUMAS (used in CAM).

## 2. Python scripts from Fortran using Python bindings

- [forpy](https://github.com/ylikx/forpy) : not to be confused with **fortpy** !! Fortran module to wrap and manipulate Python objects (list, dict, numpy arrays...). Allows to import and use Python packages or user-defined Python functions. Requires to convert Fortran variables into Python variables by hand.
- [call_py_fort](https://github.com/nbren12/call_py_fort) : Fortran module to call Python functions written in a third Python script. Uses numpy to convert Fortran arrays passed as arguments.


## 3. Leverage C/C++ bindings of ML libraries

- [infero](https://github.com/ecmwf/infero) : Machine learning support library that runs pre-trained machine learning models for inference. Provides a common interface to multiple inference engines (TensorFlow LITE, TensorFlow C-API, ONNX-Runtime, TensorRT) and can be called from C/C++, Fortran or Python.
- [FTorch](https://github.com/Cambridge-ICCS/FTorch) : Fortran wrapper for calling PyTorch models for inference. Runs on CPU and Nvidia, Intel, AMD, and Apple GPUs.
- [pytorch-fortran](https://github.com/alexeedm/pytorch-fortran) : Fortran bindings to PyTorch for inference and training. Passes Fortran arrays/tensors and runs on CPU or GPU. Requires converting PyTorch models to TorchScript, which may be depreciated.
- [Fortran-TF-lib](https://github.com/Cambridge-ICCS/fortran-tf-lib) : Fortran wrapper for calling TensorFlow / Keras models for inference.
- [TorchClim](https://zenodo.org/records/8390519) : Fortran wrapper for calling PyTorch models. Also provides an additional layer to ease wrapping in the Community Earth System Model (CESM) framework.
- [TorchFort](https://github.com/NVIDIA/TorchFort) : Fortran/C/C++ wrapper for calling PyTorch models for training and inference. Also wraps the use of NVIDIA GPUs.

## 4. Leverage high-level couplers Fortran and Python APIs

- [smartsim](https://github.com/CrayLabs/SmartSim/tree/master) : Workflow library in which Fortran/C/Python clients can send data to a remote server that executes ML models and scripts on GPUs or CPUs.
- [PhyDLL](https://gitlab.com/cerfacs/phydll) : Coupler with Fortran/C/Python APIs. Allows two coupled scripts (heterogeneously written or not) to exchange data. Built on [CWIPI](https://w3.onera.fr/cwipi/fr).
- [Eophis](https://github.com/meom-group/eophis) : Python wrapper to ease the deployment and configuration of [OASIS](https://oasis.cerfacs.fr/en/) Python API. OASIS works similarly as PhyDLL and is built on [MCT](https://github.com/quantheory/MCT).
- [ZhangT2025](https://gmd.copernicus.org/articles/18/1917/2025/), [Wang2022](https://gmd.copernicus.org/articles/15/3923/2022/) : Miscellaneous articles with in-house developed coupling interface. 

## 5. Build Python wrappers of ESMs

- [fv3gfs-wrapper](https://github.com/ai2cm/fv3gfs-wrapper) : Python wrapper for the FV3GFS global climate model. The wrapper provides interfaces to advance the Fortran main loop and get/set variables used by the Fortran model to/from the Python environment.

## Related efforts on GitHub

 - [HybridESM Living Review](https://github.com/tbeucler/HybridESM) maintained by Tom Beucler (UNil)
