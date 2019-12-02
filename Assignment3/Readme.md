## <u>Assignment 3</u>

## <u>Advanced Convolutions, Batch Normalization & Receptive field</u>

### <u>Task</u>
	The task is to write a DNN for the CIFAR-10 dataset satisfying the following conditions

1. Use depthwise separable convolution only
2. Use BatchNormalization
3. Use less than 100000 parameters
4. Use proper dropout values
5. o/p size of each layer
6. receptive field of each layer
7. 50 epochs
8. Beat base validation accuracy

### <u>Base validation accuracy</u>
Highest - 82.8
At 50th epoch - 82.02

## <u>Achieved Results:</u><u></u>

## <u>Highest validation accuracy</u> - 83.6%

## <u>Number of parameters</u> - 94, 911

================================================================

### <u>Base validation log</u>

390/390 [===] - 17s 43ms/step - loss: 1.8323 - acc: 0.3050 - val_loss: 1.3921 - val_acc: 0.4895
Epoch 2/50
390/390 [===] - 7s 19ms/step - loss: 1.3237 - acc: 0.5231 - val_loss: 1.1247 - val_acc: 0.5865
Epoch 3/50
390/390 [===] - 7s 19ms/step - loss: 1.1088 - acc: 0.6082 - val_loss: 0.9720 - val_acc: 0.6589
Epoch 4/50
390/390 [===] - 7s 19ms/step - loss: 0.9564 - acc: 0.6660 - val_loss: 0.8204 - val_acc: 0.7124
Epoch 5/50
390/390 [===] - 7s 19ms/step - loss: 0.8632 - acc: 0.7015 - val_loss: 0.7705 - val_acc: 0.7326
Epoch 6/50
390/390 [===] - 7s 19ms/step - loss: 0.7857 - acc: 0.7313 - val_loss: 0.7657 - val_acc: 0.7453
Epoch 7/50
390/390 [===] - 7s 19ms/step - loss: 0.7355 - acc: 0.7494 - val_loss: 0.6982 - val_acc: 0.7637
Epoch 8/50
390/390 [===] - 7s 19ms/step - loss: 0.6848 - acc: 0.7656 - val_loss: 0.6992 - val_acc: 0.7661
Epoch 9/50
390/390 [===] - 7s 19ms/step - loss: 0.6589 - acc: 0.7771 - val_loss: 0.6536 - val_acc: 0.7775
Epoch 10/50
390/390 [====] - 8s 19ms/step - loss: 0.6215 - acc: 0.7883 - val_loss: 0.6232 - val_acc: 0.7911
Epoch 11/50
390/390 [===] - 8s 19ms/step - loss: 0.5974 - acc: 0.7949 - val_loss: 0.6565 - val_acc: 0.7843
Epoch 12/50
390/390 [===] - 7s 19ms/step - loss: 0.5776 - acc: 0.8050 - val_loss: 0.5955 - val_acc: 0.8042
Epoch 13/50
390/390 [===] - 7s 19ms/step - loss: 0.5565 - acc: 0.8092 - val_loss: 0.6088 - val_acc: 0.7988
Epoch 14/50
390/390 [===] - 7s 19ms/step - loss: 0.5440 - acc: 0.8150 - val_loss: 0.5925 - val_acc: 0.8087
Epoch 15/50
390/390 [===] - 8s 19ms/step - loss: 0.5147 - acc: 0.8225 - val_loss: 0.5864 - val_acc: 0.8050
Epoch 16/50
390/390 [===] - 7s 19ms/step - loss: 0.5018 - acc: 0.8285 - val_loss: 0.5980 - val_acc: 0.8000
Epoch 17/50
390/390 [===] - 7s 19ms/step - loss: 0.4900 - acc: 0.8338 - val_loss: 0.6142 - val_acc: 0.7978
Epoch 18/50
390/390 [===] - 7s 19ms/step - loss: 0.4879 - acc: 0.8326 - val_loss: 0.5790 - val_acc: 0.8109
Epoch 19/50
390/390 [===] - 8s 19ms/step - loss: 0.4728 - acc: 0.8372 - val_loss: 0.5861 - val_acc: 0.8117
Epoch 20/50
390/390 [===] - 7s 19ms/step - loss: 0.4655 - acc: 0.8413 - val_loss: 0.5906 - val_acc: 0.8107
Epoch 21/50
390/390 [===] - 7s 19ms/step - loss: 0.4576 - acc: 0.8436 - val_loss: 0.5989 - val_acc: 0.8099
Epoch 22/50
390/390 [===] - 7s 19ms/step - loss: 0.4462 - acc: 0.8468 - val_loss: 0.5781 - val_acc: 0.8186
Epoch 23/50
390/390 [===] - 8s 19ms/step - loss: 0.4370 - acc: 0.8512 - val_loss: 0.5878 - val_acc: 0.8109
Epoch 24/50
390/390 [===] - 7s 19ms/step - loss: 0.4295 - acc: 0.8532 - val_loss: 0.5819 - val_acc: 0.8124
Epoch 25/50
390/390 [===] - 8s 19ms/step - loss: 0.4177 - acc: 0.8555 - val_loss: 0.6060 - val_acc: 0.8167
Epoch 26/50
390/390 [===] - 7s 19ms/step - loss: 0.4128 - acc: 0.8600 - val_loss: 0.5624 - val_acc: 0.8189
Epoch 27/50
390/390 [===] - 8s 19ms/step - loss: 0.4046 - acc: 0.8620 - val_loss: 0.6209 - val_acc: 0.8071
Epoch 28/50
390/390 [===] - 8s 19ms/step - loss: 0.4093 - acc: 0.8604 - val_loss: 0.5818 - val_acc: 0.8199
Epoch 29/50
390/390 [===] - 7s 19ms/step - loss: 0.3992 - acc: 0.8641 - val_loss: 0.5813 - val_acc: 0.8185
Epoch 30/50
390/390 [===] - 7s 19ms/step - loss: 0.3926 - acc: 0.8663 - val_loss: 0.5741 - val_acc: 0.8222
Epoch 31/50
390/390 [===] - 7s 19ms/step - loss: 0.3880 - acc: 0.8689 - val_loss: 0.5779 - val_acc: 0.8234
Epoch 32/50
390/390 [===] - 8s 19ms/step - loss: 0.3887 - acc: 0.8691 - val_loss: 0.5833 - val_acc: 0.8229
Epoch 33/50
390/390 [===] - 7s 19ms/step - loss: 0.3743 - acc: 0.8721 - val_loss: 0.6228 - val_acc: 0.8116
Epoch 34/50
390/390 [===] - 7s 19ms/step - loss: 0.3723 - acc: 0.8717 - val_loss: 0.5700 - val_acc: 0.8245
Epoch 35/50
390/390 [===] - 7s 19ms/step - loss: 0.3696 - acc: 0.8745 - val_loss: 0.5684 - val_acc: 0.8270
Epoch 36/50
390/390 [===] - 7s 19ms/step - loss: 0.3580 - acc: 0.8776 - val_loss: 0.5982 - val_acc: 0.8193
Epoch 37/50
390/390 [===] - 8s 19ms/step - loss: 0.3605 - acc: 0.8797 - val_loss: 0.5798 - val_acc: 0.8201
Epoch 38/50
390/390 [===] - 8s 19ms/step - loss: 0.3620 - acc: 0.8785 - val_loss: 0.5709 - val_acc: 0.8227
Epoch 39/50
390/390 [===] - 7s 19ms/step - loss: 0.3457 - acc: 0.8830 - val_loss: 0.5766 - val_acc: 0.8239
Epoch 40/50
390/390 [===] - 8s 19ms/step - loss: 0.3429 - acc: 0.8846 - val_loss: 0.5924 - val_acc: 0.8222
Epoch 41/50
390/390 [===] - 7s 19ms/step - loss: 0.3491 - acc: 0.8814 - val_loss: 0.6263 - val_acc: 0.8138
Epoch 42/50
390/390 [===] - 7s 19ms/step - loss: 0.3503 - acc: 0.8832 - val_loss: 0.5754 - val_acc: 0.8280
Epoch 43/50
390/390 [===] - 8s 19ms/step - loss: 0.3425 - acc: 0.8851 - val_loss: 0.6340 - val_acc: 0.8144
Epoch 44/50
390/390 [===] - 7s 19ms/step - loss: 0.3295 - acc: 0.8884 - val_loss: 0.5992 - val_acc: 0.8227
Epoch 45/50
390/390 [===] - 7s 19ms/step - loss: 0.3457 - acc: 0.8843 - val_loss: 0.6166 - val_acc: 0.8227
Epoch 46/50
390/390 [===] - 7s 19ms/step - loss: 0.3314 - acc: 0.8884 - val_loss: 0.5777 - val_acc: 0.8277
Epoch 47/50
390/390 [===] - 7s 19ms/step - loss: 0.3282 - acc: 0.8883 - val_loss: 0.5860 - val_acc: 0.8287
Epoch 48/50
390/390 [===] - 7s 19ms/step - loss: 0.3237 - acc: 0.8916 - val_loss: 0.6032 - val_acc: 0.8194
Epoch 49/50
390/390 [===] - 7s 19ms/step - loss: 0.3208 - acc: 0.8918 - val_loss: 0.6173 - val_acc: 0.8185
Epoch 50/50
390/390 [===] - 7s 19ms/step - loss: 0.3163 - acc: 0.8934 - val_loss: 0.5985 - val_acc: 0.8202


