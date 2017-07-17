# Explaining behaviour of ML models with eli5 library (Mikhail Korobov)

- https://github.com/TeamHG-Memex/eli5,
- Information Retrieval by Christopher Manning
  (https://nlp.stanford.edu/IR-book/).

- Typical ML
  - Collect training data
  - Extract data
  - Train the classifier
  - Production
- But the in the real world it's not so simple
  - How do we evaluate quality?
  - Do we have bugs, or is the accuracy already as good as it gets?
  - Is the model reliable? Robust?
- There's no silver bullet, but understanding the model helps.
- Model example:
  - You get some idea from looking at the parameters of the model, but
    parameters are not commensuate, scales are different.
  - For correlated variables, their weights can be distributed in any way.
- eli5
  - Knows how to extract coefficients from various models.
  - Can explain black box models with LIME algorithm.
  - Example with text classification where we can improve the model by seeing
    why it classifies the messages a certain way.
    - We can see irrelevant information being used,
    - We can also see bugs in the library or in our own code.
- We can also explain decision trees and tree ensembles.
- Explaining random models:
  - Remove a feature (actually shuffle existing values), see what the model
    says, then you know if the feature was relevant (not implemented yet, but
    would be nice).
  - Train an explainable model using a black box model, but only in a small
    neighbourhood of an existing example. Explain the explainable model. (this
    we have in eli5)
- There's new research:
  - New white-box models,
  - Models with explanations built-in,
  - New ways to visualise models.
