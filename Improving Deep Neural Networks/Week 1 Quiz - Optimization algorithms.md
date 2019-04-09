## Week 1 Quiz - Practical aspects of deep learning


#### 1.Which notation would you use to denote the 3rd layer’s activations when the input is the 7th example from the 8th minibatch?

- [ ] a [8]{3}(7)
- [ ] a [3]{7}(8)
- [x] a [8]{7}(3)
- [ ] a [3]{8}(7)


#### 2.Which of these statements about mini-batch gradient descent do you agree with?

- [x] You should implement mini-batch gradient descent without an explicit for-loop over different mini-batches, so that the algorithm processes all mini-batches at the same time (vectorization).
- [ ] One iteration of mini-batch gradient descent (computing on a single mini-batch) is faster than one iteration of batch gradient descent.
- [ ] Training one epoch (one pass through the training set) using mini-batch gradient descent is faster than training one epoch using batch gradient descent.


#### 3.Why is the best mini-batch size usually not 1 and not m, but instead something in-between?

- [ ] If the mini-batch size is m, you end up with stochastic gradient descent, which is usually slower than mini-batch gradient descent.
- [x] If the mini-batch size is m, you end up with batch gradient descent, which has to process the whole training set before making progress.
- [ ] If the mini-batch size is 1, you end up having to process the entire training set before making any progress.
- [x] If the mini-batch size is 1, you lose the benefits of vectorization across examples in the mini-batch.


#### 4. Suppose your learning algorithm’s cost JJ, plotted as a function of the number of iterations, looks like this:
#### Which of the following do you agree with?

- [x] If you’re using mini-batch gradient descent, this looks acceptable. But if you’re using batch gradient descent, something is wrong.
- [ ] If you’re using mini-batch gradient descent, something is wrong. But if you’re using batch gradient descent, this looks acceptable.
- [x] Whether you’re using batch gradient descent or mini-batch gradient descent, this looks acceptable.
- [ ] Whether you’re using batch gradient descent or mini-batch gradient descent, something is wrong.


#### 5.Suppose the temperature in Casablanca over the first three days of January are the same:

- [ ] v <sub>2	 =7.5, v_2^{corrected} = 10v 
2
corrected
​	 =10
- [ ] The process of gradually decreasing the learning rate during training.
- [ ] A technique to avoid vanishing gradient by imposing a ceiling on the values of the weights.
- [x] A regularization technique (such as L2 regularization) that results in gradient descent shrinking the weights on every iteration.


#### 6.Which of these is NOT a good learning rate decay scheme? Here, t is the epoch number.


- [x] Weights are pushed toward becoming smaller (closer to 0)
- [ ] Weights are pushed toward becoming bigger (further from 0)
- [ ] Doubling lambda should roughly result in doubling the weights
- [ ] Gradient descent taking bigger steps with each iteration (proportional to lambda)


#### 7. You use an exponentially weighted average on the London temperature dataset. You use the following to track the temperature: v_{t} = \beta v_{t-1} + (1-\beta)\theta_tv 
t
​	 =βv 
t−1
​	 +(1−β)θ 
t
​	 . The red line below was computed using \beta = 0.9β=0.9. What would happen to your red curve as you vary \betaβ? (Check the two that apply)

- [ ] You apply dropout (randomly eliminating units) but keep the 1/keep_prob factor in the calculations used in training.
- [x] You do not apply dropout (do not randomly eliminate units) and do not keep the 1/keep_prob factor in the calculations used in training
- [ ] You do not apply dropout (do not randomly eliminate units), but keep the 1/keep_prob factor in the calculations used in training.
- [ ] You apply dropout (randomly eliminating units) and do not keep the 1/keep_prob factor in the calculations used in training


#### 8. Consider this figure:

- [ ] Increasing the regularization effect
- [x] Reducing the regularization effect
- [ ] Causing the neural network to end up with a higher training set error
- [x] Causing the neural network to end up with a lower training set error


#### 9.Suppose batch gradient descent in a deep network is taking excessively long to find a value of the parameters that achieves a small value for the cost function J(W[1],b[1],...,W[L],b[L]). Which of the following techniques could help find parameter values that attain a small value forJ? (Check all that apply)

- [ ] Gradient Checking
- [ ] Xavier initialization
- [ ] Vanishing gradient
- [x] Dropout
- [x] L2 regularization
- [ ] Exploding gradient
- [x] Data augmentation


#### 10. Which of the following statements about Adam is False?

- [ ] It makes the parameter initialization faster
- [ ] It makes it easier to visualize the data
- [x] It makes the cost function faster to optimize
- [ ] Normalization is another word for regularization--It helps to reduce variance
