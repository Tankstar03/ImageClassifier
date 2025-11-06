# ImageClassifier
Data Science Capstone 3 (Springboard)

A dive into constructing Convolutional Neural Networks (CNN) to classify any image as either real or fake (AI generated). Details of the project include:
- Jupyter Notebooks with the python code constructing and training all the neural net models
- Modified data folder containing the images the models are trained and tested with
- Library folder that holds some helper functions
- Models folder that contains the models created from the analysis
- Problem Statement file that shows the planning and background created for this project
- Model Metrics file that contains details for each model
- Model Report that discusses the entire process of the analysis
- A Powerpoint presentation that compiles all the information of the analysis into a real life scenario where the analysis is put to good use

Each section is described in greater detail below.

[Link to Original dataset](https://www.kaggle.com/datasets/tristanzhang32/ai-generated-images-vs-real-images?search=real+vs+ai+generated)

## Jupyter Notebooks
There are 3 Jupyter Notebooks showing the analysis, development, and documentation of the dataset and CNN models throughout the project.

1. data_wrangling_&_EDA - organizing the image dataset, checking its distribution, and creating downsized varients of all 60,000 images, one version 128x128 pixels and the other 224x224 pixels. The downsized images standardize the images and prevent memory overloading.
2. preprocessing_&_modeling - load in the image datasets and construct the models that will be used to classify the images. Models include ones built from scratch and those from open sources modified to fit the task of the project.
3. documentation - graphs out multiple performance metrics between all the candidate models.

## Folders
- ### modified_data
    Contains all the downsized images that will be used for modeling. Folder contains many subfolders with all the images organized by 128x128/224x224, train/test and within real/fake.
- ### library
    Folder containing helper functions, mainly to help with writting to files. Created by Springboard.
- ### models
    Folder containing the 2 models that were concluded by the analysis to be viable candidates to serve as a base model for generalized image classification between real and fake.

## Other Files
- ### Problem Statement
    A word document that sets the backdrop for the project including significance to today's technology advancements in the field of artificial intelligence and goals for the end result.

- ### Model Metrics
    A markdown file detailing each model's:
    - layer types
    - layer count
    - head design
    Plus key performance metrics such as:
    - training accuracy/loss
    - training time
    - validation accuracy/loss
    - testing accuracy/loss

- ### Final Report
    A word document going through the entire development process of the project. Begins at the background and problem statement, ends with further topics for research and discussion and a conclusion recommending the best models for this classfication task.

- ### Image Classifier Presentation
    A PowerPoint presentation condensing the entire project into a format presentable to shareholders and non-technical audiences while maintain some level of analysis of the models.