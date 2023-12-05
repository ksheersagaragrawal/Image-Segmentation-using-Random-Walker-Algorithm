# Image Segmentation Using Random Walker Algorithm

This repository contains the implementation of the Random Walker Algorithm for image segmentation. This technique is part of a computational approach to segmenting images based on probability calculations and pixel value analysis.

## Overview

The Random Walker Algorithm is a powerful method for image segmentation that treats pixel nodes in an image as a part of a graph. Segmentation is achieved by marking nodes and calculating the probability of a neighbor taking the same pixel value, inversely proportional to the difference between the pixel values.

## Algorithm Steps

1. Mark nodes based on pixel values (greater than 110 as 255, less than 75 as 0).
2. Mark all unmarked nodes in subsequent steps.
3. Implement matrix operations to calculate probabilities.
4. Construct a new image based on calculated probabilities.

## Results and Performance

The algorithm's performance is evaluated based on the accuracy of segmentation. The accuracy is calculated as:

`Accuracy = (|White Pixels in SkitLearn - White Pixels in New Image| ) / (Total White + Black Pixels) * 100`

Overall accuracy achieved: 93.682%

## Usage

1. Run the provided Jupyter Notebook: [ImageSegmentation.ipynb](https://github.com/ksheersagaragrawal/Image-Segmentation-using-Random-Walker-Algorithm/blob/main/ImageSegmentation.ipynb).
2. To process a different image, change the image path in the notebook accordingly.
3. The notebook includes code and visualizations demonstrating the segmentation process.

## Dependencies

- Python
- Numpy
- Matplotlib
- (Any other libraries used in the project)

## Future Work

- Improving the algorithm to handle more complex image structures.
- Optimizing performance for large-scale images.
- Exploring the use of the algorithm in various application areas such as medical imaging or satellite imagery.

## License
This project is open-source and available under the MIT License.

