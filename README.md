**Pizza Image Detector**

**Authors: Evan Turkon, Warren K. Watson II**

**Problem Introduction:**

For our final project, we decided to create a Pizza Detector to detect if a certain picture is of a pizza or not. It took us quite a while to come up with this idea, as a number of our previous ideas didn’t end up working out for various reasons. At first, we wanted to create a Machine Learning Model to detect locations of chess pieces and their types in a chess game, but after doing our initial proposal and planning, we realized that our project idea was too specific, too “niche”. So, we decided to try an ImageNet Object Localization Model instead. With this model, we wanted to detect the presence of certain objects in an image. After coming up with another proposal and talking to our professor, we realized that we probably were not going to have enough time in the semester to accomplish a task of this magnitude, our idea was too ambitious. We went back to brainstorming once again. This time, we settled on a simple Machine Learning Model that would take a bunch of pictures and decide whether they were lions or cheetahs. We then got to work, only to realize that most of our model was built off of strictly transfer learning. We didn’t like this at all. We wanted to create our own model from scratch so we could really get the experience of creating our own neural network with our own features and tuning all of the parameters, minimizing the cost, etc., so we decided to do just that. This is where the idea for creating a Pizza Detector was born.

**Proposed Solution:**

In order to successfully create a pizza detector, we quickly realized we were going to have to find some data that is already pre trained, and we were going to have to build a Convolutional Neural Network from scratch in order to actually be able to detect if images are pizza or not. Convolutional Neural Networks have a convolutional layer and in that layer it uses convolution operations to process the data, which has benefits for working with images. This is what allows you to even be able to process your data through the network. You wouldn’t be able to with a regular Neural Network. 

**Experimental Setup (data, evaluation procedure):**

We found a set of images on kaggle. 983 instances are pizza, 983 instances are not pizza.
- Link: https://www.kaggle.com/datasets/carlosrunner/pizza-not-pizza

We decided to split our data up and into two sets, a training set and a validation set. We did a 70/30 split.

**Results (stats, figures, plots, etc.):**

Our model turned out to be pretty good. There was some randomness in the validation accuracy but that is to be expected due to batch normalization.


**Conclusion:**

Getting to this point of having a fully functional pizza detector was definitely not easy, but we had a ton of fun. After a bunch of brainstorming and troubleshooting of ideas, we were finally able to gain some traction in a project that definitely proved to be worthwhile in the understanding of machine learning in general. Being able to apply what we learned in class to a facet of machine learning we’ve never seen before to curate this project is something that we believe is very special. We learned a ton about CNN’s and Batch Normalization, and about the ups and downs of the development of ML models as a whole. We are definitely pleased with the results and real world application of our model.

**Annotated references/Work Cited:** 

- https://keras.io/api/layers/convolution_layers/convolution2d/#:~:text=2D%20convolution%20layer%20
- https://www.tensorflow.org/
- https://medium.com/intelligentmachines/convolutional-neural-network-and-regularization-techniques-with-tensorflow-and-keras-5a09e6e65dc7

