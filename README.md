# Priyanka-Deep-learning-assignment2-
MNIST Handwritten Digit Classification using Neural Network

📌 Project Overview

This project implements a Neural Network model using TensorFlow and Keras to classify handwritten digits from the MNIST dataset.

The model learns to recognize digits from 0 to 9 using 28×28 grayscale images. The project also includes data preprocessing, model training, evaluation, visualization of training performance, prediction on test images, and experimentation with different model architectures.

---

🎯 Objectives

- Load and explore the MNIST handwritten digit dataset.
- Preprocess and normalize image data.
- Build a neural network using TensorFlow/Keras.
- Train the model on handwritten digit images.
- Evaluate the model using test data.
- Visualize training and validation accuracy/loss.
- Test the model on individual handwritten images.
- Experiment with different neural network architectures.

---

🗂️ Dataset

The project uses the MNIST dataset, which contains handwritten digits from 0 to 9.

- Training images: 60,000
- Test images: 10,000
- Image size: 28 × 28 pixels
- Image type: Grayscale
- Number of classes: 10 (digits 0–9)

The dataset is loaded directly using TensorFlow:

tf.keras.datasets.mnist.load_data()

---

🛠️ Technologies Used

- Python
- TensorFlow
- Keras
- NumPy
- Matplotlib
- Google Colab

---

🔄 Project Workflow

The project is divided into the following steps:

Step 1: Load and Explore the MNIST Dataset

The MNIST dataset is loaded using TensorFlow. The shape of the training and testing datasets is displayed, and sample images are visualized.

Step 2: Preprocess the Data

Pixel values range from 0 to 255. They are normalized to a range between 0 and 1:

train_images = train_images / 255.0
test_images = test_images / 255.0

Normalization helps the neural network train more effectively.

Step 3: Build the Neural Network

The model consists of:

- Flatten layer to convert 28×28 images into a one-dimensional vector.
- Dense layer with 128 neurons and ReLU activation.
- Dropout layer with a rate of 0.2.
- Dense layer with 64 neurons and ReLU activation.
- Output layer with 10 neurons and Softmax activation.

Input Image (28 × 28)
        ↓
     Flatten
        ↓
Dense (128, ReLU)
        ↓
Dropout (0.2)
        ↓
Dense (64, ReLU)
        ↓
Dense (10, Softmax)
        ↓
Predicted Digit (0–9)

Step 4: Compile the Model

The model is compiled using:

- Optimizer: Adam
- Loss Function: Sparse Categorical Crossentropy
- Metric: Accuracy

Step 5: Train the Model

The model is trained for 10 epochs with 20% of the training data used for validation.

history = model.fit(
    train_images,
    train_labels,
    epochs=10,
    validation_split=0.2
)

Step 6: Evaluate the Model

The trained model is evaluated using the MNIST test dataset.

The final test accuracy is displayed as:

Test Accuracy: XX.XX%

The exact accuracy may vary slightly between training runs.

Step 7: Visualize Training

Training and validation performance are visualized using two graphs:

1. Training vs. validation accuracy
2. Training vs. validation loss

These graphs help understand how the model performs during training.

Step 8: Test on Handwritten Images

Five images from the test dataset are selected and passed through the trained model.

For each image, the program displays:

- The image
- Actual digit
- Predicted digit

Step 9: Experiment with Model Variations

A second model is created with a different architecture:

- Dense layer with 256 neurons
- Dropout of 0.3
- Dense layer with 128 neurons
- Output layer with 10 neurons

This allows comparison between different neural network architectures.

---

📊 Model Architecture

Original Model

Layer| Configuration
Input| 28 × 28
Flatten| Converts image to 1D
Dense| 128 neurons, ReLU
Dropout| 0.2
Dense| 64 neurons, ReLU
Output| 10 neurons, Softmax

Experimental Model

Layer| Configuration
Input| 28 × 28
Flatten| Converts image to 1D
Dense| 256 neurons, ReLU
Dropout| 0.3
Dense| 128 neurons, ReLU
Output| 10 neurons, Softmax

---

📈 Results

The model is evaluated using the MNIST test dataset.

The project generates:

- Test accuracy
- Training accuracy graph
- Validation accuracy graph
- Training loss graph
- Validation loss graph
- Predictions for five test images

The exact test accuracy depends on the training run and environment.

---

📁 Project Structure

MNIST-Neural-Network/
│
├── MNIST_Neural_Network.ipynb
├── README.md
└── requirements.txt

If using Google Colab, the notebook can be opened directly in Google Colab.

---

🚀 How to Run

Option 1: Google Colab

1. Open the ".ipynb" notebook in Google Colab.
2. Run the cells from Step 1 to Step 9.
3. The MNIST dataset will be downloaded automatically.
4. View the accuracy, graphs, and predictions.

Option 2: Local Python Environment

Install the required libraries:

pip install tensorflow numpy matplotlib

Then open the Jupyter Notebook and run the cells sequentially.

---

🔗 Google Colab

Google Colab Notebook:
https://share.google/MRTAK6vK6bvFBdJj7

---

💡 Key Learning Outcomes

Through this project, I learned:

- How to load and explore image datasets.
- Image normalization and preprocessing.
- Building neural networks using Keras.
- Using ReLU and Softmax activation functions.
- Model compilation and training.
- Evaluating classification models.
- Visualizing training and validation performance.
- Making predictions using a trained neural network.
- Experimenting with different model architectures.

---

🔮 Future Improvements

The project can be further improved by:

- Increasing or tuning the number of hidden layers.
- Experimenting with different learning rates.
- Using Convolutional Neural Networks (CNNs).
- Applying data augmentation.
- Comparing multiple optimizers.
- Comparing different dropout rates.
- Generating a confusion matrix.
- Comparing the performance of different architectures.

---

👩‍💻 Author

Priyanka Madankar

B.E. – Information Technology (AIML)

---

📜 License

This project is created for educational and academic purposes.
