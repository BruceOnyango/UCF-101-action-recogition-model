# UCF-101-action-recogition-model
This project involves developing an action recognition model that identifies different types of actions in video clips. The model is trained using the UCF-101 dataset, which is a large-scale action recognition dataset consisting of 13,320 video clips distributed across 101 action categories.

### Project Title: Action Recognition Model Using UCF-101 Dataset
### Description
This project involves developing an action recognition model that identifies different types of actions in video clips. The model is trained using the UCF-101 dataset, which is a large-scale action recognition dataset consisting of 13,320 video clips distributed across 101 action categories.

Key Details
### Dataset
Name: UCF-101
Description: UCF-101 is a dataset of 101 human actions, including activities like "Playing Guitar," "Swinging," "Archery," and "Biking."
Number of Videos: 13,320
Categories: 101
### Model
- **Type**: Sequential Convolutional Neural Network (CNN)
- **Architecture Details**:
  - **Layers**:
    - Input Layer: `Input(shape=(64, 64, 3))`
    - Conv2D Layer 1: `Conv2D(32, (3, 3), activation='relu')`
    - MaxPooling Layer 1: `MaxPooling2D(pool_size=(2, 2))`
    - Conv2D Layer 2: `Conv2D(64, (3, 3), activation='relu')`
    - MaxPooling Layer 2: `MaxPooling2D(pool_size=(2, 2))`
    - Dropout Layer 1: `Dropout(0.25)`
    - Flatten Layer: `Flatten()`
    - Dense Layer 1: `Dense(128, activation='relu')`
    - Dropout Layer 2: `Dropout(0.5)`
    - Output Layer: `Dense(101, activation='softmax')`
  - **Number of Parameters**: 3,107,557 (Example, replace with the actual number from `model.summary()`)

Framework: TensorFlow
Training
Training Accuracy: 0.9049
Training Loss: 0.3851
Epochs: 200
Batch Size: 2 (this was due to memory issues adjust to your fitting)
Optimizer: Adam
Validation Accuracy: 0.9379
Validation Loss: 0.2859
Evaluation Metrics: Accuracy
### Results
Overall Performance: The model achieved a training accuracy of 0.9049 with a loss of 0.3851, indicating strong performance in recognizing a variety of actions from the dataset.
Challenges and Considerations
### Computational Resources: 
Hardware Specifications:
    -System Configuration:
    -CPU: Intel i5-5200U
    -RAM: 8 GB
    -Storage: 500 HDD
    -Environment Setup:
    -Operating System:  Windows 10
    -Deep Learning Framework: TensorFlow 2.16
    -Training Duration:
    -Total Training Time: Approximately 3-4 hours
    -Training Sessions: Continuous training session
    -Resource Utilization:
    -CPU Utilization: Between 85% and 96%
### Future Work
# Improvements:  using different model architectures
  Using Different Model Architectures:
  -3D-CNNs: Utilize 3D Convolutional Neural Networks to capture temporal information in video sequences.
  -RNNs/LSTMs: Integrate Recurrent Neural Networks or Long Short-Term Memory networks for better sequence modeling of actions over time.
  -Two-Stream Networks: Implement two-stream networks that separately process spatial and temporal features from video data.
  -Transformers: Explore transformer-based architectures for improved attention mechanisms and better sequence processing.
  -Hybrid Models: Combine CNNs with RNNs or transformers to leverage both spatial and temporal features effectively.
# Applications:  potential applications of the model in real-world scenarios
  -Surveillance: Apply the model for real-time action recognition in security systems.
  -Sports Analysis: Use the model to analyze and classify actions in sports footage.
  -Human-Computer Interaction: Integrate the model into systems for gesture and action recognition to enhance user interaction.
