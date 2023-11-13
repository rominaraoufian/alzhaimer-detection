# Alzheimer Detection
## Data
Data that is used in this project has images of diffent brain MRI which devided in 4 classes. ('VeryMildDemented', 'MildDemented', 'ModerateDemented', 'NonDemented)
You can access this data from [here](https://www.kaggle.com/datasets/tourist55/alzheimers-dataset-4-class-of-images/data)

## Preprocessing
- create dataframes for all images
- all images converted to (124,124) shape
- rescaling images
- since classes are imblance, weights were calculated for all of them and passed to fit function.
## Models
### CNN:
this model has conv2d, dropout, flatten, and dense layers.
#### Hyperparameters
- Batch size: 16
- Epochs: 30
- Channels images: 3
- optimizer: adam
### ResNet:
this model has ResNet50 pretrained model followed by flatten and dense layers.
#### Hyperparameters
- Batch size: 16
- Epochs: 30
- Channels images: 3
- optimizer: adam
- learning rate: (1e-3) * (0.1 ** (0.05 * epoch))
- early stopping: 5
### Xception:
this model has Xception pretrained mdodel followed by dense and dropout layers.
#### Hyperparameters
- Batch size: 16
- Epochs: 30
- Channels images: 3
- optimizer: adam
- learning rate: (1e-3) * (0.1 ** (0.05 * epoch))
- early stopping: 5

## Results
CNN: val_accuracy: 0.9125
ResNet: val_accuracy: 0.9047 (early stopped at 20th epoch)
Xception: val_accuracy: 0.9320 (early stopped at 16th epoch)



