## Week 1 Quiz - Bird recognition in the city of Peacetopia (case study)


#### 1. Problem Statement
#### This example is adapted from a real production application, but with details disguised to protect confidentiality.
- [x] True
- [ ] False


#### 2. After further discussions, the city narrows down its criteria to:

- [ ] Test Accuracy : 97%, Runtime : 3 sec, Memory suze : 2MB
- [x] Test Accuracy : 98%, Runtime : 9 sec, Memory suze : 9MB

#### 3. Based on the city’s requests, which of the following would you say is true?

- [x] Accuracy is an optimizing metric; running time and memory size are a satisficing metrics.
- [ ] Accuracy is a satisficing metric; running time and memory size are an optimizing metric.
- [ ] Accuracy, running time and memory size are all optimizing metrics because you want to do well on all three.
- [ ] Accuracy, running time and memory size are all satisficing metrics because you have to do sufficiently well on all three for your system to be acceptable.

#### 4. Structuring your data
####Before implementing your algorithm, you need to split your data into train/dev/test sets. Which of these do you think is the best choice?

- [ ] Train : 6,000,000 Dev : 3,000,000 Test : 1,000,000
- [ ] Train : 6,000,000 Dev : 1,000,000 Test : 3,000,000
- [x] Train : 9,500,000 Dev : 2,500,000 Test : 2,500,000
- [ ] Train : 3,333,334 Dev : 3,333,333 Test : 3,333,333


#### 5. After setting up your train/dev/test sets, the City Council comes across another 1,000,000 images, called the “citizens’ data”. Apparently the citizens of Peacetopia are so scared of birds that they volunteered to take pictures of the sky and label them, thus contributing these additional 1,000,000 images. These images are different from the distribution of images the City Council had originally given you, but you think it could help your algorithm.

- [ ] True
- [x] False

#### 6. One member of the City Council knows a little about machine learning, and thinks you should add the 1,000,000 citizens’ data images to the test set. You object because:


- [x] This would cause the dev and test set distributions to become different. This is a bad idea because you’re not aiming where you want to hit.
- [ ] A bigger test set will slow down the speed of iterating because of the computational expense of evaluating models on the test set.
- [x] The test set no longer reflects the distribution of data (security cameras) you most care about.
- [ ] The 1,000,000 citizens’ data images do not have a consistent x-->y mapping as the rest of the data (similar to the New York City/Detroit housing prices example from lecture).


#### 7. You train a system, and its errors are as follows (error = 100%-Accuracy):

- [ ] Yes, because having 4.0% training error shows you have high bias.
- [ ] Yes, because this shows your bias is higher than your variance.
- [ ] No, because this shows your variance is higher than your bias.
- [x] No, because there is insufficient information to tell.


#### 8. You ask a few people to label the dataset so as to find out what is human-level performance. You find the following levels of accuracy:


- [ ] 0.0% (because it is impossible to do better than this)
- [x] 0.3% (accuracy of expert #1)
- [ ] 0.4% (average of 0.3 and 0.5)
- [ ] 0.75% (average of all four numbers above)


#### 9. Which of the following statements do you agree with?

- [x] A learning algorithm’s performance can be better than human-level performance but it can never be better than Bayes error.
- [ ] A learning algorithm’s performance can never be better than human-level performance but it can be better than Bayes error.
- [ ] A learning algorithm’s performance can never be better than human-level performance nor better than Bayes error.
- [ ] A learning algorithm’s performance can be better than human-level performance and better than Bayes error.


#### 10. You find that a team of ornithologists debating and discussing an image gets an even better 0.1% performance, so you define that as “human-level performance.” After working further on your algorithm, you end up with the following:


- [ ] Try increasing regularization.
- [x] Train a bigger model to try to do better on the training set.
- [x] Try decreasing regularization.
- [ ] Get a bigger training set to reduce variance.


#### 11. You also evaluate your model on the test set, and find the following:
#### What does this mean? (Check the two best options.)

- [ ] You have overfit to the dev set.
- [x] You have underfit to the dev set.
- [x] You should try to get a bigger dev
- [x] You should get a bigger test set.


#### 12. After working on this project for a year, you finally achieve:
#### What can you conclude? (Check all that apply.)


- [x] If the test set is big enough for the 0.05% error estimate to be accurate, this implies Bayes error is ≤0.05
- [x] It is now harder to measure avoidable bias, thus progress will be slower going forward.
- [ ] With only 0.09% further progress to make, you should quickly be able to close the remaining gap to 0%
- [ ] This is a statistical anomaly (or must be the result of statistical noise) since it should not be possible to surpass human-level performance.



#### 13. It turns out Peacetopia has hired one of your competitors to build a system as well. Your system and your competitor both deliver systems with about the same running time and memory size. However, your system has higher accuracy! However, when Peacetopia tries out your and your competitor’s systems, they conclude they actually like your competitor’s system better, because even though you have higher overall accuracy, you have more false negatives (failing to raise an alarm when a bird is in the air). What should you do?


- [ ] Look at all the models you’ve developed during the development process and find the one with the lowest false negative error rate.- [x] It is now harder to measure avoidable bias, thus progress will be slower going forward.
- [ ] Ask your team to take into account both accuracy and false negative rate during development.
- [x] Rethink the appropriate metric for this task, and ask your team to tune to the new metric.
- [ ] Pick false negative rate as the new metric, and use this new metric to drive all further development.


#### 14. You’ve handily beaten your competitor, and your system is now deployed in Peacetopia and is protecting the citizens from birds! But over the last few months, a new species of bird has been slowly migrating into the area, so the performance of your system slowly degrades because your data is being tested on a new type of data.
#### You have only 1,000 images of the new species of bird. The city expects a better system from you within the next 3 months. Which of these should you do first?

- [x] Use the data you have to define a new evaluation metric (using a new dev/test set) taking into account the new species, and use that to drive further progress for your team.
- [ ] Put the 1,000 images into the training set so as to try to do better on these birds.
- [ ] Try data augmentation/data synthesis to get more images of the new type of bird.
- [ ] Add the 1,000 images into your dataset and reshuffle into a new train/dev/test split.


#### 15. The City Council thinks that having more Cats in the city would help scare off birds. They are so happy with your work on the Bird detector that they also hire you to build a Cat detector. (Wow Cat detectors are just incredibly useful aren’t they.) Because of years of working on Cat detectors, you have such a huge dataset of 100,000,000 cat images that training on this data takes about two weeks. Which of the statements do you agree with? (Check all that agree.)


- [x] Needing two weeks to train will limit the speed at which you can iterate.
- [ ] Having built a good Bird detector, you should be able to take the same model and hyperparameters and just apply it to the Cat dataset, so there is no need to iterate.
- [x] If 100,000,000 examples is enough to build a good enough Cat detector, you might be better of training with just 10,000,000 examples to gain a \approx≈10x improvement in how quickly you can run experiments, even if each model performs a bit worse because it’s trained on less data.
- [x] Buying faster computers could speed up your teams’ iteration speed and thus your team’s productivity.
- [ ] Look at all the models you’ve developed during the development process and find the one with the lowest false negative error rate.- [x] It is now harder to measure avoidable bias, thus progress will be slower going forward.




