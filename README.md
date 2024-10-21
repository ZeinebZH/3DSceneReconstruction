# 3D Scene Reconstruction

A MATLAB-based app for real-time 3D scene reconstruction from interior image sequences using geometric computer vision algorithms (group project for the EI70110 challenge, SS23 Edition).

## Table of Contents

- [Description](#description)
- [Requirements](#requirements)
- [Quick Start](#quick-start)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)

## Description

This software processes a collection of room images to generate a 3D model, reconstructing its spatial structure and providing an abstract visual representation. While it can work with random images, sequentially ordered images yield more accurate results.

![GUI](/visuals/3dmodel.png)

## Requirements

This software has been developed and tested using the following software and libraries:

- MATLAB (version R2023a)
- [Computer Vision Toolbox](https://www.mathworks.com/products/computer-vision.html)
- [Image Processing Toolbox](https://www.mathworks.com/products/image.html)
- [Statistics and Machine Learning Toolbox](https://www.mathworks.com/products/statistics.html)

## Quick Start

### Step 1: Launch GUI
Ensure MATLAB R2023a is running. Execute the `main.m` script to open the GUI:

![GUI](/visuals/gui.png)

### Step 2: Load Camera Parameters
Click "Load Parameters" and select the folder containing `images.txt` and `cameras.txt`.

### Step 3: Load Images
Click "Load Images" to select the images of the room you want to process.

![GUI](/visuals/guiloaded.png)

### Step 4: Select Feature Extraction Algorithm
Choose between "SIFT" (more accurate but slower) and "SURF" for feature extraction.

### Step 5: Generate Point Cloud
Click "Generate Point Cloud" to create and display a 3D point cloud of the room.

![GUI](/visuals/point_cloud.png)

### Step 6: Optimize Parameters
Adjust the following parameters for optimal results:

- **Distance for Denoising**: Controls clustering distance during denoising.
- **Point Count for Denoising**: Sets threshold for removing noise.
- **Shrink Factor for Room Shape**: Adjusts the fit of the wall structure.
- **Number of Boxes in Visualization**: Modifies point clusters created during k-means.

### Step 7: Visualize the 3D Model
Click "Plot Visualization" to view the abstract 3D model. Click again to return to the point cloud view.

![GUI](/visuals/3dmodel.png)

### Step 8: Measure Distance
Enable "Distance Measurement Mode" to select two points in the 3D model and calculate the distance between them.

![GUI](/visuals/distance.png)
