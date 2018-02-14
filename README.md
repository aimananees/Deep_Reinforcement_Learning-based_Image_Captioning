### Deep Reinforcement Learning-based Image Captioning

Image captioning is a challenging problem owing to the complexity in understanding the image content and diverse ways of describing it in natural language. Recent advances in deep neural network have substantially improved the performance of this task. <br>
In this project, we will implement a novel decision making framework for image captioning. We utilize a “policy network” and a “value network” to collaboratively generate captions and train both networks using an actor-critic reinforcement learning model, with a novel reward defined by visual-semantic embedding.

#### Objective
The Image captioning model has been implemented using keras. It consists of three components:<br>
1. Policy network pπ that is comprised of a CNN and a RNN. The CNNp output is fed as the initial input of RNNp. The policy network computes the probability of executing an action at at a certain state st, by pπ(at|st).<br>
2. An encoder CNN model: A pre-trained CNN is used to encode an image to its features. In this implementation VGG16 model is used as encoder and with its pretrained weights loaded.<br>
3. A word embedding model: An embedding model is trained that takes a word and outputs an embedding vector.<br>
4. A decoder RNN model: A LSTM network has been employed for the task of generating captions. It takes the image vector and partial captions at the current timestep and input and generated the next most probable word as output.<br>
