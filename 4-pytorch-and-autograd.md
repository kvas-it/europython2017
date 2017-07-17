# An introduction to PyTorch and Autograd (Paul O'Grady)

## Matrix computations and Deep Learning

- Before deep learning/GPUs we only had linear algebra tools: BLAS, LINAPACK,
  Numpy...
- Now we're using GPUs more and work with Tensors, bla
  - TensorFlow
  - Theano
  - Caffee
  - Gradients + Automatic / Symbolc diff
  - Python is actively used

## Pytorch

- PyTorch is the new kid on the block
  - define-by-run vs define-and-run (more pythonic?)
- Fundamental data abstraction is Tensor
  - Can convert numpy arrays to Tensors
  - Reshape tensors using views
- Can work with a GPU

## AutoGrad

- Variables that allow specifying a computation graph
  - Variables know how they are calculated (DAG of dependencies + operations)
- Variables facilitate backpropagation: `requires_grad=True`
- Automatic differentiation of scalar valued functions:
  - Reverse-mode auto-differentiation,
  - Inspired by Python Autograd.
- Backpropagation, chain rule (look it up!)

## Linear regression

- Fit a line to the data.
- Model, cost function, learning (optmimisation) algorithm -> go.

## Define-and-run vs define-by-run

- Theano defines the computation graph explicitly.
- You can't change the structure of the model during learning, only the
  parameters get updated. In contrast, PyTorch allows that.