# <u>Submission</u>
## <u>Model Definition</u>
~~~python
model = Sequential()

model.add(SeparableConv2D(32, 3, 3, border_mode='same', input_shape=(32, 32, 3), use_bias = False, kernel_initializer='he_uniform'))	# o/p channel size - 32x32x32; Receptive field - 1x1
model.add(BatchNormalization())
model.add(Activation('relu'))
model.add(SeparableConv2D(64, 3, 3, border_mode='same', use_bias = False, kernel_initializer='he_uniform'))		# o/p channel size - 32x32x64; Receptive field - 3x3
model.add(BatchNormalization())
model.add(Activation('relu'))
model.add(MaxPooling2D(pool_size=(2, 2)))		# o/p channel size - 16x16x64; Receptive field - 4x4
model.add(Dropout(0.15))


model.add(SeparableConv2D(128, 3, 3, border_mode='same', use_bias = False, kernel_initializer='he_uniform'))	# o/p channel size - 16x16x128; Receptive field - 8x8
model.add(BatchNormalization())
model.add(Activation('relu'))
model.add(SeparableConv2D(156, 3, 3, border_mode='same', use_bias = False, kernel_initializer='he_uniform'))	# o/p channel size - 16x16x156; Receptive field - 12x12
model.add(BatchNormalization())
model.add(Activation('relu'))
model.add(MaxPooling2D(pool_size=(2, 2)))	# o/p channel size - 8x8x156; Receptive field - 14x14
model.add(Dropout(0.2))

