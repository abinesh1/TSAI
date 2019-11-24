# EIP 4 - Assignment 2

### 9th DNN

model.evaluate Accuracy attained - 99.4%
model max Accuracy attained - 99.51%
Number of parameters -15,712 [15,448+264]
Number of epochs - 20

No fully connected layers were used.
No biases we used in conv layers.

#### model.evaluate on test data = 99.4

### Strategy Used

Followed instructor's code till 8th DNN

Made the following changes
 - separated the 1x1 conv layer in the second block
 - increased the dropout rate of later layers
 - Replaced flatten layer with GlabalAveragePooling2D
 - increased the learning rate of the optimizer

### Network architecture

model = Sequential()

model.add(Convolution2D(16, 3, 3, activation='relu', input_shape=(28,28,1), use_bias = False)) #26
model.add(BatchNormalization())
model.add(Dropout(0.1))

model.add(Convolution2D(32, 3, 3, activation='relu', use_bias = False)) #24
model.add(BatchNormalization())
model.add(Dropout(0.1))

model.add(Convolution2D(10, 1, 1, activation='relu', use_bias = False)) #22

model.add(MaxPooling2D(pool_size=(2, 2)))#11

model.add(Convolution2D(16, 3, 3, activation='relu', use_bias = False))#9
model.add(BatchNormalization())
model.add(Dropout(0.1))


model.add(Convolution2D(16, 3, 3, activation='relu', use_bias = False))#7
model.add(BatchNormalization())
model.add(Dropout(0.1))


model.add(Convolution2D(16, 3, 3, activation='relu', use_bias = False))#5
model.add(BatchNormalization())
model.add(Dropout(0.1))


model.add(Convolution2D(16, 3, 3, activation='relu', use_bias = False))#3
model.add(BatchNormalization())
model.add(Dropout(0.15))

model.add(Convolution2D(10, 1, 1, activation='relu', use_bias = False))#3
model.add(BatchNormalization())
model.add(Dropout(0.15))

model.add(Convolution2D(10, 4, use_bias = False))
model.add(BatchNormalization())
model.add(Dropout(0.15))

model.add(GlobalAveragePooling2D())
#model.add(Flatten())
model.add(Activation('softmax'))

### Logs

Train on 60000 samples, validate on 10000 samples
Epoch 1/20

Epoch 00001: LearningRateScheduler setting learning rate to 0.003.
60000/60000 [==============================] - 26s 437us/step - loss: 0.6267 - acc: 0.8189 - val_loss: 0.1113 - val_acc: 0.9783
Epoch 2/20

Epoch 00002: LearningRateScheduler setting learning rate to 0.0022744503.
60000/60000 [==============================] - 13s 223us/step - loss: 0.2791 - acc: 0.9139 - val_loss: 0.0667 - val_acc: 0.9870
Epoch 3/20

Epoch 00003: LearningRateScheduler setting learning rate to 0.0018315018.
60000/60000 [==============================] - 13s 217us/step - loss: 0.2209 - acc: 0.9335 - val_loss: 0.0481 - val_acc: 0.9880
Epoch 4/20

Epoch 00004: LearningRateScheduler setting learning rate to 0.0015329586.
60000/60000 [==============================] - 13s 220us/step - loss: 0.1874 - acc: 0.9404 - val_loss: 0.0544 - val_acc: 0.9864
Epoch 5/20

Epoch 00005: LearningRateScheduler setting learning rate to 0.0013181019.
60000/60000 [==============================] - 13s 217us/step - loss: 0.1703 - acc: 0.9444 - val_loss: 0.0378 - val_acc: 0.9909
Epoch 6/20

Epoch 00006: LearningRateScheduler setting learning rate to 0.0011560694.
60000/60000 [==============================] - 13s 220us/step - loss: 0.1547 - acc: 0.9474 - val_loss: 0.0343 - val_acc: 0.9925
Epoch 7/20

Epoch 00007: LearningRateScheduler setting learning rate to 0.0010295127.
60000/60000 [==============================] - 13s 222us/step - loss: 0.1426 - acc: 0.9489 - val_loss: 0.0331 - val_acc: 0.9922
Epoch 8/20

Epoch 00008: LearningRateScheduler setting learning rate to 0.0009279307.
60000/60000 [==============================] - 13s 224us/step - loss: 0.1366 - acc: 0.9512 - val_loss: 0.0275 - val_acc: 0.9923
Epoch 9/20

Epoch 00009: LearningRateScheduler setting learning rate to 0.0008445946.
60000/60000 [==============================] - 13s 218us/step - loss: 0.1306 - acc: 0.9505 - val_loss: 0.0252 - val_acc: 0.9931
Epoch 10/20

Epoch 00010: LearningRateScheduler setting learning rate to 0.0007749935.
60000/60000 [==============================] - 13s 217us/step - loss: 0.1208 - acc: 0.9536 - val_loss: 0.0219 - val_acc: 0.9937
Epoch 11/20

Epoch 00011: LearningRateScheduler setting learning rate to 0.0007159905.
60000/60000 [==============================] - 13s 218us/step - loss: 0.1190 - acc: 0.9538 - val_loss: 0.0255 - val_acc: 0.9926
Epoch 12/20

Epoch 00012: LearningRateScheduler setting learning rate to 0.000665336.
60000/60000 [==============================] - 13s 216us/step - loss: 0.1142 - acc: 0.9544 - val_loss: 0.0224 - val_acc: 0.9937
Epoch 13/20

Epoch 00013: LearningRateScheduler setting learning rate to 0.0006213753.
60000/60000 [==============================] - 13s 219us/step - loss: 0.1135 - acc: 0.9541 - val_loss: 0.0236 - val_acc: 0.9924
Epoch 14/20

Epoch 00014: LearningRateScheduler setting learning rate to 0.0005828638.
60000/60000 [==============================] - 13s 215us/step - loss: 0.1101 - acc: 0.9549 - val_loss: 0.0233 - val_acc: 0.9935
Epoch 15/20

Epoch 00015: LearningRateScheduler setting learning rate to 0.0005488474.
60000/60000 [==============================] - 13s 218us/step - loss: 0.1066 - acc: 0.9563 - val_loss: 0.0200 - val_acc: 0.9941
Epoch 16/20

Epoch 00016: LearningRateScheduler setting learning rate to 0.0005185825.
60000/60000 [==============================] - 13s 215us/step - loss: 0.1056 - acc: 0.9555 - val_loss: 0.0193 - val_acc: 0.9953
Epoch 17/20

Epoch 00017: LearningRateScheduler setting learning rate to 0.000491481.
60000/60000 [==============================] - 13s 214us/step - loss: 0.1052 - acc: 0.9556 - val_loss: 0.0228 - val_acc: 0.9925
Epoch 18/20

Epoch 00018: LearningRateScheduler setting learning rate to 0.0004670715.
60000/60000 [==============================] - 13s 215us/step - loss: 0.1008 - acc: 0.9568 - val_loss: 0.0185 - val_acc: 0.9951
Epoch 19/20

Epoch 00019: LearningRateScheduler setting learning rate to 0.0004449718.
60000/60000 [==============================] - 13s 220us/step - loss: 0.1006 - acc: 0.9560 - val_loss: 0.0193 - val_acc: 0.9948
Epoch 20/20

Epoch 00020: LearningRateScheduler setting learning rate to 0.000424869.
60000/60000 [==============================] - 13s 217us/step - loss: 0.0993 - acc: 0.9575 - val_loss: 0.0221 - val_acc: 0.9940