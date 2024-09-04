---

# Brain MRI Augmentation using MONAI

This repository contains a Jupyter Notebook that performs various data augmentation techniques on Brain MRI scans using the MONAI library. The augmentations are designed to enhance and increase the dataset for training deep learning models, particularly in medical imaging applications such as brain tumor segmentation.

## Overview

Medical image data is often limited in quantity and diversity. To improve the generalization capability of machine learning models, data augmentation is a crucial step. This repository provides a comprehensive set of augmentation techniques applied to Brain MRI scans, making use of MONAI, a specialized library for deep learning in healthcare.

## Augmentations Used

The following augmentations are applied to the Brain MRI scans in the notebook:

1. **Load Images and Labels**: 
   - `LoadImaged`: Loads the MRI scans and corresponding labels from files.
   
2. **Ensure Channel First**: 
   - `EnsureChannelFirstd`: Ensures the channel dimension is first in the tensor.

3. **Type Conversion**: 
   - `EnsureTyped`: Converts the loaded images and labels into MONAI-compatible tensor types.

4. **Multi-Channel Label Conversion**: 
   - `ConvertToMultiChannelBasedOnBratsClassesd`: Converts label data to a multi-channel format based on BraTS tumor classes.

5. **Orientation**: 
   - `Orientationd`: Reorients images and labels to a standard orientation (RAS).

6. **Resampling**: 
   - `Spacingd`: Resamples the images and labels to a uniform voxel spacing of 1mm x 1mm x 1mm.

7. **Resizing**: 
   - `Resized`: Resizes images and labels to a fixed size of 96x96x96 voxels.

8. **Random Flips**: 
   - `RandFlipd`: Randomly flips images and labels along the specified axes (x, y, z).

9. **Random Rotation**: 
   - `RandRotate90d`: Randomly rotates images and labels by 90 degrees.

10. **Intensity Scaling**: 
   - `RandScaleIntensityd`: Randomly scales the intensity of the images by a factor within ±10%.

11. **Intensity Shifting**: 
   - `RandShiftIntensityd`: Randomly shifts the intensity of the images within ±10%.

12. **Gaussian Noise**: 
   - `RandGaussianNoised`: Adds Gaussian noise to the images with a standard deviation of 0.01.

13. **Normalization**: 
   - `NormalizeIntensityd`: Normalizes the intensity values of the images on a per-channel basis.

14. **Tensor Conversion**: 
   - `ToTensord`: Converts images and labels into PyTorch tensors.

## Getting Started

### Prerequisites

- Python 3.8+
- MONAI
- PyTorch
- Jupyter Notebook


## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.


## Acknowledgments

- [MONAI](https://monai.io/) for providing the tools to perform medical image processing.
- The [BraTS Challenge](https://www.med.upenn.edu/cbica/brats2021/) for the dataset and inspiration.

---
