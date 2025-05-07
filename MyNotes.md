## 01. How can different epochs have very different val loss but very similar val accuracy?

Loss refers to the probability so if the model is less confident but the response is still right, the loss will increase while the accuracy stays the same. In a case where the probability is 0.9 for the prediction for a 2, assuming its the highest probability, it would be marked as correct, raising the accuracy, and the loss is low, bringing the loss down. On the contrary, with 0.6 for a prediction for it to be 2, assuming 0.6 is the highest probability, the loss will be higher than it would be for the other example, but the accuracy would be the same. Accuracy refers to the output, while loss refers to the probability. The probability could be lower while the accuracy is the same.

## 02. Explain Binary Cross Entropy Loss Formula

$$-\frac{1}{N}\sum_{i=1}^{N}y_{i}*log(p(y_{i})) + (1-y_{i}) * log(1-p(y_{i}))$$

## 03. Explain Categorical Cross Entropy Formula. How is this different from Sparse Categorical Cross Entropy

[Answer]
