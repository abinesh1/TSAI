##Assignment 1

#### MNIST 99% accuracy

The accuracy on the test set attained by changing the model architecture is 99.12%

The model is as follows

'''
model = Sequential()
model.add(Convolution2D(32, 3, activation='relu', input_shape = (28,28,1)))
model.add(MaxPooling2D(2))
model.add(BatchNormalization())
model.add(Convolution2D(64, 3, activation='relu'))
model.add(MaxPooling2D(2))
model.add(Dropout(0.5))
model.add(BatchNormalization())
model.add(Convolution2D(10, 1, activation='relu'))
model.add(Convolution2D(10, 5, name = 'conv2d_14'))
model.add(Flatten())
model.add(Activation('softmax'))
'''


####Descriptive writeup

*Convolution*
It is the process of convolving a filter/window over an image to extract features and create a feature map.

*Filter/Kernel*
A filter is a matrix of randomly initialised weights which convolve on an input image. The matrix represents a feature such as edges or curved lines. Typical filters used are 3x3, 5x5, 7x7

*Epochs*
Epochs represents the number of times that the model looks through the entire training dataset.

*1x1 convolution*
1x1 convolutions are used to either increase or decrease the filter size. This is largely helpful to decrease the numberof parameters when decreasing the filter size, thus speeding up training.

*3x3 convolution*
A 3x3 convolution is the most commonly used filter. When a 3x3 with no padding is used, it reduces the image dimension by 2.

*Feature map*
A feature map is a filter containing relevant features that is obtained by combining the results of the features extracted by the kernels by convolving on top of the image.

*Activation function*
An activation function is one where the output is triggered based onthe input. Relu, sigmoid, elu are some of the activation functions

*Receptive field*
It refers to the area or the pixels in the image the a kernel looks at during a convolution operation.
