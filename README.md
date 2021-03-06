## Google Satelite Image to Streetmap Image translation using Pix2Pix GAN

The Pix2Pix GAN is a general approach for image-to-image translation. It is based on the conditional generative adversarial network, where a target image is generated, that is conditioned on a given input image. The idea of Pix2Pix GAN was proposed in this [paper](https://arxiv.org/abs/1611.07004). According to the paper, the model not only learn the mapping from source image to target image, but also learn a loss function to train this mapping. 


### Network Architecture
The **generator** is a modified U-net model, it takes an RGB image as input and then tries to map it to another RGB image of the same shape.
The discriminator is a PatchGan and which outputs a 30x30 matrix, which is then used to calculate the adversarial loss.

<img src="https://github.com/Therickysen08/pix2pix/blob/main/images/discriminator.png" width="650" height="240"/>


### Dataset
The dataset can be downloaded from Kaggle by using this [link](https://www.kaggle.com/alincijov/pix2pix-maps/version/1). After downloading the dataset extract it to the data/dataset folder.

### Hyperparameters
    source_images = 1096
    target_images = 1096
    IMAGE_HEIGHT = 256
    IMAGE_WIDTH = 256
    IMAGE_CHANNEL = 3
    DISCRIMINATOR_LEARNING_RATE = 0.0002
    GENERATOR_LEARNING_RATE = 0.0002
    BATCH_SIZE = 1
    EPOCHS = 180
    BETA1 = 0.5
    BETA2 = 0.999
    WEIGHT_INIT_STDDEV = 0.02

### Results

<img src="https://github.com/Therickysen08/pix2pix/blob/main/images/result.png" width="650" height="240"/>

<img src="https://github.com/Therickysen08/pix2pix/blob/main/images/result2.png" width="650" height="240"/>

## Acknowledgment
This [playlist](https://www.youtube.com/playlist?list=PLhhyoLH6IjfwIp8bZnzX8QR30TRcHO8Va) helped me a lot. 

