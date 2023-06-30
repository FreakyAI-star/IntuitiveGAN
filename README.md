# What is GAN?
**GAN** stands for Generative Adversarial Networks. These kinds of networks are used for developing synthetic data generation. It combines two different models to achieve this task namely Generator and Discriminator models.

![gd](https://github.com/FreakyAI-star/IntuitiveGAN/assets/95335223/af7e0a81-bcb9-4d62-aa64-ea895bb3dd2b)

### Generator model
Generator models try to learn how to make a realistic representation of some class. They take input as noise which represents a random set of values going into the generative model. The generative model also sometimes takes input as a class Y. From these inputs, its goal is to generate a set of features X that look realistic. The noise is introduced to ensure that what's generated isn't actually the same dog each time and you'll see this theme play out shortly. More generally, generative models try to capture the probability distribution of the set of features X of a class Y. With the added noise, these models would generate realistic and diverse representations of this class Y. If we're generating only one class then we don't need this conditioning on Y and instead, it's just the probability over all the features X. Some of the most popular generative models are: **VAE** and **GAN**.

<p>
    <img src="https://github.com/FreakyAI-star/IntuitiveGAN/assets/95335223/9ff0ebdb-f46f-4621-a4b0-200ce78ec40e" height="200" width="400">
    <img src="https://github.com/FreakyAI-star/IntuitiveGAN/assets/95335223/4b4f60eb-c5e2-448f-890a-9fe19a8e7ff8" height="200" width="400">
</p>

### Discriminator model
A discriminative model is one typically used for classification in machine learning. These try to model the probability of class Y given a set of features X. Specific to our use case discriminator models are used for distinguishing real and fake. It learns the probability of class Y (real or fake) given features X. This probability is the feedback for the generator. 

<p>
    <img src="https://github.com/FreakyAI-star/IntuitiveGAN/assets/95335223/0f46b31e-1dde-47a0-bebe-5b059dfff400" height="200" width="400">
    <img src="https://github.com/FreakyAI-star/IntuitiveGAN/assets/95335223/55bdbe78-f259-485b-addb-d7f199f737d7" height="200" width="400">
</p>


* The generator's goal is to fool the discriminator.
* The discriminator's goal is to distinguish real and fake.
* They learn by adversarially competing with each other and in the end fakes look real.


### Combining Generator and Discriminator: Complete architecture of a basic GAN
![image](https://github.com/FreakyAI-star/IntuitiveGAN/assets/95335223/9ed84744-05a9-461d-9ddc-1285871740cd)
![image](https://github.com/FreakyAI-star/IntuitiveGAN/assets/95335223/425a7b86-b0cb-4a52-b113-fd5ff6fe6b8a)
![image](https://github.com/FreakyAI-star/IntuitiveGAN/assets/95335223/f5c3429d-5911-445f-9dc8-9863cdf1768c)

* GANs are trained in an alternating fashion
* The two models should be at similar skill levels so that the generator can know in which direction to improve.


# Building MNSIT GAN
Check out this [notebook](MNIST_GAN.ipynb)
