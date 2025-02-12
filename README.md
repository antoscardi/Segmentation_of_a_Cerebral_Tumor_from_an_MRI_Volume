# Segmentation of a Cerebral Tumor from an MRI Volume

## Overview
This project involves processing MRI data to detect and segment cerebral tumors using MATLAB. The developed pipeline allows users to visualize MRI slices, apply noise filtering, perform edge detection, manually refine segmentations, and compute the lesion area and volume.

## Features
- **Noise Handling:** Supports clean images as well as images with salt-and-pepper or Gaussian noise.
- **Edge Detection:** Utilizes Prewitt filters for edge enhancement in three directions.
- **User Interaction:** Provides GUI prompts for slice selection and manual segmentation refinement.
- **Lesion Analysis:** Computes lesion areas per slice and estimates total tumor volume.

## How to Run
### Prerequisites
- MATLAB
- Image Processing Toolbox

### Steps
1. Load the MRI data (`MRIdata.mat`).
2. Run the MATLAB script.
3. Follow the GUI prompts:
   - Choose noise type: clean, salt-and-pepper, or Gaussian.
   - Select slices for analysis.
   - Manually refine lesion segmentation by marking and adjusting regions.
4. The script will output:
   - Segmented images.
   - A table of lesion areas per slice.
   - A message displaying the computed tumor volume.

## Output
- **Segmented Images:** Displays MRI slices with detected tumor regions.
- **Area Computation:** Outputs a table of lesion areas for different MRI slices.
- **Volume Estimation:** Computes the total tumor volume in mm³.

## Methodology
1. **Preprocessing:**
   - Loads MRI data and applies optional noise (salt-and-pepper or Gaussian).
   - Provides options for noise filtering (median filtering for salt-and-pepper noise, convolution-based filtering for Gaussian noise).
2. **Edge Detection:**
   - Applies Prewitt filters to enhance edges in three directions (x, y, diagonal).
   - Binarizes the gradient image for clearer tumor segmentation.
3. **Manual Refinement:**
   - Users manually select the region of interest (ROI) for lesion segmentation.
   - Enables further corrections using interactive selection tools.
4. **Lesion Area and Volume Calculation:**
   - Computes lesion area in each slice.
   - Estimates total tumor volume using pixel dimensions.

## Example Usage
Upon running the script, the user follows on-screen prompts to:
- Select the first and last slice for segmentation.
- Refine the detected lesion by clicking on affected regions.
- View the computed lesion area and volume in a summarized report.

## Authors
- Guglielmo Bruno (Politecnico di Milano)
- Mirko Coggi (Politecnico di Milano)
- Antonio Scardino (Politecnico di Milano)

For any inquiries, contact:
- guglielmo.bruno@mail.polimi.it
- mirko.coggi@mail.polimi.it
- antonio.scardino@mail.polimi.it

