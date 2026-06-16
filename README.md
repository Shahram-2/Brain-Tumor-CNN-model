# Brain-Tumor-CNN-model

This project focused on developing a deep learning model capable of automatically detecting and classifying brain tumours from medical imaging data. The goal was to build a reliable and efficient CNN-based classification system that could distinguish between three categories: glioma, pituitary tumour, and no tumour.
Using TensorFlow and Keras, a convolutional neural network was designed, trained, and evaluated on a brain cancer imaging dataset. The process began with loading and preprocessing the dataset, which involved resizing images, normalising pixel values, and structuring the data into training and validation sets to ensure the model could generalise effectively. The CNN architecture was then defined, incorporating convolutional layers for feature extraction, pooling layers to reduce dimensionality, and dense layers for final classification. The model was compiled with an appropriate loss function and optimiser before being trained over a set number of epochs, with performance monitored throughout.
The project demonstrated how deep learning can serve as a powerful tool in medical imaging, capable of identifying subtle structural patterns in brain scans that correspond to different tumour types. By automating this classification process, the system has the potential to reduce reliance on specialist interpretation, minimise human error, and support earlier and more consistent diagnosis.

codespace: Google Colab Jupyter Notebook

Image Dataset for Training, Validation, Testing:
https://brunel365-my.sharepoint.com/personal/cssrajt_brunel_ac_uk/_layouts/15/onedrive.aspx?id=%2Fpersonal%2Fcssrajt%5Fbrunel%5Fac%5Fuk%2FDocuments%2FTeaching%2FCS3002%2F7%20DeepLearning%20Part%202%2FLab%2FDataset%2FBrainTumorDataset%2Ezip&parent=%2Fpersonal%2Fcssrajt%5Fbrunel%5Fac%5Fuk%2FDocuments%2FTeaching%2FCS3002%2F7%20DeepLearning%20Part%202%2FLab%2FDataset&ga=1  


<img width="560" height="281" alt="image" src="https://github.com/user-attachments/assets/f63730aa-fc09-482b-b989-cf0a66e50d18" />

FIgure 1. Example Image Dataset



Relevant functions:

Glob

PIL.Image.open

tf.keras.utils.image_dataset_from_directory

history.history['loss']

history.history['val_loss']

tf.keras.Sequential

tf.keras.layers.Conv2D

tf.keras.layers.MaxPooling2D

tf.keras.layers.Flatten()

tf.keras.layers.Dense

model.fit(..)
