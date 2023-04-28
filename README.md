# Inverse-Subset

This notebook constructs a subset of CIFAR-10 cat/dog data, on which it is better to train with inverted labels, rather than the true labels.

Steps executed:
1. Train a model on 15% of cat/dog training examples (-> 75% acc).
2. On the remaining 85% of examples, evaluate the model.
3. Take the 15% of those examples which is most confidently mis-predicted by the model.
4. Train a new model on this subset (-> 37% acc).

If the labels of this subset are inverted, it should be clear that this will yield 100 - 37 = 63% accuracy.
