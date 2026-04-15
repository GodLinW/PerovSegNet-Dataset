# PerovSegNet: Automated and Scalable SEM Image Analysis Framework

PerovSegNet is a high-precision deep learning framework tailored for the automated segmentation of perovskite solar cell SEM images. It is designed to quantify lead iodide, perovskite grains, and defect domains with high robustness across various magnifications and imaging conditions.

## 📂 Project Directory Structure

The repository is organized to support systematic training, validation, and benchmarking across diverse material systems.

```text
Perovskite_Project_V2/
├── Internal_Dataset/           # Core training & validation set (46 samples)
│   ├── images/                 # Raw SEM images
│   ├── labels/                 # Annotated segmentation masks
│   └── data.yaml               # Dataset configuration
├── External_Test_Set/          # Cross-laboratory OOD benchmark
│   ├── Sub_Mag_200nm/ & _label/
│   ├── Sub_Mag_500nm/ & _label/
│   ├── Sub_Mag_1um/   & _label/
│   └── Sub_Mag_4um/   & _label/
├── Robustness_Stress_Test/     # Digital degradation benchmark
│   ├── 01_Blurring_Test/       # Defocus simulation (σ=0 to 5)
│   ├── 02_Resolution_Test/     # Downsampling simulation (100% to 25%)
│   ├── 03_Contrast_Test/       # Signal loss simulation (100% to 40%)
│   ├── Source_Images/          # Original reference set
│   └── Source_Images_label/    # Ground truth masks
├── chalcogenide thin-film images/
├── lead-free perovskite images/
├── cross-sectional images/
└── oxide thin-film images/
```
## 📥 Dataset Access

To facilitate reproducibility and further research, our datasets are publicly available. You can access and download the raw data and corresponding annotation masks via the following links:

| Dataset | Description | Download Link |
| :--- | :--- | :--- |
| **Internal Dataset** | High-resolution labeled perovskite SEM images for model training and baseline validation. | [👉 Download Link](https://drive.google.com/file/d/1V7X78butwTfp0JktDmamgi093WcYRL3v/view?usp=sharing) |
| **Robustness Stress Test** | Systematically degraded SEM images (blur, downsampling, and contrast attenuation) to evaluate model generalization. | [👉 Download Link](https://drive.google.com/file/d/1ukzQctgXwgs51YfDhnc-hWxjXrxUKgI3/view?usp=sharing) |

---
*Note: Please refer to the `Dataset Directory Structure` above to ensure the data is placed in the correct subfolders after downloading.*
