## Week 2 Quiz - Autonomous driving (case study)


#### 1.To help you practice strategies for machine learning, in this week we’ll present another scenario and ask how you would act. We think this “simulator” of working in a machine learning project will give a task of what leading a machine learning project could be like!

- [ ] Spend a few days checking what is human-level performance for these tasks so that you can get an accurate estimate of Bayes error.
- [x] Spend a few days training a basic model and see what mistakes it makes.
- [ ] Spend a few days getting the internet data, so that you understand better what data is available.
- [ ] Spend a few days collecting more data using the front-facing camera of your car, to better understand how much data per unit time you can collect.


#### 2.Your goal is to detect road signs (stop sign, pedestrian crossing sign, construction ahead sign) and traffic signals (red and green lights) in images. The goal is to recognize which of these objects appear in each image. You plan to use a deep neural network with ReLU units in the hidden layers.

- [ ] True
- [x] False

#### 3. You are carrying out error analysis and counting up what errors the algorithm makes. Which of these datasets do you think you should manually go through and carefully examine, one image at a time?

- [ ] 10,000 images on which the algorithm made a mistake
- [x] 500 images on which the algorithm made a mistake
- [ ] 10,000 randomly chosen images
- [ ] 500 randomly chosen images


#### 4. After working on the data for several weeks, your team ends up with the following data:

- [ ] True
- [x] False


#### 5. The distribution of data you care about contains images from your car’s front-facing camera; which comes from a different distribution than the images you were able to find and download off the internet. How should you split the dataset into train/dev/test sets?

- [x] Choose the training set to be the 900,000 images from the internet along with 80,000 images from your car’s front-facing camera. The 20,000 remaining images will be split equally in dev and test sets.
- [ ] Mix all the 100,000 images with the 900,000 images you found online. Shuffle everything. Split the 1,000,000 images dataset into 600,000 for the training set, 200,000 for the dev set and 200,000 for the test set.
- [ ] Mix all the 100,000 images with the 900,000 images you found online. Shuffle everything. Split the 1,000,000 images dataset into 980,000 for the training set, 10,000 for the dev set and 10,000 for the test set.
- [ ] Choose the training set to be the 900,000 images from the internet along with 20,000 images from your car’s front-facing camera. The 80,000 remaining images will be split equally in dev and test sets.


#### 6. Assume you’ve finally chosen the following split between of the data:

- [ ] Your algorithm overfits the dev set because the error of the dev and test sets are very close.
- [ ] You have a large variance problem because your model is not generalizing well to data from the same training distribution but that it has never seen before.
- [x] You have a large avoidable-bias problem because your training error is quite a bit higher than the human-level error.
- [x] You have a large data-mismatch problem because your model does a lot better on the training-dev set than on the dev set
- [ ] You have a large variance problem because your training error is quite higher than the human-level error.


#### 7. Based on table from the previous question, a friend thinks that the training data distribution is much easier than the dev/test distribution. What do you think?

- [ ] Your friend is right. (I.e., Bayes error for the training data distribution is probably lower than for the dev/test distribution.)
- [ ] Your friend is wrong. (I.e., Bayes error for the training data distribution is probably higher than for the dev/test distribution.)
- [x] There’s insufficient information to tell if your friend is right or wrong.


#### 8. You decide to focus on the dev set and check by hand what are the errors due to. Here is a table summarizing your discoveries:

- [ ] True because it is the largest category of errors. As discussed in lecture, we should prioritize the largest category of error to avoid wasting the team’s time.
- [ ] True because it is greater than the other error categories added together (8.0 > 4.1+2.2+1.0).
- [x] False because this would depend on how easy it is to add this data and how much you think your team thinks it’ll help.
- [ ] False because data augmentation (synthesizing foggy images by clean/non-foggy images) is more efficient.


#### 9. You can buy a specially designed windshield wiper that help wipe off some of the raindrops on the front-facing camera. Based on the table from the previous question, which of the following statements do you agree with?

- [x] 2.2% would be a reasonable estimate of the maximum amount this windshield wiper could improve performance.
- [ ] 2.2% would be a reasonable estimate of the minimum amount this windshield wiper could improve performance.
- [ ] 2.2% would be a reasonable estimate of how much this windshield wiper will improve performance.
- [ ] 2.2% would be a reasonable estimate of how much this windshield wiper could worsen performance in the worst case.


#### 10. You decide to use data augmentation to address foggy images. You find 1,000 pictures of fog off the internet, and “add” them to clean images to synthesize foggy days, like this:


- [ ] Adding synthesized images that look like real foggy pictures taken from the front-facing camera of your car to training dataset won’t help the model improve because it will introduce avoidable-bias.
- [x] There is little risk of overfitting to the 1,000 pictures of fog so long as you are combing it with a much larger (>>1,000) of clean/non-foggy images.
- [x] So long as the synthesized fog looks realistic to the human eye, you can be confident that the synthesized data is accurately capturing the distribution of real foggy images (or a subset of it), since human vision is very accurate for the problem you’re solving.



#### 11. After working further on the problem, you’ve decided to correct the incorrectly labeled data on the dev set. Which of these statements do you agree with? (Check all that apply).

- [x] You should also correct the incorrectly labeled data in the test set, so that the dev and test sets continue to come from the same distribution
- [ ] You should correct incorrectly labeled data in the training set as well so as to avoid your training set now being even more different from your dev set.
- [x] You should not correct the incorrectly labeled data in the test set, so that the dev and test sets continue to come from the same distribution
- [ ] You should not correct incorrectly labeled data in the training set as it does not worth the time.



#### 12. So far your algorithm only recognizes red and green traffic lights. One of your colleagues in the startup is starting to work on recognizing a yellow traffic light. (Some countries call it an orange light rather than a yellow light; we’ll use the US convention of calling it yellow.) Images containing yellow lights are quite rare, and she doesn’t have enough data to build a good model. She hopes you can help her out using transfer learning.

#### What do you tell your colleague?

- [x] She should try using weights pre-trained on your dataset, and fine-tuning further with the yellow-light dataset.
- [ ] If she has (say) 10,000 images of yellow lights, randomly sample 10,000 images from your dataset and put your and her data together. This prevents your dataset from “swamping” the yellow lights dataset.
- [ ] You cannot help her because the distribution of data you have is different from hers, and is also lacking the yellow label.
- [ ] Recommend that she try multi-task learning instead of transfer learning using all the data.


#### 13. Another colleague wants to use microphones placed outside the car to better hear if there’re other vehicles around you. For example, if there is a police vehicle behind you, you would be able to hear their siren. However, they don’t have much to train this audio system. How can you help?

- [ ] Transfer learning from your vision dataset could help your colleague get going faster. Multi-task learning seems significantly less promising.
- [ ] Multi-task learning from your vision dataset could help your colleague get going faster. Transfer learning seems significantly less promising.
- [ ] Either transfer learning or multi-task learning could help our colleague get going faster.
- [x] Neither transfer learning nor multi-task learning seems promising.


#### 14. To recognize red and green lights, you have been using this approach:

- [ ] True
- [x] False


#### 15. Approach A (in the question above) tends to be more promising than approach B if you have a ________ (fill in the blank).

- [x] Large training set
- [ ] Multi-task learning problem.
- [ ] Large bias problem.
- [ ] Problem with a high Bayes error.



