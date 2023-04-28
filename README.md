## Inverse-Subset

This notebook constructs a subset of CIFAR-10 cat/dog data, on which it's better to train with inverted labels than the true labels.

Steps executed:
1. Train a model on 15% of cat/dog training examples (-> 75% acc).
2. On the remaining 85%, evaluate the model.
3. Take the 15% of that which is most confidently mis-predicted.
4. Train on this subset (-> 37% acc).

If the labels of this subset are inverted, it should be clear that this will yield 100 - 37 = 63% accuracy.

