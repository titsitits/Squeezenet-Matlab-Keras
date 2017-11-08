# Squeezenet-Matlab-Keras
Squeezenet pretrained model compatible with Matlab function ImportKerasNetwork.

These files were created from https://github.com/rcmalli/keras-squeezenet with keras 2.0.6.

### Usage example in Matlab R2017b :

~~~matlab
squeezenet = importKerasNetwork('squeezenet.json','WeightFile','squeezenet.h5','OutputLayerType','classification');
figure;plot(pretrainednet);

~~~

### Saving method (with python):

~~~python
import numpy as np
from keras_squeezenet import SqueezeNet
from keras.applications.imagenet_utils import preprocess_input, decode_predictions
from keras.preprocessing import image

model = SqueezeNet()

model_json = model.to_json()
with open("squeezenet.json", "w") as json_file:
    json_file.write(model_json)
model.save_weights("squeezenet.h5")

~~~



### References

1) [Keras Framework](www.keras.io)

2) [SqueezeNet Official Github Repo](https://github.com/DeepScale/SqueezeNet)

4) [Python/Keras code for squeezenet model](https://github.com/rcmalli/keras-squeezenet)

5) [SqueezeNet Paper](http://arxiv.org/abs/1602.07360)

### Notes
Layers names have been changed from original python code as / are not allowed in layers names in Matlab. Instead, _ was used.

