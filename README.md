Run with:

THEANO_FLAGS=mode=FAST_RUN,device=gpu,floatX=float32 python model.py

Reads in Cifar data data from Keras.  To replace training data, X_train, Y_train, X_test, Y_test should be replaced.

X_train should be a numpy matrix of stacked vectors with final shape of:

(# of samples, 3 (for rgb), height of individual image, width of image)

Y_train and Y_test will be converted to a matrix of stacked binary vectors that will match the expected output of the network.  This is what happens in keras.np_utils.to_categorcial

e.g:

5 classes - Y_train = [[0, 0, 0, 0, 1],    # representing 5th class
                       [0, 1, 0, 0, 0],    # representing 2nd class
                       [0, 0, 1, 0, 0]]    # representing 3rd class