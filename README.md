# Digit Recognizer Challenge on Kaggle

## Introduction
This repository contains my solution to the "Digit Recognizer" challenge on Kaggle. The goal of this challenge is to build a machine learning model that can accurately recognize hand-written digits. Although it's often considered the "hello world" of machine learning, this challenge serves as a great educational platform to grasp fundamental concepts in deep learning.

## Framework Used
For this challenge, I utilized TensorFlow, one of the most popular deep learning frameworks. TensorFlow offers a wide range of tools and resources for building, training, and evaluating neural networks, making it an excellent choice for this task.

## Callback for Achieving High Accuracy
To ensure that the model achieved a high level of performance, I implemented a custom callback that monitors the training process. Specifically, the callback was designed to stop training once an accuracy of 99.9% was achieved. This not only demonstrates the potential of neural networks but also emphasizes the importance of setting appropriate performance goals.

## Traditional Neural Network
In my initial approach, I trained a traditional neural network. Here's a simplified version of the model:

```python
model = tf.keras.models.Sequential([
    keras.layers.Flatten(input_shape=(28, 28)),
    keras.layers.Dense(128, activation='relu'),
    keras.layers.Dense(10, activation='softmax')
])
```

## Convolutional Neural Network (CNN)

Subsequently, I explored the use of Convolutional Neural Networks (CNNs) to tackle the problem. CNNs are particularly well-suited for image-related tasks. Here's a simplified version of the CNN model:
```python
model = tf.keras.models.Sequential([
    tf.keras.layers.Conv2D(32, (5, 5), activation='relu', input_shape=(28, 28, 1)),
    tf.keras.layers.MaxPooling2D(2, 2),
    tf.keras.layers.Conv2D(64, (5, 5), activation='relu'),
    tf.keras.layers.MaxPooling2D(2, 2),
    tf.keras.layers.Flatten(),
    tf.keras.layers.Dense(512, activation='relu'),
    tf.keras.layers.Dense(10, activation='softmax')
])
```

## Conclusion

This challenge serves as an educational experience to highlight key deep learning concepts. By using TensorFlow, creating a callback for accuracy goals, and exploring both traditional neural networks and CNNs, I was able to gain insights into the power of neural networks for image recognition tasks. The code in this repository represents my approach to solving the "Digit Recognizer" challenge.

Feel free to explore the code and adapt it to your own projects. Good luck with your machine learning journey!
