# SignSpeak

![SignSpeak Logo](https://github.com/Mukunj-21/SignSpeak/raw/main/Images/Logo.png)

## Breaking Communication Barriers: Real-time Sign Language Detection and Translation

SignSpeak is an advanced, machine learning-powered application that bridges the communication gap between the hearing and deaf communities through real-time sign language recognition and translation.

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Python](https://img.shields.io/badge/Python-3.7+-blue.svg)](https://www.python.org/downloads/)
[![TensorFlow](https://img.shields.io/badge/TensorFlow-2.x-orange.svg)](https://www.tensorflow.org/)
[![OpenCV](https://img.shields.io/badge/OpenCV-4.x-green.svg)](https://opencv.org/)

## Features

- **Real-time Sign Language Detection**: Accurately recognizes American Sign Language (ASL) hand gestures through your webcam
- **Text-to-Speech Output**: Converts detected signs into audible speech for seamless communication
- **Responsive Web Interface**: Access the application from any device with a modern browser
- **High Detection Accuracy**: Powered by a custom-trained Convolutional Neural Network (CNN)
- **Low Latency**: Optimized for real-time performance with minimal delay
- **Educational Mode**: Learn sign language with interactive tutorials and practice exercises

## Screenshots

<div align="center">
  <img src="https://github.com/Mukunj-21/SignSpeak/raw/main/Images/Interface.png" alt="SignSpeak Interface" width="600"/>
  <p><i>SignSpeak Web Interface with Real-time Detection</i></p>
</div>

## Installation

### Prerequisites

- Python 3.10 (Recommended)
- Webcam or camera device
- Internet connection (for initial setup)

### Quick Install

1. Clone the repository:

   ```bash
   git clone https://github.com/sharonn-madan/SignSpeak.git
   cd SignSpeak
   ```

2. Create and activate a virtual environment:

   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. Install dependencies:

   ```bash
   pip install -r requirements.txt
   ```

4. Start the application:

   ```bash
   python app.py
   ```

5. Open your browser and visit:
   ```
   http://localhost:5000
   ```

## How It Works

SignSpeak uses a landmark-based approach rather than processing raw pixels, leading to a highly efficient pipeline:

1. **Webcam Input**: The application captures video from the webcam using OpenCV.
2. **Hand Landmark Detection**: Each frame is processed by MediaPipe, which detects the user's hand and generates a 21-point skeletal model.
3. **Feature Engineering**: The coordinates of these 21 landmarks are normalized to make them independent of the hand's position and scale in the frame. This creates a 42-point feature vector.
4. **Classification**: The feature vector is fed into a pre-trained Random Forest Classifier which predicts the corresponding ASL sign.
5. **User Interface**: The prediction is displayed on the Flask-powered web interface. A stabilization buffer and delay are used to ensure a smooth and accurate user experience.



## Model Architecture

The model is a Random Forest Classifier from the Scikit-learn library, chosen for its speed and effectiveness with tabular data.:

- Model: RandomForestClassifier()
- Input Features: A 42-element vector representing the normalized x and y coordinates of 21 key hand landmarks.
- Dataset: The model was trained on a custom-built dataset of 3,800 images (100 samples for each of 38 classes), which were converted into landmark feature vectors. This approach makes the model lightweight and robust.

## Technology Stack

- **Backend**: Python, Flask
- **Machine Learning**: Scikit-learn, MediaPipe, OpenCV
- **Frontend**: HTML, CSS, JavaScript
- **Data Processing**: NumPy

## Future Roadmap

- [X] ASL alphabet and number recognition
- [x] Real-time web interface with text-to-speech
- [x] Gesture stabilization and usability enhancements
- [ ] Improve Model Generalization: Expand the dataset with more samples from a diverse group of users to reduce overfitting and improve accuracy.
- [ ] Support for Dynamic Gestures: Implement an RNN/LSTM model to recognize full words and phrases that involve movement.
- [ ] Mobile Application Development: Package the application for iOS and Android for wider accessibility.
- [ ] Offline Mode Functionality: Allow the application to run without an internet connection.

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- The open-source communities behind Scikit-learn, MediaPipe, OpenCV, and Flask.

## Contact

Project Creator: Sharon Madan - [GitHub Profile](https://github.com/sharonn-madan)

Project Link: [https://github.com/sharonn-madan/SignSpeak](https://github.com/sharonn-madan/SignSpeak)

---

<p align="center">Made with ❤️ for the deaf and hard-of-hearing community</p>
