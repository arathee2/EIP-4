# base model accuracy
0.8290

# my model definition

my_model = Sequential()
my_model.add(SeparableConv2D(48, 3, 3, activation='relu', input_shape=(32, 32, 3))) # (30, 3)
my_model.add(BatchNormalization())
my_model.add(Dropout(0.1))

my_model.add(SeparableConv2D(96, kernel_size = (3, 3), strides=(2, 2), activation='relu')) # (14, 5)
my_model.add(BatchNormalization())
my_model.add(Dropout(0.15))

my_model.add(SeparableConv2D(48, 3, 3, activation='relu')) # (12, 7)
my_model.add(BatchNormalization())
my_model.add(Dropout(0.15))

my_model.add(SeparableConv2D(96, 3, 3, activation='relu')) # (10, 11)
my_model.add(BatchNormalization())
my_model.add(Dropout(0.15))

my_model.add(SeparableConv2D(96, 3, 3, activation='relu')) # (8, 15)
my_model.add(BatchNormalization())
my_model.add(Dropout(0.15))

my_model.add(SeparableConv2D(96, kernel_size = (3, 3), strides=(2, 2), activation='relu')) # (3, 19)
my_model.add(BatchNormalization())
my_model.add(Dropout(0.15))

my_model.add(SeparableConv2D(192, 3, 3, activation='relu')) # (1, 23)
my_model.add(BatchNormalization())
my_model.add(Dropout(0.15))

my_model.add(SeparableConv2D(num_classes, 1, 1, activation='relu')) # (1, 23)
my_model.add(BatchNormalization())

my_model.add(Flatten())
my_model.add(Activation('softmax')) #(1, 23)


lr_reducer = ReduceLROnPlateau(factor=np.sqrt(0.1), cooldown=0, patience=2, min_lr=0.1e-6)


my_model.compile(optimizer='adam', loss='categorical_crossentropy', metrics=['accuracy'])



# model log

