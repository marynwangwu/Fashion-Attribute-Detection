# Fashion Attribute Detection
## DS-GA 3001-009: Introduction to Computer Vision Final Project

[abstract here]

Below are each folder in the repo.  The raw segmentations and images can be downloaded from [link to data].  Paths to this data may need to be updated throughout the code to reproduce results.  After downloading the data, run `data_preprocessing.ipynb`.  Then train and evaluate the segmentation model and mask images using `segmentation_model.ipynb`.  Finally each classification model can be trained and evaluated in parallel.

## EDA
- `EDA.ipynb` - contains exploratory data analysis of raw data
  
## data
- `data_preprocessing.ipynb` - data preprocessing for metadata, segmentations, and images as described in the report
- `full_data_classification_EDA.ipynb` - additional EDA of preprocessed data distributions
- CSV files - preprocessed metadata in train/val/test splits
  
## models
- `segmentation_model_baseline.ipynb` - baseline and final U-Net segmentation model architecture, training, and evaluation
- `classification_model_baseline_pattern.ipynb` - baseline and tuned ResNet18 classification model model architecture, training, and evaluation for pattern
- `classification_model_pattern.ipynb` - EfficientNetV2 classification model model architecture, training, and evaluation for pattern
- `classification_model_baseline_fabric.ipynb` - baseline and tuned ResNet18 classification model model architecture, training, and evaluation for fabric
- `classification_model_fabric.ipynb` - EfficientNetV2 classification model model architecture, training, and evaluation for fabric
- Pickle Files - Loss and accuracy outputs per epoch for each model

