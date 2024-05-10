# Fashion Attribute Detection
## DS-GA 3001-009: Introduction to Computer Vision Final Project

The ubiquitous nature of fashion necessitates the automation of style and design recognition in clothing images for high-level semantic analysis. This project addresses this task by utilizing 12,701 full-body human images and segmentations from the DeepFashion-MultiModal dataset to establish a fashion attribute recognition pipeline, including clothing segmentation and pattern \& fabric classification.  The clothing segmentation model is implemented using a U-Net Convolutional Neural Network (CNN) architecture, and two main CNN models are built and compared for pattern and fabric attribute classification: ResNet18 and EfficientNetV2.  The segmentation model proved to be successful in segmenting clothing items. The ResNet18 and EfficientNetV2 models both were effective in classifying multiple clothing fabrics and patterns, with the ResNet18 model slightly outperforming EfficientNetV2. The results of this study demonstrate considerable preliminary success in the tasks of clothing segmentation and classification for downstream fashion analysis.

Below are each folder in the repo.  The raw segmentations and images can be downloaded from https://github.com/yumingj/DeepFashion-MultiModal.  Paths to this data may need to be updated throughout the code to reproduce results.  After downloading the data, run `data_preprocessing.ipynb`.  Then train and evaluate the segmentation model and mask images using `segmentation_model.ipynb`.  Finally each classification model can be trained and evaluated in parallel.

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

