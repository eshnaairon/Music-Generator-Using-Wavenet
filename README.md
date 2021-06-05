# Music-Generator-Using-Wavenet

Deep Learning architectures are being used for generating music , a field many assume is beyond the scope of machines.
This project uses WaveNet to generate music .WaveNet's primary goal is to produce new samples from the data's original distribution ,and therefore it's called a Generative Model. As an input, it takes a piece of a raw audio wave , that is represented in the form of amplitude values which are recorded at different intervals of time. WaveNet tries to anticipate the next amplitude value given the series of amplitude values.

#### WaveNet Architecture -

![image](https://user-images.githubusercontent.com/52113227/120904078-c8ef7700-c667-11eb-8b9a-04b3258370d8.png)

Workflow- 
1. A causal 1D convolution is fed as input.
2. After that, the output is fed into two dilated 1D convolution layers with sigmoid and tanh activations.
3. Skip connection is created by multiplying two separate activation values element-by-element.
4. The residual is obtained by adding a skip connection and the output of causal 1D element by element.

* However because the objective of the skip and connection layers is to improve faster convergence, I have simplified the WaveNet architecture by removing residual and skip connections (and WaveNet takes raw audio wave as input).

#### Data used 
A small collection of midi files . It is present in the data folder

#### Requiremnets
1. Numpy
2. pandas
3. Tensorflow 2.0 
4. Music21 - For handeling midi files
5. Sklearn

References-
https://www.analyticsvidhya.com/blog/2020/01/how-to-perform-automatic-music-generation/
