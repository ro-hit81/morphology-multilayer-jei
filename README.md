# Morphology on Label Images: Multilayer Approach

[![Paper](https://img.shields.io/badge/Paper-JEI-blue.svg)](https://doi.org/10.1117/1.JEI.34.6.063017)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

## Abstract
Mathematical morphology was originally defined using set theory based on binary relationships. The complete lattice theory was later adopted as a theoretical framework to define morphological operators on an ordered set and extended to a certain extent into more complex data such as color images. However, the pixel values in label images represent semantic content without the underlying order of the labels, making it unsuitable for label images such as graphics, cartoons, geographical maps, and visualization results of image processing or analysis steps, including image segmentation. We present a framework of mathematical morphology for label images to address this issue. In the framework, the images are divided into multiple binary layers, which are processed independently and then merged back to restore the processed label image. The framework allows the application of all well-established tools from the original binary morphology, whereas the problem of label ordering is solved locally during the layer merging phase.

**📄 The full paper can be found [here](https://doi.org/10.1117/1.JEI.34.6.063017)**

## Repository Structure
```
├── notebooks/           # Jupyter notebooks with implementations
│   ├── 3_2_layer_decomposition_reconstruction.ipynb
│   ├── 5_2_layer_removal_reconstruction.ipynb
│   ├── 5_3_segmentation.ipynb
│   └── 5_4_template_matching.ipynb
├── data/                # Dataset and sample data
│   ├── container.jpg
│   ├── eval_mask.tif
│   ├── map.png
│   ├── map_image.png
│   ├── residential.tif
│   └── train_mask.tif
└── readme.md
```

## Usage
Install required packages and then:
1. Start Jupyter Lab/Notebook:
   ```bash
   jupyter lab
   ```
2. Run notebooks corresponding to paper figures:
   - `3_2_layer_decomposition_reconstruction.ipynb` - Figure 3: Example of layer reconstruction.
   - `5_2_layer_removal_reconstruction.ipynb` - Figure 9: Removal of the selected layers and image reconstruction by processing water and field Layers through the closing operation.
   - `5_3_segmentation.ipynb` - Figure 10: Improving low-level unsupervised image segmentation by OCCO morphological filtering, possibly followed by morphological reconstruction.
   - `5_4_template_matching.ipynb` - Figure 11: Performing template matching by combining supervised pixelwise classification and multi-layer morphological hit-or-miss transform.

## Requirements
- Python 3.8+
- Jupyter Lab/Notebook
- NumPy, Matplotlib, PIL (Pillow)
- OpenCV (cv2), scikit-image
- scikit-learn, rasterio
- scipy

## Citation
```bibtex
@article{khati2025morphology,
  title={Morphology on Label Images: Multilayer Approach},
  author={Pasi Fränti, Swaiz Ahmed, Rohit Khati, Sébastien Lefèvre},
  journal={Journal of Electronic Imaging},
  year={2025}
}
```

## Contact
For questions about this research, please contact franti@cs.uef.fi