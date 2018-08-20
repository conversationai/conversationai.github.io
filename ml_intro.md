[Back to Conversation AI Research Overview](index.md)

## A quick introduction to Machine Learning

To get involved, it's helpful to understand some of the core topics and terminology in the Machine Learning (typically abbreviated to just ML). This is a short introduction to the branch ML we use.

Machine learning is about getting computers to learn patterns. For example, we might try to get a computer to learning to predict a person's height from their weight. A machine learning algorithm would do this by finding a pattern between people's heights and weights.

Unlike traditional programs which after being written only carry out the instructions of the programmer, machine learning programs are first written, but then trained on examples, and only then are they ready to run. When they are run, they get to use the knowledge they learned from the training examples. The knowledge they picked up from those examples is called a 'model'.

One of the most popular paradigms in machine learning is called supervised learning. The machine learning algorithm is given training examples (e.g. a person's weight) and for each one it is asked to predict the correct answer (e.g. the person's height). When the program gets the answer wrong, it's model (the knowledge it has so far) is updated so it is more likely to get the answer right next time.

A popular approach to this learning is called neural networks because it is (loosely) inspired by how the brain works. Lets walk through a small example to illustrate the idea. The job of the machine learning programmer is to write a network (also sometimes called a network topology) which describes how the knowledge in a model is used to decide the output. For our example of predicting a person's height from their weight, the model might consist of two numbers: x1 and x2, and a person's height might be computed by (x1 * weight) + x2. The machine then learns roughly like this: each time the program over-estimates a person's height, it decreases x1 and x2 (each time by different small amounts, defined by something called the derivative). And each time it underestimates their height, they are increased (also each time by different small amounts). An important quantity that defines how much x1 and x2 are changed by is called the learning rate. This is important. If it is too small, it can take a very long time to learn. If it is too high, then the over-and under-estimates for the person's height can become wildly increasingly wrong, instead of better. A lot of machine learning research goes into designing the neural network for machine learning and how to get a good learning rate.

This kind of supervised machine learning using neural networks is the primary way we train models for the Perspective API.

Now you've read this, you might enjoy reading about [bias in machine learning](bias.md).
