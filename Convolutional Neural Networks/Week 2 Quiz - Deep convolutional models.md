## Week 2 Quiz - Deep convolutional models


#### 1. Which of the following do you typically see as you move to deeper layers in a ConvNet?

- [x] n<sub>H</sub> and n<sub>W</sub> decreases, while n<sub>C</sub> increases
- [ ] n<sub>H</sub> and n<sub>W</sub> increases, while n<sub>C</sub> increases
- [ ] n<sub>H</sub> and n<sub>W</sub> increases, while n<sub>C</sub> decreases
- [ ] n<sub>H</sub> and n<sub>W</sub> decrease, while n<sub>C</sub> decreases


#### 2. Which of the following do you typically see in a ConvNet? (Check all that apply.)


- [x] Multiple CONV layers followed by a POOL layer
- [ ] Multiple POOL layers followed by a CONV layer
- [x] FC layers in the last few layers
- [ ] FC layers in the first few layers



#### 3. In order to be able to build very deep networks, we usually only use pooling layers to downsize the height/width of the activation volumes while convolutions are used with “valid” padding. Otherwise, we would downsize the input of the model too quickly.

- [ ] True
- [x] False



#### 4. Training a deeper network (for example, adding additional layers to the network) allows the network to fit more complex functions and thus almost always results in lower training error. For this question, assume we’re referring to “plain” networks.

- [ ] True
- [x] False



#### 5. The following equation captures the computation in a ResNet block. What goes into the two blanks above?
#### a<sup>[l+2]</sup> = g(W<sup>[l+2]</sup>g(W<sup>[l+1]</sup>a<sup>l</sup> + b<sup>[l+1]) + b<sup>[l+2] + ________) +________

- [ ] z<sup>[l]</sup> and a<sup>[l]</sup>, respectively
- [ ] 0 and z<sup>[l]</sup>, respectively
- [ ] 0 and a<sup>[l]</sup>, respectively
- [x] a<sup>[l]</sup> and 0, respectively



#### 6. Which ones of the following statements on Residual Networks are true? (Check all that apply.)

- [x] The skip-connections compute a complex non-linear function of the input to pass to a deeper layer in the network.
- [ ] A ResNet with L layers would have on the order of L<sup>2</sup> skip connections in total.
- [ ] The skip-connection makes it easy for the network to learn an identity mapping between the input and the output within the ResNet block.
- [x] Using a skip-connection helps the gradient to backpropagate and thus helps you to train deeper networks



#### 7. Suppose you have an input volume of dimension 64x64x16. How many parameters would a single 1x1 convolutional filter have (including the bias)?


- [ ] 4097
- [ ] 2
- [ ] 1
- [x] 17


#### 8. Suppose you have an input volume of dimension n<sub>H</sub> x n<sub>W</sub> x n<sub>C</sub>. Which of the following statements you agree with? (Assume that “1x1 convolutional layer” below always uses a stride of 1 and no padding.)

- [x] You can use a pooling layer to reduce n<sub>H</sub>, n<sub>W</sub>, but not n<sub>C</sub>.
- [] You can use a pooling layer to reduce  n<sub>H</sub>, n<sub>W</sub>, and n<sub>C</sub>.
- [ ] You can use a 1x1 convolutional layer to reduce  n<sub>H</sub>, n<sub>W</sub>, and n<sub>C</sub>.
- [x] You can use a 1x1 convolutional layer to reduce n<sub>C</sub>>, but not n<sub>H</sub>, n<sub>W</sub



#### 9. Which ones of the following statements on Inception Networks are true? (Check all that apply.)

- [ ] Inception networks incorporates a variety of network architectures (similar to dropout, which randomly chooses a network architecture on each step) and thus has a similar regularizing effect as dropout.
- [x] A single inception block allows the network to use a combination of 1x1, 3x3, 5x5 convolutions and pooling.
- [ ] Making an inception network deeper (by stacking more inception blocks together) should not hurt training set performance.
- [x] Inception blocks usually use 1x1 convolutions to reduce the input data volume’s size before applying 3x3 and 5x5 convolutions.



#### 10. Which of the following are common reasons for using open-source implementations of ConvNets (both the model and/or weights)? Check all that apply.

- [x] It is a convenient way to get working an implementation of a complex ConvNet architecture.
- [x] Parameters trained for one computer vision task are often useful as pretraining for other computer vision tasks.
- [ ] The same techniques for winning computer vision competitions, such as using multiple crops at test time, are widely used in practical deployments (or production system deployments) of ConvNets.
- [ ] A model trained for one computer vision task can usually be used to perform data augmentation even for a different computer vision task.