390/390 [==============================] - 23s 59ms/step - loss: 1.8721 - acc: 0.2761 - val_loss: 1.4198 - val_acc: 0.4710
Epoch 2/50
390/390 [==============================] - 20s 51ms/step - loss: 1.3461 - acc: 0.5100 - val_loss: 1.1519 - val_acc: 0.5843
Epoch 3/50
390/390 [==============================] - 20s 51ms/step - loss: 1.1030 - acc: 0.6095 - val_loss: 0.9154 - val_acc: 0.6794
Epoch 4/50
390/390 [==============================] - 20s 51ms/step - loss: 0.9455 - acc: 0.6707 - val_loss: 0.8912 - val_acc: 0.7000
Epoch 5/50
390/390 [==============================] - 20s 51ms/step - loss: 0.8625 - acc: 0.7029 - val_loss: 0.7615 - val_acc: 0.7369
Epoch 6/50
390/390 [==============================] - 20s 51ms/step - loss: 0.7909 - acc: 0.7303 - val_loss: 0.7276 - val_acc: 0.7538
Epoch 7/50
390/390 [==============================] - 20s 51ms/step - loss: 0.7386 - acc: 0.7468 - val_loss: 0.6675 - val_acc: 0.7704
Epoch 8/50
390/390 [==============================] - 20s 51ms/step - loss: 0.6991 - acc: 0.7620 - val_loss: 0.6757 - val_acc: 0.7769
Epoch 9/50
390/390 [==============================] - 20s 51ms/step - loss: 0.6621 - acc: 0.7754 - val_loss: 0.7041 - val_acc: 0.7652
Epoch 10/50
390/390 [==============================] - 20s 51ms/step - loss: 0.6316 - acc: 0.7848 - val_loss: 0.6250 - val_acc: 0.7863
Epoch 11/50
390/390 [==============================] - 20s 51ms/step - loss: 0.6159 - acc: 0.7909 - val_loss: 0.6285 - val_acc: 0.7882
Epoch 12/50
390/390 [==============================] - 20s 51ms/step - loss: 0.5936 - acc: 0.7987 - val_loss: 0.6064 - val_acc: 0.7952
Epoch 13/50
390/390 [==============================] - 20s 51ms/step - loss: 0.5716 - acc: 0.8051 - val_loss: 0.6337 - val_acc: 0.7846
Epoch 14/50
390/390 [==============================] - 20s 51ms/step - loss: 0.5563 - acc: 0.8107 - val_loss: 0.5895 - val_acc: 0.8036
Epoch 15/50
390/390 [==============================] - 20s 51ms/step - loss: 0.5317 - acc: 0.8213 - val_loss: 0.5807 - val_acc: 0.8076
Epoch 16/50
390/390 [==============================] - 20s 51ms/step - loss: 0.5190 - acc: 0.8228 - val_loss: 0.5935 - val_acc: 0.8049
Epoch 17/50
390/390 [==============================] - 20s 51ms/step - loss: 0.5025 - acc: 0.8278 - val_loss: 0.6088 - val_acc: 0.8033
Epoch 18/50
390/390 [==============================] - 20s 51ms/step - loss: 0.5005 - acc: 0.8296 - val_loss: 0.5867 - val_acc: 0.8025
Epoch 19/50
390/390 [==============================] - 20s 50ms/step - loss: 0.4920 - acc: 0.8323 - val_loss: 0.5890 - val_acc: 0.8055
Epoch 20/50
390/390 [==============================] - 20s 51ms/step - loss: 0.4771 - acc: 0.8370 - val_loss: 0.5949 - val_acc: 0.8086
Epoch 21/50
390/390 [==============================] - 20s 51ms/step - loss: 0.4712 - acc: 0.8396 - val_loss: 0.5889 - val_acc: 0.8064
Epoch 22/50
390/390 [==============================] - 20s 52ms/step - loss: 0.4490 - acc: 0.8450 - val_loss: 0.5761 - val_acc: 0.8158
Epoch 23/50
390/390 [==============================] - 20s 51ms/step - loss: 0.4482 - acc: 0.8468 - val_loss: 0.5739 - val_acc: 0.8160
Epoch 24/50
390/390 [==============================] - 20s 51ms/step - loss: 0.4456 - acc: 0.8487 - val_loss: 0.5568 - val_acc: 0.8209
Epoch 25/50
390/390 [==============================] - 20s 51ms/step - loss: 0.4395 - acc: 0.8510 - val_loss: 0.5808 - val_acc: 0.8168
Epoch 26/50
390/390 [==============================] - 20s 50ms/step - loss: 0.4251 - acc: 0.8561 - val_loss: 0.5904 - val_acc: 0.8134
Epoch 27/50
390/390 [==============================] - 20s 51ms/step - loss: 0.4236 - acc: 0.8582 - val_loss: 0.5907 - val_acc: 0.8091
Epoch 28/50
390/390 [==============================] - 20s 50ms/step - loss: 0.4168 - acc: 0.8571 - val_loss: 0.5814 - val_acc: 0.8134
Epoch 29/50
390/390 [==============================] - 20s 50ms/step - loss: 0.4142 - acc: 0.8588 - val_loss: 0.5996 - val_acc: 0.8178
Epoch 30/50
390/390 [==============================] - 20s 51ms/step - loss: 0.4054 - acc: 0.8606 - val_loss: 0.5604 - val_acc: 0.8209
Epoch 31/50
390/390 [==============================] - 20s 51ms/step - loss: 0.3887 - acc: 0.8667 - val_loss: 0.5542 - val_acc: 0.8213
Epoch 32/50
390/390 [==============================] - 20s 51ms/step - loss: 0.3867 - acc: 0.8693 - val_loss: 0.5851 - val_acc: 0.8171
Epoch 33/50
390/390 [==============================] - 20s 51ms/step - loss: 0.3931 - acc: 0.8660 - val_loss: 0.5601 - val_acc: 0.8254
Epoch 34/50
390/390 [==============================] - 20s 51ms/step - loss: 0.3865 - acc: 0.8674 - val_loss: 0.5569 - val_acc: 0.8264
Epoch 35/50
390/390 [==============================] - 20s 51ms/step - loss: 0.3807 - acc: 0.8717 - val_loss: 0.5785 - val_acc: 0.8229
Epoch 36/50
390/390 [==============================] - 20s 51ms/step - loss: 0.3824 - acc: 0.8710 - val_loss: 0.5728 - val_acc: 0.8285
Epoch 37/50
390/390 [==============================] - 20s 51ms/step - loss: 0.3784 - acc: 0.8723 - val_loss: 0.5534 - val_acc: 0.8249
Epoch 38/50
390/390 [==============================] - 20s 51ms/step - loss: 0.3636 - acc: 0.8779 - val_loss: 0.5751 - val_acc: 0.8200
Epoch 39/50
390/390 [==============================] - 20s 51ms/step - loss: 0.3691 - acc: 0.8764 - val_loss: 0.5872 - val_acc: 0.8197
Epoch 40/50
390/390 [==============================] - 20s 51ms/step - loss: 0.3648 - acc: 0.8777 - val_loss: 0.5824 - val_acc: 0.8224
Epoch 41/50
390/390 [==============================] - 20s 51ms/step - loss: 0.3619 - acc: 0.8780 - val_loss: 0.5847 - val_acc: 0.8230
Epoch 42/50
390/390 [==============================] - 20s 51ms/step - loss: 0.3457 - acc: 0.8811 - val_loss: 0.5817 - val_acc: 0.8227
Epoch 43/50
390/390 [==============================] - 20s 51ms/step - loss: 0.3445 - acc: 0.8832 - val_loss: 0.5721 - val_acc: 0.8217
Epoch 44/50
390/390 [==============================] - 20s 51ms/step - loss: 0.3455 - acc: 0.8837 - val_loss: 0.5522 - val_acc: 0.8265
Epoch 45/50
390/390 [==============================] - 20s 51ms/step - loss: 0.3472 - acc: 0.8816 - val_loss: 0.5758 - val_acc: 0.8266
Epoch 46/50
390/390 [==============================] - 20s 51ms/step - loss: 0.3430 - acc: 0.8856 - val_loss: 0.5961 - val_acc: 0.8224
Epoch 47/50
390/390 [==============================] - 20s 51ms/step - loss: 0.3366 - acc: 0.8871 - val_loss: 0.6032 - val_acc: 0.8173
Epoch 48/50
390/390 [==============================] - 20s 51ms/step - loss: 0.3416 - acc: 0.8850 - val_loss: 0.5757 - val_acc: 0.8251
Epoch 49/50
390/390 [==============================] - 20s 50ms/step - loss: 0.3342 - acc: 0.8880 - val_loss: 0.5823 - val_acc: 0.8260
Epoch 50/50
390/390 [==============================] - 20s 50ms/step - loss: 0.3232 - acc: 0.8905 - val_loss: 0.5718 - val_acc: 0.8290
Model took 994.94 seconds to train

