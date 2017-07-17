# GPU acceleration of global atmospheric models

- Modern processors:
  - CPU
    - most transistors are control and cache, not so much for ALU,
  - GPU
    - most transistors are in ALU, but you need very parallelisable algos,
  - FPGA
- Lately Moore's Law stopped for single-thread performance but the number of
  cores started going up a lot
- How do we utilise modern processors:
  - Directive-based tools in Fortran, ...
  - The processors have their own programming languages: CUDA, OpenCL, ISPC,...
- PyMIP
  - Based on PyCUDA, PyOpenCL, ...
- It works comparably to Fortran and C on CPU and faster on GPU and the code is
  portable.
- I converted existing model by wrapping Python with PyMIP and now it can be
  run on a GPU. It runs up to 10 times faster now.
- PyMIP will be renamed to OCCA (http://libocca.org/)
- Using Loo.py for metaprogramming and code generation:
  https://pypi.python.org/pypi/loo.py

## Q/A
- How do you debug this? When the language is compiled, you don't have the line
  number information anymore.
