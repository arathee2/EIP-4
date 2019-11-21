# logs

Train on 60000 samples, validate on 10000 samples
Epoch 1/20

Epoch 00001: LearningRateScheduler setting learning rate to 0.003.
60000/60000 [==============================] - 19s 322us/step - loss: 0.0641 - acc: 0.9806 - val_loss: 0.0499 - val_acc: 0.9849
Epoch 2/20

Epoch 00002: LearningRateScheduler setting learning rate to 0.0022744503.
60000/60000 [==============================] - 7s 118us/step - loss: 0.0527 - acc: 0.9836 - val_loss: 0.0348 - val_acc: 0.9890
Epoch 3/20

Epoch 00003: LearningRateScheduler setting learning rate to 0.0018315018.
60000/60000 [==============================] - 7s 117us/step - loss: 0.0455 - acc: 0.9867 - val_loss: 0.0354 - val_acc: 0.9899
Epoch 4/20

Epoch 00004: LearningRateScheduler setting learning rate to 0.0015329586.
60000/60000 [==============================] - 7s 120us/step - loss: 0.0440 - acc: 0.9870 - val_loss: 0.0306 - val_acc: 0.9917
Epoch 5/20

Epoch 00005: LearningRateScheduler setting learning rate to 0.0013181019.
60000/60000 [==============================] - 7s 118us/step - loss: 0.0396 - acc: 0.9888 - val_loss: 0.0259 - val_acc: 0.9922
Epoch 6/20

Epoch 00006: LearningRateScheduler setting learning rate to 0.0011560694.
60000/60000 [==============================] - 7s 119us/step - loss: 0.0395 - acc: 0.9884 - val_loss: 0.0296 - val_acc: 0.9906
Epoch 7/20

Epoch 00007: LearningRateScheduler setting learning rate to 0.0010295127.
60000/60000 [==============================] - 7s 117us/step - loss: 0.0356 - acc: 0.9899 - val_loss: 0.0269 - val_acc: 0.9927
Epoch 8/20

Epoch 00008: LearningRateScheduler setting learning rate to 0.0009279307.
60000/60000 [==============================] - 7s 117us/step - loss: 0.0364 - acc: 0.9892 - val_loss: 0.0238 - val_acc: 0.9930
Epoch 9/20

Epoch 00009: LearningRateScheduler setting learning rate to 0.0008445946.
60000/60000 [==============================] - 7s 119us/step - loss: 0.0341 - acc: 0.9899 - val_loss: 0.0224 - val_acc: 0.9935
Epoch 10/20

Epoch 00010: LearningRateScheduler setting learning rate to 0.0007749935.
60000/60000 [==============================] - 7s 118us/step - loss: 0.0317 - acc: 0.9907 - val_loss: 0.0230 - val_acc: 0.9935
Epoch 11/20

Epoch 00011: LearningRateScheduler setting learning rate to 0.0007159905.
60000/60000 [==============================] - 7s 122us/step - loss: 0.0322 - acc: 0.9906 - val_loss: 0.0215 - val_acc: 0.9935
Epoch 12/20

Epoch 00012: LearningRateScheduler setting learning rate to 0.000665336.
60000/60000 [==============================] - 7s 119us/step - loss: 0.0305 - acc: 0.9910 - val_loss: 0.0212 - val_acc: 0.9935
Epoch 13/20

Epoch 00013: LearningRateScheduler setting learning rate to 0.0006213753.
60000/60000 [==============================] - 7s 121us/step - loss: 0.0299 - acc: 0.9916 - val_loss: 0.0204 - val_acc: 0.9944
Epoch 14/20

Epoch 00014: LearningRateScheduler setting learning rate to 0.0005828638.
60000/60000 [==============================] - 7s 119us/step - loss: 0.0302 - acc: 0.9912 - val_loss: 0.0192 - val_acc: 0.9943
Epoch 15/20

Epoch 00015: LearningRateScheduler setting learning rate to 0.0005488474.
60000/60000 [==============================] - 7s 117us/step - loss: 0.0285 - acc: 0.9910 - val_loss: 0.0213 - val_acc: 0.9941
Epoch 16/20

Epoch 00016: LearningRateScheduler setting learning rate to 0.0005185825.
60000/60000 [==============================] - 7s 119us/step - loss: 0.0268 - acc: 0.9919 - val_loss: 0.0191 - val_acc: 0.9943
Epoch 17/20

Epoch 00017: LearningRateScheduler setting learning rate to 0.000491481.
60000/60000 [==============================] - 7s 118us/step - loss: 0.0268 - acc: 0.9923 - val_loss: 0.0184 - val_acc: 0.9946
Epoch 18/20

Epoch 00018: LearningRateScheduler setting learning rate to 0.0004670715.
60000/60000 [==============================] - 7s 123us/step - loss: 0.0285 - acc: 0.9914 - val_loss: 0.0192 - val_acc: 0.9952
Epoch 19/20

Epoch 00019: LearningRateScheduler setting learning rate to 0.0004449718.
60000/60000 [==============================] - 7s 120us/step - loss: 0.0254 - acc: 0.9926 - val_loss: 0.0198 - val_acc: 0.9941
Epoch 20/20

Epoch 00020: LearningRateScheduler setting learning rate to 0.000424869.
60000/60000 [==============================] - 7s 116us/step - loss: 0.0262 - acc: 0.9923 - val_loss: 0.0195 - val_acc: 0.9942
<keras.callbacks.History at 0x7fdd55696c88>


# accuracy on test set

0.9942

# strategy
1. Used global max pooling instead of fully connected layer in the end.
2. Removed biases from each layer.
3. Total number of parameters used = 13100.
4. Changed the learning rate to 0.0045.