# Non-parametric Bayesian Models

- In machine learning the most probable hypothesis given the data is the
  hypothesis that makes the data most probable (follows from Bayes rule if we
  assume identical prior probabilities for hypotheses).
- Most models used in ML are parametric, they usually incorporate some
  assumptions about the data, its amount and complexity.
- Non-parametric models can adapt to changing structure of the data and
  increasing complexity and amount.
  - Essentially this is achieved through infinite number of parameters but at
    any one time only a finite number of them is non-zero.

## Chinese restaurant process

- https://en.wikipedia.org/wiki/Chinese_restaurant_process
- Infinite number of tables (clusters), each of infinite capacity,
- A sequence of customers entering and sitting down,
- The first customer enters and sits at the first table,
- Each subsequent one can join an existing table or take a new one.
- Eventually we infer the number of clusters and where they are from the data.
  - This last point is a bit handwavy and I don't quite understand how random
    seating method is combined with similarity to produce the clustering.

## Libraries in Python

- SKLearn,
- Datamicroscopes (more advanced, but only available on Conda).

## Further reading

- Tutorial paper: http://gershmanlab.webfactional.com/pubs/GershmanBlei12.pdf
- ML book: https://www.cs.cmu.edu/~tom/mlbook.html
