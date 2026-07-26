# 👕 Fashion MNIST Clothing Classification using TensorFlow

A beginner-friendly Deep Learning project that classifies grayscale clothing images into one of **10 fashion categories** using an **Artificial Neural Network (ANN)** built with **TensorFlow/Keras**.

This project demonstrates the complete Deep Learning workflow—from loading data and preprocessing to training, evaluating, and making predictions.

---

## 📌 Project Overview

The model is trained on the **Fashion MNIST** dataset, which contains **70,000 grayscale images** of clothing items.

Each image is:
- 28 × 28 pixels
- Grayscale
- Belongs to one of 10 classes

The dataset is divided into:
- **60,000** Training Images
- **10,000** Testing Images

---

## 🎯 Objective

Build an Artificial Neural Network that can accurately classify clothing images into one of the following categories:

| Label | Class |
|--------|----------------|
| 0 | T-shirt/Top |
| 1 | Trouser |
| 2 | Pullover |
| 3 | Dress |
| 4 | Coat |
| 5 | Sandal |
| 6 | Shirt |
| 7 | Sneaker |
| 8 | Bag |
| 9 | Ankle Boot |

---

## 🛠️ Technologies Used

- Python
- TensorFlow
- Keras
- NumPy
- Matplotlib

---

## 📂 Project Structure

```
Fashion-MNIST-Classification/
│
├── fashion_classifier.ipynb
├── README.md
├── requirements.txt
```

---

## 🚀 Workflow

1. Import Libraries
2. Load Fashion MNIST Dataset
3. Normalize Image Data
4. Visualize Sample Images
5. Build ANN Model
6. Compile the Model
7. Train the Model
8. Evaluate Performance
9. Predict New Images

---

## 🧠 Model Architecture

```
Input Layer
(28 × 28)

↓

Flatten Layer
(784 neurons)

↓

Dense Layer
128 neurons
ReLU Activation

↓

Output Layer
10 neurons
Softmax Activation
```

---

## ⚙️ Model Compilation

```python
model.compile(
    optimizer="adam",
    loss="sparse_categorical_crossentropy",
    metrics=["accuracy"]
)
```

### Optimizer
- Adam

### Loss Function
- Sparse Categorical Crossentropy

### Metric
- Accuracy

---

## 📈 Model Training

```python
history = model.fit(
    X_train,
    y_train,
    epochs=10,
    validation_split=0.2
)
```

During training, the model learns by:
- Forward Propagation
- Loss Calculation
- Backpropagation
- Weight Updates using Adam Optimizer

---

## 📊 Model Evaluation

```python
loss, accuracy = model.evaluate(X_test, y_test)
```

Example Output:

```
Test Accuracy: 89%
```

*(Accuracy may vary depending on training.)*

---

## 🔍 Making Predictions

```python
predictions = model.predict(X_test)

predicted_class = np.argmax(predictions[0])

print(predicted_class)
```

The model outputs probabilities for all 10 classes and predicts the class with the highest probability.

---

## 📷 Sample Prediction

```
Actual Label    : Sneaker

Predicted Label : Sneaker

Prediction Confidence : 99.2%
```

---

## 📚 Concepts Covered

- Artificial Neural Networks (ANN)
- TensorFlow & Keras
- Sequential API
- Dense Layers
- Flatten Layer
- ReLU Activation
- Softmax Activation
- Optimizers
- Loss Functions
- Model Training
- Model Evaluation
- Image Classification
- Prediction

---

## 💻 Installation

Clone the repository

```bash
git clone https://github.com/your-username/Fashion-MNIST-Classification.git
```

Move into the project folder

```bash
cd Fashion-MNIST-Classification
```

Install dependencies

```bash
pip install -r requirements.txt
```

Run the notebook

```bash
jupyter notebook
```

---

## 📦 Requirements

```
tensorflow
numpy
matplotlib
jupyter
```

---

## 🎓 Learning Outcomes

After completing this project, you will understand:

- How TensorFlow works
- How to build an ANN using Keras
- Data preprocessing techniques
- Neural network architecture
- Model compilation and training
- Performance evaluation
- Image classification
- Making predictions using trained models

---

## 🔮 Future Improvements

- Improve model accuracy
- Add Dropout layers to reduce overfitting
- Build a Convolutional Neural Network (CNN)
- Hyperparameter tuning
- Save and load trained models
- Deploy the model using Streamlit or Flask

---

## 👨‍💻 Author

**Prajju**

Computer Science Engineering (AI & ML)

---

## ⭐ If you found this project helpful

Give this repository a ⭐ on GitHub and feel free to fork it for learning and experimentation!
