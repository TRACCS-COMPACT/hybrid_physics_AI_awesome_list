# Hybrid Physic / AI methods : awesome list

List of sofware solutions to interface between physics based simulation codes with machine learning models for high performance computing.

All listed names have corresponding LaTeX reference for citation in [bibtex file](https://github.com/TRACCS-COMPACT/hybrid_physic_IA_awesmone_list/blob/main/bibtex.bib). Ex: ```\cite{neural-fortran}```

## 1. Neural Network in Fortran

- [neural-fortran](https://github.com/modern-fortran/neural-fortran) : Fortran library, allows creation of NN layers of arbitrary size and structure with several activation functions and stochastic gradient descent, uses Fortran 2018.
- [inference-engine](https://github.com/BerkeleyLab/fiats) : or ```Fiats```, as neural-fortran but leverage advanced Fortran 2023 features.
- [Fortran-Keras-Bridge](https://github.com/scientific-computing/FKB) : convert models built and trained in Keras (TensorFlow) to one usables in Fortran, also provide Fortran module to load and use converted model.
- [FNN](https://github.com/cerea-daml/fnn) : a Fortran module to implement simple, sequential neural network. Can also convert Keras model to FNN-useable model.


## 2. Python scripts from Fortran using Python bindings

- [forpy](https://github.com/ylikx/forpy) : do not mix up with **fortpy** !! Fortran module to wrapp and manipulate Python objects (list, dict, numpy arrays...). Allows to import and use Python package or user-defined Python functions. Requires to convert Fortran-variable to Python-variables by hand.
- [call_py_fort](https://github.com/nbren12/call_py_fort) : Fortran module to call Python functions written in a third Python script. Uses numpy to convert Fortran arrays passed as arguments.


## 3. Leverage C/C++ bindings of ML libraries

- [infero](https://github.com/ecmwf/infero) : Machine learning that runs pre-trained machine learning model for inference. Provides a common interface to multiple inference engines (TensorFlow LITE, TensorFlow C-API, ONNX-Runtime, TensorRT) and can be called from C/C++, Fortran or Python.
- [FTorch](https://github.com/Cambridge-ICCS/FTorch) : Fortran wrapper to directly call PyTorch models for inference.
- [Fortran-TF-lib](https://github.com/Cambridge-ICCS/fortran-tf-lib) : Fortran wrapper to directly call TensorFlow / Keras models for inference.
- [TorchClim](https://zenodo.org/records/8390519) : Fortran wrapper to call PyTorch models. Also provide an additional layer to ease wrapping in the Community Earth System Model (CESM) framework.
- [TorchFort](https://github.com/NVIDIA/TorchFort) : Fortran/C/C++ wrapper to call PyTorch model for training and inference. Also wrapp use of NVIDIA GPUs.

## 4. Leverage high-level couplers Fortran and Python APIs

- [smartsim](https://github.com/CrayLabs/SmartSim/tree/master) : Workflow library in which Fortran/C/Python clients can send data to a remote server that executes ML models and scripts on GPU or CPU. 
- [PhyDLL](https://gitlab.com/cerfacs/phydll) : Coupler with Fortran/C/Python APIs. Allows two (heterogeneously written or not) coupled scripts to exchange data. Built on [CWIPI](https://w3.onera.fr/cwipi/fr).
- [Eophis](https://github.com/meom-group/eophis) : Python wrapper to ease the deployment and configuration of [OASIS](https://oasis.cerfacs.fr/en/) Python API. OASIS works similarly as PhyDLL and is built on [MCT](https://github.com/quantheory/MCT).
- [ZhangT2025](https://gmd.copernicus.org/articles/18/1917/2025/), [Wang2022](https://gmd.copernicus.org/articles/15/3923/2022/) : Miscellaneous articles with in-house developped coupling interface. 

