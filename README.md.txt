# Neural Style Transfer Using VGG-19

## Project Overview

This project implements neural style transfer using PyTorch and a pretrained VGG-19 convolutional neural network.

The goal is to combine the content of a photograph with the artistic style of another image. Content loss helps preserve the structure of the photograph, while style loss helps reproduce the colours, textures, and patterns of the style image.

The project also investigates how different style-loss weights and CNN layer selections affect the generated image.

## Methodology

- **Feature extractor:** Pretrained VGG-19
- **Content layer:** `conv4_2`
- **Style layers:** `conv1_1`, `conv2_1`, `conv3_1`, `conv4_1`, `conv5_1`
- **Content loss:** Mean squared error between feature maps
- **Style loss:** Difference between Gram matrices
- **Optimiser:** Adam
- **Image size:** 256 × 256 pixels

## Experiments

### Experiment 1: Effect of Style Weight

Style weights of 1,000, 10,000, and 50,000 are compared to investigate how the relative importance of style loss affects the output.

### Experiment 2: Effect of Style Layers

Two shallow style layers are compared with five selected style layers to investigate the effect of layer selection on the generated image.

## Project Structure

```text
neural-style-transfer/
├── README.md
├── Neural_Style_Transfer.ipynb
├── requirements.txt
├── images/
│   ├── content_image.png
│   └── style_image.png
└── results/
    └── results_table.csv
```

## Requirements

- Python 3
- PyTorch
- torchvision
- NumPy
- Matplotlib
- Pillow
- pandas

## How to Run

### Option 1: Google Colab

1. Open the notebook in Google Colab.
2. Select a runtime.
3. Upload the content and style images when prompted.
4. Run all notebook cells in order.
5. Review the generated images, loss curve, and experiment results.

### Option 2: Local Environment

Install the dependencies listed in `requirements.txt`, then launch Jupyter Notebook and open `Neural_Style_Transfer.ipynb`.

## Reproducibility

The random seed, software versions, image size, optimisation settings, and loss weights should be recorded to make experiments easier to reproduce.

Record the seed actually used in the final notebook. A fixed seed does not guarantee identical results across all hardware and software environments.

## Results

Add the measured results from the final notebook run to the table below. Do not enter estimated or invented values.

| Experiment | Setting | Steps | Content Loss | Style Loss | Total Loss |
|---|---|---:|---:|---:|---:|
| Baseline | Style weight = 10,000 | 150 | To be recorded | To be recorded | To be recorded |
| Style weight | 1,000 | 100 | To be recorded | To be recorded | To be recorded |
| Style weight | 10,000 | 100 | To be recorded | To be recorded | To be recorded |
| Style weight | 50,000 | 100 | To be recorded | To be recorded | To be recorded |
| Layer comparison | Two shallow layers | 100 | To be recorded | To be recorded | To be recorded |
| Layer comparison | Five style layers | 100 | To be recorded | To be recorded | To be recorded |

## References

1. L. A. Gatys, A. S. Ecker, and M. Bethge, “Image Style Transfer Using Convolutional Neural Networks,” CVPR, 2016.
2. PyTorch, “Neural Transfer Using PyTorch,” https://docs.pytorch.org/tutorials/advanced/neural_style_tutorial.html
3. Torchvision, “VGG Models,” https://docs.pytorch.org/vision/main/models/vgg.html

