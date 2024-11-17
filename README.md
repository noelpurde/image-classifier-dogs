# Dog Image Classifier

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
```

## Project Rubric

| **Category**                | **Criteria**                                                                                     | **Submission Requirements**                                                                                  |
|-----------------------------|-------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| **Timing Code**             | Implementing Time functions.                                                                    | Student calls the time functions before the start of the main code and after the main logic has been finished. |
| **Command Line Arguments**  | Question 1: Enable `--dir` argument                                                             | Adds command line argument for `--dir`; uses default = `pet_images/`.                                       |
|                             | Question 2: Enable `--arch` argument                                                            | Adds command line argument for `--arch`; default = `vgg`.                                                   |
|                             | Question 3: Enable `--dogfile` argument                                                         | Adds command line argument for `--dogfile`; default = `dognames.txt`.                                       |
| **Pet Image Labels**        | Dictionary returned is in the correct format.                                                   | Dictionary key and label are in the correct format and retrieves 40 key-value pairs. Example: `{'Poodle_07956.jpg': ['poodle'], 'fox_squirrel_01.jpg': ['fox squirrel'], ...}` |
|                             | Correct Function Call                                                                           | `in_arg.dir` is passed as an argument inside `check_images.py` while calling the `get_pet_labels` function. |
| **Classifying Images**      | Correct Function Call                                                                           | Appends `images_dir` to each value before making the function call: `classifier(images_dir + users_key, model)`. |
|                             | Output Formatting                                                                              | Converts the output to lowercase and strips any whitespaces. Verifies and stores results appropriately. Displays output when the function call is made. Appends `1` to correct label and `0` to falsely classified values. |
| **Classifying Labels as Dogs** | Matches between Classifier and Pet Image Labels correctly classify both labels as "dogs" or "not dogs." | Check the displayed output to verify all matches are appropriately displayed.                               |
|                             | Non-matches between Classifier and Pet Image Labels correctly classify each label as "dogs" or "not dogs." | Check the displayed output to verify all non-matches are appropriately displayed.                           |
| **Results**                 | Accurate overall scores for three models by running `run_models_batch.sh` after writing all the code. | All three models score as expected.                                                                         |

