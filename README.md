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
   git clone https://github.com/Mukunj-21/SignSpeak.git
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

SignSpeak uses a deep learning approach to recognize sign language gestures:

1. **Hand Detection**: OpenCV processes webcam input to isolate hand regions
2. **Feature Extraction**: Key points and hand shapes are identified and normalized
3. **Classification**: Our custom CNN model classifies the hand gesture into corresponding letters/words
4. **Translation**: Recognized signs are converted to text and optionally speech
5. **User Interface**: Results are displayed in real-time through our Flask-powered web interface

## Model Architecture

Our CNN model was trained on a dataset of over 20,000 sign language images covering the ASL alphabet and common phrases. The architecture includes:

- Input layer for normalized hand images (64x64x1)
- 4 convolutional layers with max-pooling
- 2 fully connected layers
- Dropout layers to prevent overfitting
- SoftMax output layer for multi-class classification

## Technology Stack

- **Backend**: Python, Flask
- **Machine Learning**: TensorFlow, Keras, OpenCV
- **Frontend**: HTML, CSS, JavaScript, Bootstrap
- **Data Processing**: NumPy, Pandas
- **Deployment**: Docker support for easy deployment

## Future Roadmap

- [x] Basic ASL alphabet recognition
- [x] Web interface implementation
- [x] Real-time processing optimization
- [ ] Support for full ASL grammar and syntax
- [ ] Mobile application development
- [ ] Offline mode functionality
- [ ] Multi-language sign language support
- [ ] Integration with AR/VR platforms

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

- [ASL Dataset Contributors](https://www.kaggle.com/datasets/grassknoted/asl-alphabet)
- All open-source libraries and tools used in this project

## Contact

Project Creator: Sharon Madan - [GitHub Profile](https://github.com/sharonn-madan)

Project Link: [https://github.com/sharonn-madan/SignSpeak](https://github.com/sharonn-madan/SignSpeak)

---

<p align="center">Made with ❤️ for the deaf and hard-of-hearing community</p>
