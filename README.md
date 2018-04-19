# What-is-Tensorflow?
Brief description on Tensorflow library and its functionalities..

Tensoflow is a Machine Learning Library which was made public by Google on 9th November 2015, www.tensorflow.org gets you to their official website. The Tensorflow has made machine learning very easy by contibuting many API's which do the whole task of manuel programming.

# Terminologies

1. Dataset     - Collection of data for training and testing.
2. Train       - Run the dataset over a function(y = m\*x + c) so called model.
3. Weights     - Values of 'm' in the above function are known as weights.
4. Bias        - Values of 'c' in the above function are known as bias.
5. Model/Graph - It is the output obtained after training over train dataset.
6. Evaluate    - Evaluate the model on the basis of a testing dataset.
7. Predict     - Predict a value of 'y' for a given x using the model parameters such as (weights)'m' and (biases)'c'.
8. tf          - After importing the Tensorflow library( import tensorflow as tf ) tf - represents tensorflow.

# Tensorflow Variables

1. Tensorflow Variable : as the name suggest, used for declaring some variables in tensorflow programming, mainly used in declaring Weights and Bias in building a model. Where they needs to be changed according to each iteration. 
Eg : a = tf.Varaible(0.0, dtype=tf.float32, name='weights')

2. Tensorflow Placeholders : they are used to hold up some values, mostly used to place values of training and testing dataset.
Eg : a = tf.placeholder(dtype=tf.float32, name='train_data')

3. Tensorflow Constants : used to declare a constant.
Eg : a = tf.constant(1.0, dtype=tf.float32, name='constant_bias')

There are a lot more but to run a simple model these are more than enough.

# Tensorflow Session

The above variables are declared and these don't work as the same variables as that of python, so we need to initialize them in a tensorflow Session and then perform operations on the variable within the tensorflow session.

1. Start Session as : sess = tf.Session(), initialize the session to 'sess' variable

2. Initializes all the varialbles : sess.run(tf.global_variables_initializer())

3. Get the value printed for a variable : sess.run(tf.constant(1, dtype=tf.int32)) prints 1

4. close session after operations : sess.close(), frees all resources associated with the session.

# Simple Program to ADD two numbers in tensorflow

import tensorflow as tf \
a = tf.constant(1, dtype=tf.int32) # declaring variable 'a' as tf.int32(tensorflow datatype) \
b = tf.constant(2, dtype=tf.int32) # declaring variable 'b' as tf.int32(tensorflow datatype) \
c = a + b # automatic declaration of 'c' according to variable type of 'a' and 'b' \
sess = tf.Session() # Starts the tensorflow session. \
sess.run(tf.global_variables_initializer()) -- it works even without this \
print(sess.run(c)) # to obtain value of 'c' it should be run with a session. \
sess.run(tf.add(a, b)) # same as above, used tensorflow build-in fumction for add. \

Value of 'c' is printed as 3. Hurray..!! you have done you very first Tensorflow program.

# Use-Case Challenge

1. Feed your daily activity data to a model as training dataset, like what all you did in every hour of a week, and the model could predict what you will be doing the next week at any day for any hour..

2. Feed stock price or bitcoin price for a while and make out if the price are going down or up in the comming weeks \
don't think hard.. you will be able to do that in weeks.. Happy Learning ;)

# For Next

So now you must have got a vague picture of how Tensorflow works, don't worry stay tuned, this is just like an ice-burg, there is much more to jump deep.. now on, we will be using the above terminologies and standards to design our model. From next tutorials, we will start building exciting models, suggest me some good use-case and we will try makeing it a model that could predict your need. \

Please share your comments and keep me posted for any doubts and updates.
