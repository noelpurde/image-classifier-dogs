# Dog Breed Image Classifier

This repository contains a project for classifying images of dogs using a pre-trained Convolutional Neural Network (CNN). Built as part of Udacity's **AI Programming with Python** course, this project demonstrates the use of CNN architectures, such as VGG, in identifying specific dog breeds from images. 

## Project Overview

The program accepts a directory of dog images and classifies each image by breed, displaying various classification statistics. It includes a set of evaluation metrics to provide insight into the model’s performance, such as accuracy for identifying dogs, correct breed classification, and misclassified images.

## Key Features

- **Supported CNN Models:** The classifier supports multiple architectures (e.g., VGG).
- **Image Classification:** Identifies each image as a dog or not-a-dog, and, if a dog, attempts to predict the correct breed.
- **Performance Statistics:** Reports metrics such as the percentage of correct classifications, breed accuracy, and overall match percentage.
- **Misclassification Detection:** Lists dogs misclassified as other breeds and non-dog images classified incorrectly as dogs.

## Setup Instructions

### Prerequisites

- Python 3.10
- Required packages (see `requirements.txt` for installation details).

### Running the Program

To run the classifier, provide the image directory, model architecture, and dog breed file as command-line arguments:

```bash
python main.py --dir pet_images/ --arch vgg --dogfile dognames.txt
