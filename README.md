problem with counting is that it would quickly blows out. it would be 27^context_length , if we takes 2 chars as context, it becomes 729, and when we take 3 chars as context, we have roughly 20k of context.

we're doing too much work for 200k+ examples, so perform backward, forward, update on many batches of data
so randomly select some portion of dataset, and only forward, backward, update on that mini batch and iterate on that many batches

it is better to approx gradient and make more steps than to compute it exactly and take fewer steps

as capacity of NN grows, it becomes more capable of overfitting your training set, that means loss on training set will be low, but all model is doing is only memorizing, if we try to evaluate with other stuff, it could have higher loss.

decaying learning rate for model training (decreasing the step), normally lr * .1 because if the step is too large when we train it several times already, there could be problem, so step is decreased

so, this is a far improvement from the previous bigram model, could be seen from example that it could at least form words that are readable.


## Credits

This work is made with the teachings and materials from Andrej Karpathy.