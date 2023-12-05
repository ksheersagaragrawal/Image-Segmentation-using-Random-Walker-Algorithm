# Image Segmentation Using Random Walker Algorithm

This repository contains the implementation of the Random Walker Algorithm for image segmentation. This technique is part of a computational approach to segmenting images based on probability calculations and pixel value analysis.

## Overview

The Random Walker Algorithm is a powerful method for image segmentation that treats pixel nodes in an image as a part of a graph. Segmentation is achieved by marking nodes and calculating the probability of a neighbor taking the same pixel value, inversely proportional to the difference between the pixel values.

## Random Walk Algorithm Formulas

The Random Walk Algorithm for image segmentation is based on the following steps and formulas:

1. **Node Marking**:
   - Mark nodes based on pixel values.
   - If greater than 110, then mark as 255.
   - If less than 75, then mark as 0.

2. **Unmarked Nodes**:
   - All the unmarked nodes will be marked in subsequent steps.

3. **Matrix Operations**:
   - `Lu . X = (-B)^T . M`
   - For a matrix of size p*q, we will have L of size p*q*8.
   - `(B)^T` is a submatrix of the L matrix that contains information about all the unmarked nodes to marked nodes.
   - `Lu` is a submatrix of the L matrix containing information about all the unmarked to unmarked nodes.
   - `M` matrix is defined for zero and 255 class `M0` and `M255`.

4. **Calculating Probabilities**:
   - Find `L inverse`, `(B)^T`, and `M` matrix to find `X`.
   - `X` for `M0` is the probability for pixel k taking value 0.

5. **Image Construction**:
   - Construct a new image from `X` by comparing their probability to determine the final pixel values.


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

