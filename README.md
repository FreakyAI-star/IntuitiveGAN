# What is GAN?
**GAN** stands for Generative Adversarial Networks. These kinds of networks are used for developing synthetic data generation. It combines two different models to achieve this task namely Generator and Discriminator models:- 

### Generator model
Generator models try to learn how to make a realistic representation of some class. They take input as noise which represents a random set of values going into the generative model. The generative model also sometimes takes input as a class Y. From these inputs, its goal is to generate a set of features X that look realistic. The noise is introduced to ensure that what's generated isn't actually the same dog each time and you'll see this theme play out shortly. More generally, generative models try to capture the probability distribution of the set of features X of a class Y. With the added noise, these models would generate realistic and diverse representations of this class Y. If we're generating only one class then we don't need this conditioning on Y and instead, it's just the probability over all the features X. Some of the most popular generative models are: **VAE** and **GAN**.

### Discriminator model
A discriminative model is one typically used for classification in machine learning. These try to model the probability of class Y given a set of features X.

