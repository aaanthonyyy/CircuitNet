<div align="center">


  <a href="https://github.com/aaanthonyyy">
    <img src="CircuitNet-Logo-01.svg" alt="Logo" width="200" height="200">
  </a>
  <h3 align="center">CircuitNet</h3>
  
   <p align="center">
      Schematic Sketch to Circuit Diagram Using Deep Learning
     <br/>
    <a href="https://colab.research.google.com/drive/1ox4m12Oa3GjwP47UdRArwCaUXbgUSLBf?authuser=2"><strong>Interactive Colab Demo »</strong></a>
  </p>

</div>

## Table of Contents
- [Introduction](#introduction)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)
- [Project Structure](#project-structure)

## Introduction
CircuitNet aims to automate the conversion of hand-drawn circuit sketches into professional circuit diagrams using deep learning. The system combines traditional image processing for component detection with a CNN for classification, achieving 90% detection and 96.5% classification accuracy across 5 common circuit components. 

## Installation
To install CircuitNet, follow these steps:

1. Clone the repository:
    ```bash
    git clone https://github.com/aaanthonyyy/CircuitNet.git
    cd CircuitNet
    ```
3. Activate the virtual environment:
    ```bash
    python -m venv circuitnet
    source circuitnet/bin/activate
    ```
5. Install the dependencies:
    ```bash
    pip install -r requirements.txt
    ```


## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Project Overview
> [!NOTE] 
> The project is divided into 3 main components: component detection, component classification, and circuit generation. The following sections provide an overview of each component.
<div align="center">
     <img src="https://user-images.githubusercontent.com/43044255/170146864-9e7f77e7-fd16-4c4e-9d26-26639a7e9c37.png" alt="Logo" width="600"/>
</div>
<br/>

### Dataset
The dataset used in this project consists of 3,191 images (including augmented data). The original dataset was sourced from [mahmut-aksakalli/circuit_recognizer](https://github.com/mahmut-aksakalli/circuit_recognizer/blob/master/traindata.zip) and was further augmented to improve model performance.

The dataset is located in the `dataset/` directory of this repository and includes:
- Original circuit component images
- Augmented variations of the original images
- Additional handcrafted component images

#### Extract the dataset:

   ```bash
   cd dataset/
   tar -xzvf circuit_dataset.tar.gz
   ```

### Notebooks
- **neural_network.ipynb**: This notebook is where the neural network is trained to predict the circuit components.
- **object_detection.ipynb**: This notebook covers the image processing algorithm used to detect circuit components.
- **circuit_generation.ipynb**: This notebook takes the detected and classified components to generate an SVG/PNG of the circuit.


### Component Classification
<div align="center">
     <img src="https://user-images.githubusercontent.com/43044255/170149446-d57c13f0-3ab0-4542-86c9-8a7093d11627.png" alt="Logo" width="600"/>
  <br/>
  <br/>
</div>
The component classification model was trained using a Convolutional Neural Network (CNN) with 5 classes: resistor, capacitor, inductor, voltage source, and current source. The model achieved an accuracy of 96.5% on the test set.
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

### Circuit Generation

The circuit generation pipeline transforms detected components into a complete circuit diagram through a three-stage process. First, the detected and classified components are processed to establish their spatial relationships and mapped to standardized circuit elements. Next, these processed components are used to automatically generate a JSON netlist that defines all component connections while preserving the original circuit topology. Finally, this netlist is rendered into an SVG circuit diagram using a rule-based placement system, which can then be exported to PNG format for easy visualization

---

#### Acknowledgements
I would like to express my sincere gratitude to Dr. Akash Pooransingh, my project supervisor, for his invaluable guidance, expertise and encouragement throughout this research project. His insights into machine learning applications in electrical engineering and consistent support were instrumental in bringing this project to fruition.