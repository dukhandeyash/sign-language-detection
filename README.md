# Sign Language Detection and Translation System

This project aims to develop an efficient and accurate system capable of detecting and translating sign language gestures into written text or speech in real time. The system utilizes image processing techniques and neural networks to identify signs made through hand gestures, fingers, and facial expressions. It ensures robustness under varying lighting conditions, camera viewpoints, and background noise, making it adaptable for real-world applications.

## Features
- **Real-time Gesture Recognition**: Detects static and dynamic gestures using a combination of CNN and RNN models.
- **Robustness**: Handles variations in lighting, camera angles, and background noise.
- **Accurate Translation**: Converts recognized gestures into text, facilitating communication.
- **Efficient Workflow**: Ensures high confidence in classification and adapts by improving datasets or retraining models as necessary.

---

## Workflow

### 1. Data Acquisition
The system captures hand gestures using a camera.

### 2. Image Quality Check
Ensures the captured image meets quality standards. If not, the system retries capturing the image.

### 3. Pre-processing
Prepares the image for feature extraction through:
- Background subtraction
- Grayscale conversion
- Noise reduction

### 4. Feature Extraction
Extracts critical features like:
- Hand shape
- Finger features
- Contours

### 5. Classification
- **Static Gestures**: Classified using CNN or SVM.
- **Dynamic Gestures**: Processed using CNN followed by RNN.

### 6. Confidence Check
Verifies classification confidence. If low confidence is detected, the system triggers retraining or dataset improvements.

### 7. Translation to Text
Decodes the recognized gestures into readable text.

### 8. Display Result
Shows the translated gesture in text format.

---

## Model Training

### Training the Model
The model is trained using the AlexNet architecture, fine-tuned with the ASL dataset. Key steps include:
1. Load the dataset with labels based on folder names.
2. Adjust the final layers of AlexNet for the number of gesture classes.
3. Preprocess and resize images for training.
