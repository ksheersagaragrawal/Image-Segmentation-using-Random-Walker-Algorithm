# Image Segmentation Using Random Walker Algorithm

This repository contains the implementation of the Random Walker Algorithm for image segmentation. This technique is part of a computational approach to segmenting images based on probability calculations and pixel value analysis.

## Overview

The Random Walker Algorithm is a powerful method for image segmentation that treats pixel nodes in an image as a part of a graph. Segmentation is achieved by marking nodes and calculating the probability of a neighbor taking the same pixel value, inversely proportional to the difference between the pixel values.

## Random Walk Algorithm Formulas

The Random Walk Algorithm for image segmentation is based on the following steps and formulas:

## Random Walk Algorithm Formulas

The Random Walk Algorithm for image segmentation is based on the following steps and formulas:

1. **Node Marking**:
   The nodes in the image are marked based on the following criteria:
   - Let $p(i, j)$ be the pixel value at position (i, j) in the image.
   - Mark the nodes as follows:
     - If $p(i, j) > 110$, then mark as 255 (white).
     - If $p(i, j) < 75$, then mark as 0 (black).

2. **Matrix Operations**:
   All the unmarked nodes will be marked in subsequent steps. The key formula in the Random Walk Algorithm for image segmentation is:
   $$L_u \cdot X = (-B)^T \cdot M$$
   Where:
   - $L_u$ is a submatrix of the L matrix containing information about all the unmarked to unmarked nodes.
   - $X$ is the matrix representing probabilities.
   - $B^T$ is a submatrix of the L matrix that contains inforation about all the unmarked nodes to marked nodes.
   - $M$ matrix is defined for zero and 255 class $M_0$ and $M_{255}$.

3. **Calculating Probabilities**:
   First, calculate $X$ using the formula:
   $$X = L^{-1} \cdot (B^T) \cdot M$$
   where $L^{-1}$ is the inverse of matrix $L$, $B^T$ is the transpose of matrix $B$, and $M$ is the predefined matrix.
   
   The probability for pixel $k$ taking the value 0 is given by the corresponding element in matrix $X$ for $M_0$, which can be represented as:
   $$P(k \text{ takes value } 0) = X_k \text{ for } M_0$$
   where $X_k$ is the k-th element in the matrix $X$.




## Results and Performance

The algorithm's performance is evaluated based on the accuracy of segmentation. The accuracy is calculated as:

$$
\text{Accuracy} = \frac{|\text{White Pixels in SkitLearn} - \text{White Pixels in New Image}|}{\text{Total White Pixels} + \text{Total Black Pixels}}
$$

Overall accuracy achieved: `93.682%`

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

