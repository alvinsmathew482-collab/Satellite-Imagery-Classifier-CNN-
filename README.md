# Satellite-Imagery-Classifier-CNN
A convolutional neural network for satellite image classification using the EuroSAT dataset, built with TensorFlow and Keras. This project classifies land cover across ten categories, inspired by a project I'd completed for geospatial analysis in humanitarian crisis detection.

**Project Overview:**

This project explores how computer vision can be applied to satellite imagery to support humanitarian decision-making. By classifying land cover types from satellite images, this system can identify crisis zones, damaged areas, and safe routes during emergencies.

**Dataset used:**

EuroSAT, a dataset of 27,000 labeled satellite images across 10 land cover classes: Annual Crop, Forest, Herbaceous Vegetation, Highway, Industrial, Pasture, Permanent Crop, Residential, River, Sea/Lake.

**Model Variants:**

3 CNN models are implemented and compared:

Model One: Balanced Baseline: Two convolutional layers with 32 and 64 filters, 128 neuron dense layer, dropout 0.5, trained for 10 epochs. Best for general-purpose.

Model Two: High Precision: Two convolutional layers with 64 and 128 filters, a 256 neuron dense layer, dropout 0.3, trained for 20 epochs. Higher accuracy, yet longer training time.

Model Three: Lightweight Fast: Two convolutional layers with 16 and 32 filters, 64 neuron dense layer, dropout 0.6, trained for 5 epochs. Fastest training, best for real-time applications.


The high precision model achieved **82% accuracy**, a 2% improvement over the baseline, at the cost of longer training time due to increased filters and epochs. The lightweight model achieved **73% accuracy**, sacrificing 7% accuracy in exchange for significantly faster training and lower computational cost. The baseline model remains the recommended choice for general use with **80% accuracy**, balancing accuracy and efficiency.

The high-precision model is suited for critical humanitarian decision-making where accuracy is paramount, while the lightweight model is ideal for real-time applications with limited computational resources.

**Future Improvements**

Train on crisis-specific datasets like flood or earthquake damage imagery

Integrate routing logic for refugee navigation

Deploy as a real-time web application


**Tech Stack**

Python, TensorFlow, Keras, NumPy, Pandas, Matplotlib, Seaborn, Google Colab

Built by Alvin.
