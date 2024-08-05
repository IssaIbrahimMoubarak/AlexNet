# Project: Plant Leaf Image Classification 🌿

## Description

This project involves training a Convolutional Neural Network (CNN) model based on the AlexNet architecture to classify images of plant leaves. The goal is to accurately identify the categories of leaves among three predefined classes.

## Installation

### Prerequisites

Ensure that the following libraries are installed in your Python environment:

- Python 3.x
- OpenCV (`cv2`)
- NumPy (`numpy`)
- PIL (Pillow)
- Matplotlib (`matplotlib`)
- Keras (`keras`)

You can install the dependencies via pip:

```bash
pip install opencv-python numpy pillow matplotlib keras
```

## Usage

### 1. Data Acquisition

Place the leaf images in a directory structured by classes. Ensure your images are organized in the following structure:

```
/path_to_data/
    ├── Class_1/
    │   ├── image_1.jpg
    │   ├── image_2.jpg
    │   └── ...
    ├── Class_2/
    │   ├── image_1.jpg
    │   └── ...
    └── Class_3/
        ├── image_1.jpg
        └── ...
```

### 2. Image Reading and Preprocessing

The script reads the images from the specified directory, resizes them to 100x100 pixels, and normalizes them to prepare the data for model training.

```python
[X_train, y_train] = read_images("/path_to_data")
```

### 3. Model Training

The AlexNet model is constructed and trained on the preprocessed images. The main hyperparameters are defined as follows:

- Number of epochs: 10
- Batch size: 64
- Optimizer: Adam

```python
history = model.fit(train_features, train_targets, batch_size=BATCH_SIZE, epochs=NB_EPOCH, verbose=VERBOSE)
```

### 4. Model Saving

The trained model is saved to a file named `AlexNet_groupe_2.h5` for future use.

```python
model.save("AlexNet_groupe_2.h5")
```

### 5. Results

The model was tested over 10 runs, achieving an average accuracy of **96.43%**.

## Image Visualization

The script also provides a function to display images from the dataset.

```python
plot_images(X_train, total_images=2, rows=1, cols=2, fsize=(10, 50), title='Training Dataset')
```

## Author

This project was created by ISSA IBRAHIM Moubarak.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
