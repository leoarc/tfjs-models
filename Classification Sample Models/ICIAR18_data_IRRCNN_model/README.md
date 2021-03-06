# ICIAR 2018 BACH Challenge

## Dataset


Dataset used is available [here](https://iciar2018-challenge.grand-challenge.org/Dataset/)

The image dataset is composed of high-resolution (2048 x 1536 pixels), uncompressed, and annotated H&E stain images from the ICIAR 2018 BACH Challenge.

Each image is labeled with one of four classes: i) normal tissue, ii) benign lesion, iii) in situ carcinoma and iv) invasive carcinoma.

Patch Size used : 128 X 128

Image Format : RGB

Pre-Processing : 128 X 128 patches are cropped from the complete images without any overlap. As there is no seperate test                            dataset 20% of the extracted patches are kept aside for testing and the rest are used for training. Pixel values are normalized before training.

Pixel scale: 0.42 µm x 0.42 µm

Magnification : 200x


Sample Images :

![](https://github.com/leoarc/tfjs-models/blob/master/Classification%20Sample%20Models/ICIAR18_data_IRRCNN_model/imgs/samp.png)
## Model Used :


The model used is the [IRRCNN](https://arxiv.org/pdf/1811.04241.pdf). It uses Residual connections in addition to the [IRCNN](https://arxiv.org/abs/1704.07709) model which adds the inputs at each step to the feature maps extracted by the IRCNN block after passing them through (1,1) convolutional filters to equate their dimensions .

Model architecture:

![](https://github.com/leoarc/tfjs-models/blob/master/Classification%20Sample%20Models/ICIAR18_data_IRRCNN_model/imgs/arch.png)


### References :

Alom, Md Zahangir, Mahmudul Hasan, Chris Yakopcic, Tarek M. Taha, and Vijayan K. Asari. "Improved Inception-Residual Convolutional Neural Network for Object Recognition."arXiv preprint arXiv:1712.09888(2017).
