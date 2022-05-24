<div align="center">


  <a href="https://github.com/aaanthonyyy">
    <img src="CircuitNet-Logo-01.svg" alt="Logo" width="200" height="200">
  </a>
  <h3 align="center">CircuitNet</h3>
  
   <p align="center">
      Schematic Sketch to Circuit Diagram Using Deep Learning
     <br/>
    <a href="github.com/aaanthonyyy"><strong>Interactive Demo Coming Soon »</strong></a>
  </p>

</div>

## Abstract
Creating a circuit diagram from a schematic sketch is a common workflow in electrical
engineering. This can be a time-consuming process and take time away from circuit design.
This paper proposes a system for automatically converting the schematic sketch into a circuit
diagram using deep learning. The input sketch was preprocessed using adaptive thresholding
and binarization. Traditional image processing techniques such as morphological closing along
with blob (contour) detection were used to get the component bounding boxes. Component
classification was done using a deep convolutional neural network. The model was trained on
9500 images containing 5 component classes: resistors, inductors, capacitors, diodes, and dc
sources. An algorithm was developed to generate a custom JSON netlist. The netlist was then
used to create the schematic through an SVG wrapper. Results seemed promising – obtaining a
detection accuracy of 90% and a classification accuracy of 96.5%. 


## Software Dependancies
This project was built using the following open-source libraries:

*   [Numpy](https://www.numpy.org/) is an array manipulation library, used for linear algebra, Fourier transform, and random number capabilities.
*   [CV2](https://opencv-python-tutroals.readthedocs.io/en/latest/py_tutorials/py_gui/py_image_display/py_image_display.html) is a library for computer vision tasks.
*   [Skimage](https://scikit-image.org/) is a library which supports image processing applications on python.
*   [Matplotlib](https://matplotlib.org/) is a library which generates figures and provides graphical user interface toolkit.
*   [Tensorflow](https://www.tensorflow.org/) is an end-to-end open source machine learning platform
*   [SVG Schematic](https://github.com/KenKundert/svg_schematic) is a library to build a schematic using Python to instantiate and place the symbols and wires
*   [Cairo SVG](https://cairosvg.org/) is a library for processing SVG in python

## Project Overview

<div align="center">
     <img src="https://user-images.githubusercontent.com/43044255/170146864-9e7f77e7-fd16-4c4e-9d26-26639a7e9c37.png" alt="Logo" width="600"/>
</div>

  
