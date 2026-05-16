# Smart Waste Sorting Using Image Recognition

This project is a deep learning-based image recognition application for smart waste sorting.  
The system classifies waste images into several categories such as plastic, paper, glass, metal, cardboard, and trash.

## Project Overview

Waste sorting is an important step in improving recycling efficiency and reducing environmental pollution.  
However, in daily life, many people still mix different types of waste in the same bin.

This project proposes a simple image recognition application that can help users identify waste categories automatically from an uploaded image.

The project is developed as part of an Image Recognition course assignment.

## Main Objective

The main objective of this project is to build a deep learning-based image recognition solution in the form of an application prototype.

The application should be able to:

- Receive a waste image as input
- Classify the image into a waste category
- Display the prediction result
- Show confidence scores
- Demonstrate the use of deep learning for a real-world problem

## Dataset

The dataset is expected to contain waste images organized by class folders.

Recommended folder structure:

```text
dataset/
├── cardboard/
├── glass/
├── metal/
├── paper/
├── plastic/
└── trash/
```

Each folder contains images that belong to the corresponding waste category.

> Note: The dataset is not included in this repository if the file size is too large.  
> You can use a public waste classification dataset from Kaggle or another open dataset source.

## Methodology

This project uses several image recognition and deep learning techniques:

1. **Image Preprocessing**  
   Images are resized, normalized, and prepared before being passed into the model.

2. **Data Augmentation**  
   Augmentation is used to improve model generalization by applying transformations such as rotation, flipping, and color adjustment.

3. **Wavelet-Based Preprocessing**  
   Wavelet transformation is used to separate low-frequency and high-frequency image components.  
   This helps the model capture shape, edge, and texture information.

4. **Transfer Learning**  
   The model uses MobileNetV3 as a pretrained backbone.

5. **Fine-Tuning**  
   Some layers of the pretrained model are unfrozen and retrained to adapt the model to the waste classification task.

6. **Model Evaluation**  
   The model is evaluated using accuracy, F1-score, and confusion matrix.

7. **Application Demo**  
   A simple Gradio app is used to demonstrate the prediction process interactively.

## Model

The model used in this project is **MobileNetV3**.

MobileNetV3 is selected because it is:

- Lightweight
- Efficient
- Suitable for image classification
- Practical for application deployment
- Faster compared to larger CNN models

## Final Output

The final output of this project is an interactive image recognition application.

The user can upload a waste image, and the application will return prediction results such as:

```text
Plastic: 92%
Glass: 4%
Metal: 2%
Paper: 1%
Trash: 1%
```

The highest confidence score is selected as the predicted waste category.

## Application Demo

The application is built using **Gradio**.

Basic workflow:

1. User uploads an image
2. The image is preprocessed
3. The trained model predicts the waste category
4. The application displays the prediction result and confidence score

## Notebook File

The main notebook file is:

```text
Smart_Waste_Sorting.ipynb
```

This notebook contains the complete workflow, including:

- Library installation and import
- Dataset preparation
- Image preprocessing
- Wavelet transformation
- Model building
- Model training
- Fine-tuning
- Model evaluation
- Prediction testing
- Gradio application demo

## Installation

Install the required libraries using:

```bash
pip install -r requirements.txt
```

If `requirements.txt` is not available, install the main dependencies manually:

```bash
pip install torch torchvision numpy pandas matplotlib scikit-learn opencv-python Pillow PyWavelets gradio tqdm
```

## How to Run

### Option 1: Run in Jupyter Notebook

```bash
jupyter notebook Smart_Waste_Sorting.ipynb
```

### Option 2: Run in Google Colab

1. Open Google Colab
2. Upload `Smart_Waste_Sorting.ipynb`
3. Upload or connect the dataset
4. Run the notebook cells from top to bottom

## Repository Structure

Recommended repository structure:

```text
smart-waste-sorting/
├── Smart_Waste_Sorting.ipynb
├── README.md
├── requirements.txt
├── .gitignore
└── sample_images/
    ├── plastic_example.jpg
    └── paper_example.jpg
```

## Evaluation Metrics

The model performance can be evaluated using:

- Accuracy
- Macro F1-score
- Confusion matrix

These metrics help measure how well the model classifies each waste category.

## Improvement

The main improvement in this project is the combination of:

- MobileNetV3 transfer learning
- Wavelet-based image preprocessing
- Fine-tuning
- Gradio-based application prototype

Wavelet preprocessing helps enhance texture and edge information, which can improve image recognition performance.

## Limitations

This project has several limitations:

- The model works best with single-object waste images
- Performance depends on dataset quality and size
- Complex backgrounds may reduce prediction accuracy
- Multiple objects in one image may require object detection or segmentation

## Future Work

Future improvements may include:

- Using YOLO for multiple waste object detection
- Using segmentation models such as U-Net or SAM
- Adding voice input for multimodal interaction
- Deploying the model to mobile or web applications
- Using user feedback to improve the model over time

## Conclusion

This project demonstrates how image recognition and deep learning can be applied to solve a real-world environmental problem.

By combining MobileNetV3, wavelet preprocessing, fine-tuning, and a Gradio application demo, this project shows a practical prototype for smart waste sorting.

## Author

Created for Image Recognition course project.  
Topic: Smart Waste Sorting Using Deep Learning.
