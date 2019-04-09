## Week 1 Quiz - Optimization algorithms


#### 1.Which notation would you use to denote the 3rd layer’s activations when the input is the 7th example from the 8th minibatch?

- [ ] a <sup>[8]{3}(7)
- [ ] a <sup>[3]{7}(8)
- [ ] a <sup>[8]{7}(3)
- [x] a <sup>[3]{8}(7)


#### 2.Which of these statements about mini-batch gradient descent do you agree with?

- [ ] You should implement mini-batch gradient descent without an explicit for-loop over different mini-batches, so that the algorithm processes all mini-batches at the same time (vectorization).
- [x] One iteration of mini-batch gradient descent (computing on a single mini-batch) is faster than one iteration of batch gradient descent.
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
- [ ] Whether you’re using batch gradient descent or mini-batch gradient descent, this looks acceptable.
- [ ] Whether you’re using batch gradient descent or mini-batch gradient descent, something is wrong.


#### 5.Suppose the temperature in Casablanca over the first three days of January are the same:

- [x] v<sub>2</sub>=7.5, v<sub>2</sub><sup>corrected</sup> = 10
- [ ] v<sub>2</sub>=10, v<sub>2</sub><sup>corrected</sup> = 7.5
- [ ] v<sub>2</sub>=10, v<sub>2</sub><sup>corrected</sup> = 10
- [ ] v<sub>2</sub>=7.5, v<sub>2</sub><sup>corrected</sup> = 7.5

#### 6.Which of these is NOT a good learning rate decay scheme? Here, t is the epoch number.


- [x] α=e<sup>t</sup>α<sub>0</sub>	



#### 7. You use an exponentially weighted average on the London temperature dataset. You use the following to track the temperature: v_{t} = \beta v_{t-1} + (1-\beta)\theta_tv 


- [ ] Decreasing β will shift the red line slightly to the right.
- [x] Increasing β will shift the red line slightly to the right.
- [x] Decreasing β will create more oscillation within the red line.
- [ ] Increasing β will create more oscillations within the red line.


#### 8. Consider this figure:

- [x] (1) is gradient descent. (2) is gradient descent with momentum (small β). (3) is gradient descent with momentum (large β)
- [ ] (1) is gradient descent with momentum (small β), (2) is gradient descent with momentum (small β), (3) is gradient descent
- [ ] (1) is gradient descent. (2) is gradient descent with momentum (large β) . (3) is gradient descent with momentum (small β)
- [ ] (1) is gradient descent with momentum (small β). (2) is gradient descent. (3) is gradient descent with momentum (large β)


#### 9.Suppose batch gradient descent in a deep network is taking excessively long to find a value of the parameters that achieves a small value for the cost function J(W[1],b[1],...,W[L],b[L]). Which of the following techniques could help find parameter values that attain a small value forJ? (Check all that apply)

- [ ] Try initializing all the weights to zero
- [x] Try mini-batch gradient descent
- [x] Try better random initialization for the weights
- [x] Try using Adam
- [x] Try tuning the learning rate α


#### 10. Which of the following statements about Adam is False?

- [x] Adam should be used with batch gradient computations, not with mini-batches.
- [ ] We usually use “default” values for the hyperparameters β1,β2 and ε in Adam (β1 = 0.9, β2 =0.999, ε=10<sup>−8</sup>)
- [ ] Adam combines the advantages of RMSProp and momentum
- [ ] The learning rate hyperparameter α in Adam usually needs to be tuned.
