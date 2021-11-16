# Detection of Products in a Shelf

## Purpose of the Project
This is my capstone project for a data science bootcamp (The Data Incubator). It detects two different products and four different design features of a shelf. I confine myself to two products and four design features because I annotate the data myself. The project is easily scalable.

## Description
The project follows the TensorFlow Object Detection API Tutorial. The GitHub repository does not include the images and labelling. To train the model on a different set of images, include them in the images folder and annotate them as explained in the TensorFlow tutorial.

The Jupyter notebook data_exploration.ipynb provides a feel for how the data looks like. It uses functions defined in object_detection_sabine.py. The notebook main.ipynb trains the model using the TensorFlow folder. 

## Annotation
I annotate the data myself with LabelImg making sure that...

* ... the bounding boxes contain the entire object and are tight.
* ... occluded objects are labelled including the occluded part.
* ... all objects in the images are labelled.

I annotate the products of interest, design features of displays, and shelves.

## Relabelling of Annotation
I use this repo for different purposes. Since I do not want to go through the entire code when filenames and annotations change, I have a script that relabels the train and test data (relabel_train.ipynb) as well as a script that relabels the analyzed data (relabel_analysis.ipynb). The relation between old labels and new labels are saved in an npy-file.