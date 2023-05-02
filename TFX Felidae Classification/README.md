# Felidae Image Classification using TFX Pipeline
This project aims to classify images of the Felidae family using TensorFlow and TFX (TensorFlow Extended). The Felidae family includes a variety of species like lions, tigers, and leopards. The goal is to identify the species of Felidae in a given image using a custom TFX pipeline. The pipeline will be implemented localy with a ContextIterator to run through it. It is expected in later versions to use Apache Airflow as an orchestrator. 

This is still a work in progress. 

## Table of Contents
[Problem Definition](#problem-definition)
[TFX Pipeline](#tfx-pipeline)
[Data Preparation](#data-preparation)
[Transformations](#transformations)
[Model Training](#model-training)
[Model Evaluation](#model-evaluation)
[Deployment](#model-deployment)
[Resources](#resources)

Problem Definition <a name="problem-definition"></a>
The goal of this project is to develop a machine learning pipeline capable of learning the unique features and characteristics of different Felidae species and classify images accordingly. The primary challenge lies in capturing the essence of each species and differentiating them from one another.

TFX Pipeline <a name="tfx-pipeline"></a>
The TFX pipeline consists of several components that process the data, train the model, and evaluate its performance. The pipeline includes components for data ingestion, data transformation, model training, model evaluation, and deployment.

Data Preparation <a name="data-preparation"></a>
The dataset consists of images of different Felidae species. The images are stored in the felidae_images folder, with each subfolder representing a different species. The images are converted to the TFRecord format and saved in the felidae_tfrecords_split folder. The dataset is split into training and evaluation sets with an 80/20 ratio.

Transformations <a name="transformations"></a>
The images are preprocessed using a custom transformation function. The preprocessing steps include resizing the images, normalizing the pixel values, and converting the labels to integers. These transformations are applied to the raw data during the pipeline execution.

Model Training <a name="model-training"></a>
The model is trained using the preprocessed data. A custom training module is implemented using TensorFlow and Keras. The model architecture consists of a series of convolutional and pooling layers, followed by fully connected layers and an output layer for classification.

Model Evaluation <a name="model-evaluation"></a>
The model performance is evaluated using the evaluation dataset. The pipeline calculates evaluation metrics, such as accuracy, precision, recall, and F1 score. These metrics help assess the model's performance and identify areas for improvement.

Deployment <a name="deployment"></a>
Once the model is trained and evaluated, it can be deployed using TensorFlow Serving. This allows the model to be used for real-time image classification tasks.

Resources <a name="resources"></a>
TensorFlow Extended (TFX): https://www.tensorflow.org/tfx
TFX User Guide: https://www.tensorflow.org/tfx/guide
TFX ExampleGen: https://www.tensorflow.org/tfx/guide/examplegen
TFX Transform: https://www.tensorflow.org/tfx/guide/transform
TFX Trainer: https://www.tensorflow.org/tfx/guide/trainer
TFX Evaluator: https://www.tensorflow.org/tfx/guide/evaluator
Dataset: https://www.kaggle.com/datasets/juliencalenge/felidae-tiger-lion-cheetah-leopard-puma