model.add(SeparableConv2D(168, 3, 3, border_mode='same', use_bias = False, kernel_initializer='he_uniform'))	# o/p channel size - 8x8x168; Receptive field - 22x22
model.add(BatchNormalization())
model.add(Activation('relu'))
model.add(MaxPooling2D(pool_size=(2, 2)))	# o/p channel size - 4x4x168; Receptive field - 26x26
model.add(Dropout(0.25))

model.add(SeparableConv2D(168, 1, 1, activation='relu', use_bias = False, kernel_initializer='he_uniform'))		# o/p channel size - 4x4x168; Receptive field - 26x26
model.add(SeparableConv2D(10, 4, use_bias = False))		# o/p channel size - 1x1x10; Receptive field - 50x50
model.add(GlobalAveragePooling2D())
model.add(Activation('softmax'))
~~~
### <u>model summary</u>
Layer (type)                 Output Shape              Param #   
------------------------------------------------------------------------------

separable_conv2d_309 ||(Separa (None, 32, 32, 32)     ||   123       
_________________________________________________________________
batch_normalization_273 ||(Bat (None, 32, 32, 32)    ||    128       
_________________________________________________________________
activation_318 (Activation) || (None, 32, 32, 32)    ||    0         
_________________________________________________________________
separable_conv2d_310 (Separa ||(None, 32, 32, 64)     ||   2336      
_________________________________________________________________
batch_normalization_274 (Bat ||(None, 32, 32, 64)    ||    256       
_________________________________________________________________
activation_319 (Activation)  ||(None, 32, 32, 64)   ||     0         ||
_________________________________________________________________
max_pooling2d_139 (MaxPoolin ||(None, 16, 16, 64)     ||   0         
_________________________________________________________________
dropout_131 (Dropout)     ||   (None, 16, 16, 64)    ||    0         
_________________________________________________________________
separable_conv2d_311 (Separa ||(None, 16, 16, 128)    ||   8768      
_________________________________________________________________
batch_normalization_275 (Bat ||(None, 16, 16, 128)    ||   512       
_________________________________________________________________
activation_320 (Activation) || (None, 16, 16, 128)   ||    0         
_________________________________________________________________
separable_conv2d_312|| (Separa (None, 16, 16, 156)   ||    21120     
_________________________________________________________________
batch_normalization_276 ||(Bat (None, 16, 16, 156)    ||   624||       
_________________________________________________________________
activation_321 (Activation)  ||(None, 16, 16, 156)   ||    0         
_________________________________________________________________
max_pooling2d_140 (MaxPoolin ||(None, 8, 8, 156)    ||     0         
_________________________________________________________________
dropout_132 (Dropout)     ||   (None, 8, 8, 156)    ||     0         
_________________________________________________________________
separable_conv2d_313 (Separa ||(None, 8, 8, 168)     ||    27612     
_________________________________________________________________
batch_normalization_277 ||(Bat (None, 8, 8, 168)     ||    672       
_________________________________________________________________
activation_322 (Activation) || (None, 8, 8, 168)   ||      0         
_________________________________________________________________
max_pooling2d_141 ||(MaxPoolin (None, 4, 4, 168)    ||     0         
_________________________________________________________________
dropout_133 (Dropout)    ||    (None, 4, 4, 168)      ||   0         
_________________________________________________________________
separable_conv2d_314 (Separa|| (None, 4, 4, 168)     ||    28392     
_________________________________________________________________
separable_conv2d_315 (Separa|| (None, 1, 1, 10)    ||      4368      
_________________________________________________________________
global_average_pooling2d_44  ||(None, 10)      ||          0         
_________________________________________________________________
activation_323 (Activation) || (None, 10)       ||         0  

--------------------------------------------------------------------------------
Total params: 94,911
Trainable params: 93,815
Non-trainable params: 1,096

### <u>Logs for the above model</u>
Epoch 1/50
390/390 [===] - 21s 54ms/step - loss: 1.3401 - acc: 0.5057 - val_loss: 1.6467 - val_acc: 0.4922
Epoch 2/50
390/390 [===] - 9s 24ms/step - loss: 0.9615 - acc: 0.6573 - val_loss: 1.1378 - val_acc: 0.6191
Epoch 3/50
390/390 [===] - 9s 24ms/step - loss: 0.8244 - acc: 0.7094 - val_loss: 1.0727 - val_acc: 0.6537
Epoch 4/50
390/390 [===] - 10s 24ms/step - loss: 0.7441 - acc: 0.7394 - val_loss: 0.8274 - val_acc: 0.7158
Epoch 5/50
390/390 [===] - 10s 25ms/step - loss: 0.6849 - acc: 0.7583 - val_loss: 0.9204 - val_acc: 0.6853
Epoch 6/50
390/390 [===] - 9s 24ms/step - loss: 0.6412 - acc: 0.7748 - val_loss: 0.8220 - val_acc: 0.7204
Epoch 7/50
390/390 [===] - 9s 24ms/step - loss: 0.6163 - acc: 0.7812 - val_loss: 0.7285 - val_acc: 0.7516
Epoch 8/50
390/390 [===] - 9s 24ms/step - loss: 0.5879 - acc: 0.7944 - val_loss: 0.7470 - val_acc: 0.7503
Epoch 9/50
390/390 [===] - 9s 24ms/step - loss: 0.5578 - acc: 0.8042 - val_loss: 0.9077 - val_acc: 0.7066
Epoch 10/50
390/390 [===] - 9s 24ms/step - loss: 0.5391 - acc: 0.8112 - val_loss: 0.6696 - val_acc: 0.7796
Epoch 11/50
390/390 [===] - 10s 25ms/step - loss: 0.5250 - acc: 0.8169 - val_loss: 0.6082 - val_acc: 0.7857
Epoch 12/50
390/390 [===] - 10s 24ms/step - loss: 0.5074 - acc: 0.8222 - val_loss: 0.6360 - val_acc: 0.7894
Epoch 13/50
390/390 [===] - 10s 24ms/step - loss: 0.4919 - acc: 0.8270 - val_loss: 0.5977 - val_acc: 0.7961
Epoch 14/50
390/390 [===] - 10s 24ms/step - loss: 0.4815 - acc: 0.8301 - val_loss: 0.6555 - val_acc: 0.7826
Epoch 15/50
390/390 [===] - 9s 24ms/step - loss: 0.4759 - acc: 0.8327 - val_loss: 0.5595 - val_acc: 0.8090
Epoch 16/50
390/390 [===] - 10s 24ms/step - loss: 0.4593 - acc: 0.8375 - val_loss: 0.6417 - val_acc: 0.7920
Epoch 17/50
390/390 [===] - 9s 24ms/step - loss: 0.4511 - acc: 0.8413 - val_loss: 0.6587 - val_acc: 0.7779
Epoch 18/50
390/390 [===] - 9s 24ms/step - loss: 0.4477 - acc: 0.8429 - val_loss: 0.6506 - val_acc: 0.7889
Epoch 19/50
390/390 [===] - 10s 25ms/step - loss: 0.4387 - acc: 0.8458 - val_loss: 0.5983 - val_acc: 0.8039
Epoch 20/50
390/390 [===] - 9s 24ms/step - loss: 0.4267 - acc: 0.8474 - val_loss: 0.6198 - val_acc: 0.8013
Epoch 21/50
390/390 [===] - 9s 24ms/step - loss: 0.4222 - acc: 0.8507 - val_loss: 0.5459 - val_acc: 0.8161
Epoch 22/50
390/390 [===] - 10s 24ms/step - loss: 0.4169 - acc: 0.8514 - val_loss: 0.5804 - val_acc: 0.8139
Epoch 23/50
390/390 [===] - 9s 24ms/step - loss: 0.4076 - acc: 0.8566 - val_loss: 0.6385 - val_acc: 0.7904
Epoch 24/50
390/390 [===] - 9s 24ms/step - loss: 0.3947 - acc: 0.8597 - val_loss: 0.5602 - val_acc: 0.8102
Epoch 25/50
390/390 [===] - 9s 24ms/step - loss: 0.3956 - acc: 0.8614 - val_loss: 0.5916 - val_acc: 0.8042
Epoch 26/50
390/390 [===] - 9s 24ms/step - loss: 0.3832 - acc: 0.8652 - val_loss: 0.5614 - val_acc: 0.8185
Epoch 27/50
390/390 [===] - 10s 25ms/step - loss: 0.3883 - acc: 0.8635 - val_loss: 0.5395 - val_acc: 0.8230
Epoch 28/50
390/390 [===] - 9s 24ms/step - loss: 0.3802 - acc: 0.8650 - val_loss: 0.5950 - val_acc: 0.8138
Epoch 29/50
390/390 [===] - 9s 24ms/step - loss: 0.3793 - acc: 0.8657 - val_loss: 0.6317 - val_acc: 0.7905
Epoch 30/50
390/390 [===] - 9s 24ms/step - loss: 0.3732 - acc: 0.8666 - val_loss: 0.5330 - val_acc: 0.8290
Epoch 31/50
390/390 [===] - 10s 24ms/step - loss: 0.3623 - acc: 0.8706 - val_loss: 0.5750 - val_acc: 0.8132
Epoch 32/50
390/390 [===] - 9s 24ms/step - loss: 0.3649 - acc: 0.8695 - val_loss: 0.5627 - val_acc: 0.8200
Epoch 33/50
390/390 [===] - 9s 24ms/step - loss: 0.3580 - acc: 0.8742 - val_loss: 0.5452 - val_acc: 0.8256
Epoch 34/50
390/390 [===] - 10s 25ms/step - loss: 0.3562 - acc: 0.8726 - val_loss: 0.6776 - val_acc: 0.7867
Epoch 35/50
390/390 [===] - 10s 24ms/step - loss: 0.3538 - acc: 0.8744 - val_loss: 0.5835 - val_acc: 0.8109
Epoch 36/50
390/390 [===] - 9s 24ms/step - loss: 0.3493 - acc: 0.8741 - val_loss: 0.5497 - val_acc: 0.8193
Epoch 37/50
390/390 [===] - 10s 25ms/step - loss: 0.3428 - acc: 0.8779 - val_loss: 0.5550 - val_acc: 0.8213
Epoch 38/50
390/390 [===] - 9s 24ms/step - loss: 0.3427 - acc: 0.8772 - val_loss: 0.5270 - val_acc: 0.8293
Epoch 39/50
390/390 [===] - 9s 24ms/step - loss: 0.3378 - acc: 0.8798 - val_loss: 0.5384 - val_acc: 0.8215
Epoch 40/50
390/390 [===] - 10s 25ms/step - loss: 0.3311 - acc: 0.8826 - val_loss: 0.5676 - val_acc: 0.8243
Epoch 41/50
390/390 [===] - 9s 24ms/step - loss: 0.3427 - acc: 0.8764 - val_loss: 0.5415 - val_acc: 0.8254
Epoch 42/50
390/390 [===] - 9s 24ms/step - loss: 0.3294 - acc: 0.8828 - val_loss: 0.5372 - val_acc: 0.8304
Epoch 43/50
390/390 [===] - 10s 25ms/step - loss: 0.3357 - acc: 0.8789 - val_loss: 0.5061 - val_acc: 0.8360
Epoch 44/50
390/390 [===] - 9s 24ms/step - loss: 0.3221 - acc: 0.8841 - val_loss: 0.5886 - val_acc: 0.8239
Epoch 45/50
390/390 [===] - 10s 24ms/step - loss: 0.3280 - acc: 0.8825 - val_loss: 0.5303 - val_acc: 0.8315
Epoch 46/50
390/390 [===] - 10s 24ms/step - loss: 0.3170 - acc: 0.8870 - val_loss: 0.5553 - val_acc: 0.8275
Epoch 47/50
390/390 [===] - 10s 24ms/step - loss: 0.3213 - acc: 0.8857 - val_loss: 0.5379 - val_acc: 0.8266
Epoch 48/50
390/390 [===] - 10s 25ms/step - loss: 0.3183 - acc: 0.8852 - val_loss: 0.5860 - val_acc: 0.8172
Epoch 49/50
390/390 [===] - 9s 24ms/step - loss: 0.3152 - acc: 0.8874 - val_loss: 0.5296 - val_acc: 0.8323
Epoch 50/50
390/390 [===] - 9s 24ms/step - loss: 0.3076 - acc: 0.8908 - val_loss: 0.5614 - val_acc: 0.8263
Model took 487.21 seconds to train

## <u>Highest validation accuracy - 83.6%</u>
## <u>Number of parameters - 94, 911</u>
