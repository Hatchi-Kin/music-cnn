# Music Genre Classification

This project aims to classify music genres using a custom Convolutional Neural Network (CNN) trained on spectrograms of songs. The project is divided into several parts, each contained in different folders.

## Project Structure

- **preprocessing**: Contains all the scripts used to create the database of all the sound files used for the project.
- **beat_openl3**: Contains all the scripts to create a dataset in the PyTorch `ImageFolder` format and then train a custom CNN to detect musical genres in songs based on spectrograms. It also logs the training process in MLflow.
- **utils**: Contains utilities related to the pretrained OpenL3 model that we are trying to outperform with our own model.

