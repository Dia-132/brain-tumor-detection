# brain-tumor-detection
# Brain Tumor Detection from MRI Scans

This project uses a U-Net-based convolutional neural network for semantic segmentation to detect and localize brain tumors in MRI scans. The model processes grayscale MRI images and produces segmentation masks highlighting tumor regions.

---

## Features

- Preprocessing and augmentation of MRI data
- U-Net model architecture for segmentation
- Dice loss + Binary Cross Entropy for optimization
- Training and validation with result visualization
- Easily extendable to other medical segmentation tasks

---

## Model Architecture: U-Net

The U-Net architecture is widely used in biomedical image segmentation. It consists of:
- Encoder (contracting path): Extracts features using convolution and pooling
- Decoder (expanding path): Reconstructs segmentation masks using transposed convolutions and skip connections

---

## Dataset

The dataset consists of MRI scans and binary masks marking tumor regions. Each MRI is grayscale with an associated ground truth label.

Note: Actual dataset is not included in this repository. You can upload your own dataset locally in a `dataset/` folder.

---

## How to Run

1. Download this repository as ZIP and extract it.
2. Open the `.ipynb` file using:
   - Jupyter Notebook (installed with Anaconda)
   - Google Colab (upload notebook and mount your dataset)
3. Run the notebook cells step-by-step.

---

## Output

The model outputs segmentation masks for input MRI images.

| MRI Image | Ground Truth | Predicted Mask |
|-----------|--------------|----------------|
| sample_mri.png | sample_mask.png | sample_pred.png |

(Optional: Add these sample images in a `samples/` folder)

---

## Requirements

You can install the required libraries using:

```bash
pip install torch torchvision matplotlib numpy opencv-python

