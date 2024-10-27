# Deforestation Segmentation Using Raw Image Processing in MATLAB

This project analyzes deforestation over time by comparing satellite images from **2000** and **2017**. It leverages MATLAB for image processing, segmentation, and area calculation using color thresholding techniques.

---

## Features
- **Image Comparison**: Display and compare images from 2000 and 2017.
- **Grayscale Conversion**: Convert original images to grayscale.
- **Intensity Adjustment**: Adjust grayscale intensity for improved segmentation.
- **Color Segmentation**: Use color thresholding to segment deforested regions.
- **Area Calculation**: Compute the area of deforested regions in pixels and convert them to square kilometers.

---

## Project Structure
- **MLX File**: `deforestation_segmentation.mlx`  
  Contains the main script for reading images, processing them, and performing segmentation.

- **M File**: `createMask.m`  
  Auto-generated mask function from the MATLAB Color Thresholder app, used to segment regions based on color.

- **Images**:
  - `2000.jpg`: Satellite image from the year 2000.
  - `2017.jpg`: Satellite image from the year 2017.
  - (Include any additional images if applicable)

---

## Dependencies
- **MATLAB**: R2022a or later recommended.
- **Image Processing Toolbox**: Required for image adjustments and segmentation.

---

## How to Run
1. Open the project folder in MATLAB.
2. Run `deforestation_segmentation.mlx` to visualize the comparison and segmentation.
3. Use the `createMask` function for additional custom segmentation, if needed.

---

## Area Calculation Formula
To convert pixels to square kilometers:
- **Given scale**: 20 km = 58 px  
- **1 px** = \( \frac{20}{58} \) km  
- **Area of 1 px** = \( \left( \frac{20}{58} \right)^2 \) km²

- The total area is computed using:
  ```matlab
    px2km = (20 / 58)^2;
    area2000 = round(areaPx2000 * px2km);
    area2017 = round(areaPx2017 * px2km);

## Results
The segmented output displays the deforested regions for both years:

- Year 2000:
    Area = `area2000` km²

- Year 2017:
    Area = `area2017` km²
