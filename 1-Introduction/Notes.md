# Notes

## 1-intro-to-ML

Early definition of machine learning (Arthur Samuel 1959): "Field of study that gives computers the ability to learn without being explicitly programmed"
- Samuel was a pioneer who wrote the first self-learning program, which played checkers
- The guy behind alpha-beta pruning

What should be the output of a learning program?
- A program, a model as output. Can be used in a regular program to predict stuff

Declarative knowledge
- "facts"
Imperative knowledge
- generalizable knowledge

### The learning paradigm

A set of observations, potentially labelled or not. How do we do inference to build a model. How do we use that model to make predictions.

- The observations: *training data*
- Infer something about process that generated data
- Use inference to make predictions about previously unseen data: *test data*

- Variations on paradigm
    - Supervised: labels given in training data, predict label for previously unseen data
    - Unsupervised: given a set of features without labels, group them in to natural clusters, or create labels for groups

### Feature engineering

Features never fully describe the situation. Represent examples by feature vectors that facilitate generalization
- Not all features matter for the prediction we want!

Labelled feature vectors may be identical, which may make it impossible to distinguish between labelled data. Need to be really careful when choosing features. Less can be more, since we can overfit when using too many features.

Distance between features
- Minkowski metric. p=1 manhattan metric, p=2 euclidean 

Confusion matrix (training error)
- measures mislabeling in the clusters (true positives, true negatives, false positives, false negatives)

accuracy = (the correctly labeled data over all data)
accuracy = (true positives + true negatives) / (true positives + true negatives + false positives + false negatives)

positive predictive value = (true positive) / (true positive + false positive)

sensitivity = (true positive) / (true positive + false negative)
[percentage correctly found]

specificity = (true negative) / (true negative + false positive)
[percentage correctly rejected]
