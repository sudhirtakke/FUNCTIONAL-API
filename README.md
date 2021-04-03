# FUNCTIONAL-API
The functional API in Keras is an alternate way of creating models that offers a lot more flexibility, including creating more complex models.

**Sequential model API** is great for developing deep learning models **in most situations**, **but it also has some limitations**

For example, it is **not straightforward** to define models that may have **multiple different input sources, produce multiple output destinations or models that re-use layers.**

### Keras Functional Models

- The **Keras functional API** provides a **more flexible** way for defining models.

 - It **specifically** allows you to **define multiple input or output models as well as models that share layers**. More than that, it allows you to **define ad hoc acyclic network graphs.**

 - Models are defined by creating instances of layers and connecting them directly to each other in pairs, then defining a Model that specifies the layers to act as the input and output to the model.

#### Defining Input

 - Unlike the Sequential model, you must create and define a standalone Input layer that specifies the shape of input data.

 - The input layer takes a shape argument that is a tuple that indicates the dimensionality of the input data.

 - When input data is one-dimensional, such as for a multilayer Perceptron, the shape must explicitly leave room for the shape of the mini-batch size used when splitting the data when training the network. Therefore, the shape tuple is always defined with a hanging last dimension when the input is one-dimensional (2,), for example:

#### Connecting Layers

 - The layers in the model are connected pairwise.

 - This is done by specifying where the input comes from when defining each new layer. A bracket notation is used, such that after the layer is created, the layer from which the input to the current layer comes from is specified.

 

