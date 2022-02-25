# Steel-Defect-Detection
In our approach, we will explore multilabel classification (single and multi-output CNN-based architectures) and semantic segmentation separately. Even though classification does not indicate where exactly the defect is occurring, it can definitely aid and ease manual localization. It will also help validate segmentation classification results.

<img src="https://github.com/Sakshee5/Steel-Defect-Detection/blob/main/Images/Fig%201.png" width="400" height="300">

## Dataset
[Kaggle Link](https://www.kaggle.com/c/severstal-steel-defect-detection/data)

The dataset explored in the work is obtained from Severstal. The exploratory data analysis (EDA) of the dataset reveals that a single image may contain one or more defects, thus presenting a problem statement of multilabel classification and segmentation. EDA also demonstrates that there is a significant class imbalance within the dataset, which is addressed using data augmentation, class-wise re-weighing and adaptive learning rate methods.

## Multilabel Classification: Single and multi-output CNN model
<img src="https://github.com/Sakshee5/Steel-Defect-Detection/blob/main/Images/Fig%205.png" width="400" height="300">

## Training Flowchart
<img src="https://github.com/Sakshee5/Steel-Defect-Detection/blob/main/Images/Fig%206.png" width="600" height="300">

## Image Segmentation Models
#### 1. Fully Connected Network (FCN)

#### 2. Modified U-Net with LeakyReLU Activation and Dropout, Batch Normalization, and 2D Upsampling layers
<img src="https://github.com/Sakshee5/Steel-Defect-Detection/blob/main/Images/Fig%208.png" width="450" height="170">

#### 3. Residual U-Net 
<img src="https://github.com/Sakshee5/Steel-Defect-Detection/blob/main/Images/Fig%2011.png" width="300" height="400">

## Conclusion
The fully connected network achieves a dice score of 0.5672 and is treated as the baseline model. The other two segmentation models are inspired by the well-reported U-Net architecture. The original encoder-decoder network with skip connections is hyper-tuned and modified by adding new learning layers and activation functions as part of the first modification. In the second method, the U-Net is strengthened with the help of residual learning. Amongst the segmentation models, the hyper-tuned modified U-Net design achieves a dice score of 0.69, whereas the Residual U-Net shows promising results as is observed from its smooth training curve. With a final dice score of 0.69 on the best model (which is an increase of 0.2 from the original U-Net structure), the objective of this study is successfully fulfilled.


