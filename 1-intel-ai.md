# Talking to Intel about AI

- The story that you need GPUs to do machine learning is somewhat of a myth:
  - General purpose CPUs do pretty well if the code is optimised,
  - GPUs limit you in terms of algorithm choice and how you separate your
    problem, in some cases the limitations are very restrictive,
  - Particularly in general AI, CPUs might be a better platform, unless you
    want to go all completely neural network.
  - So in general it depends and the devil is in the details (as always ;).
- Libraries/frameworks:
  - TensorFlow.
  - http://deeplearning.net/software/theano/
  - There's also SciKit/Learn.
  - Torch (different approach to TF and Theano, doesn't compile data flow
    graphs).
  - https://software.intel.com/en-us/ai/deep-learning
  - https://github.com/NervanaSystems/neon - Neural network library.
