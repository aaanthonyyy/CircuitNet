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

## Project Overview
<div align="center">
     <img src="https://user-images.githubusercontent.com/43044255/170146864-9e7f77e7-fd16-4c4e-9d26-26639a7e9c37.png" alt="Logo" width="600"/>
</div>

> A deep learning algorithm is proposed to automatically convert schematic sketches into circuit diagrams. The algorithm is promising, achieving a detection accuracy of 90% and a classification accuracy of 96.5%.

<br/>
<br/>


### Component Segmentation
<div align="center">
     <img src="https://user-images.githubusercontent.com/43044255/170148823-b921898d-1d6a-457b-8dfa-ffa2ad8d0ea7.png" alt="Logo" width="600"/>
  <br/>
  <br/>
</div>
There are a variety of feature detection algorithms possible, but we opted for traditional image processing techniques due to the inavailability of labeled data. 

<br/>
<br/>

### Classification Architecture
<div align="center">
     <img src="https://user-images.githubusercontent.com/43044255/170149446-d57c13f0-3ab0-4542-86c9-8a7093d11627.png" alt="Logo" width="600"/>
  <br/>
  <br/>
</div>


### Software Dependancies
This project was built using the following open-source libraries:

*   [Numpy](https://www.numpy.org/) is an array manipulation library, used for linear algebra, Fourier transform, and random number capabilities.
*   [CV2](https://opencv-python-tutroals.readthedocs.io/en/latest/py_tutorials/py_gui/py_image_display/py_image_display.html) is a library for computer vision tasks.
*   [Skimage](https://scikit-image.org/) is a library which supports image processing applications on python.
*   [Matplotlib](https://matplotlib.org/) is a library which generates figures and provides graphical user interface toolkit.
*   [Tensorflow](https://www.tensorflow.org/) is an end-to-end open source machine learning platform
*   [SVG Schematic](https://github.com/KenKundert/svg_schematic) is a library to build a schematic using Python to instantiate and place the symbols and wires
*   [Cairo SVG](https://cairosvg.org/) is a library for processing SVG in python
  
