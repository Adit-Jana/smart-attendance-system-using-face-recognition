# Smart Attendance System Using Face Recognition

## Overview
This project implements a smart attendance system using face recognition technology, allowing efficient and automated attendance tracking for educational institutions. The system utilizes various libraries for face detection and recognition.

## Features
- **Real-time face recognition**: Automatically identifies students from the video stream.
- **Attendance logging**: Maintains records of student attendance.
- **User-friendly interface**: Easy for instructors and administrators to use.

## Technologies Used
- **Python**: Core programming language
- **OpenCV**: Computer vision library for face detection and image processing
- **Haar Cascade Classifier**: Pre-trained model for face detection (haarcascade_frontalface_default.xml)
- **SQLite**: Database for storing attendance records and face data
- **NumPy**: Numerical computing library

## Project Structure
```
smart-attendance-system-using-face-recognition/
├── dataset1.py              # Dataset creation and image capture
├── train2.py                # Model training script
├── detector3.py             # Face detection module
├── drycheck.py              # Testing and validation script
├── final4.py                # Main application and recognition engine
├── end6.py                  # Utility script
├── FaceBase.db              # SQLite database for storing face data
├── attn.txt                 # Attendance log file
├── haarcascade_frontalface_default.xml  # Pre-trained face detection classifier
├── recognizer/              # Directory for trained model files
└── README.md                # This file
```

## Installation

### Prerequisites
- Python 3.6 or higher
- pip (Python package manager)
- Webcam or camera device

### Steps
1. **Clone the repository**:
   ```bash
   git clone https://github.com/Adit-Jana/smart-attendance-system-using-face-recognition.git
   cd smart-attendance-system-using-face-recognition
   ```

2. **Install required dependencies**:
   ```bash
   pip install opencv-python opencv-contrib-python numpy
   ```

## Usage

### Step 1: Capture Training Dataset
Create a dataset of face images for the system:
```bash
python dataset1.py
```
This will capture multiple images of a person's face for training purposes.

### Step 2: Train the Model
Train the face recognition model using the captured dataset:
```bash
python train2.py
```
This generates a trained recognizer model in the `recognizer/` directory.

### Step 3: Run Face Detection & Recognition
Execute the main application:
```bash
python final4.py
```
The system will:
- Detect faces in real-time using the webcam
- Recognize known faces and match them against the training data
- Log attendance records to `attn.txt`

### Step 4: Verify Results
Check the attendance log:
```bash
cat attn.txt
```

## Key Files Description

| File | Purpose |
|------|---------|
| `dataset1.py` | Captures face images and stores them for training |
| `train2.py` | Trains the face recognition model using captured images |
| `detector3.py` | Handles face detection using Haar Cascade classifier |
| `drycheck.py` | Validates the system and checks configurations |
| `final4.py` | Main application - runs the attendance system |
| `FaceBase.db` | SQLite database storing face encodings and user data |
| `attn.txt` | Text file logging attendance records with timestamps |
| `haarcascade_frontalface_default.xml` | Pre-trained classifier for face detection |

## How It Works

1. **Face Detection**: The system uses Haar Cascade Classifier to detect faces in the video stream
2. **Face Training**: Captured face images are processed and a recognizer model is trained
3. **Face Recognition**: During runtime, detected faces are compared against the trained model
4. **Attendance Logging**: Recognized faces are logged with timestamps in the attendance file

## Configuration

- Modify `dataset1.py` to adjust the number of training images captured per person
- Adjust confidence thresholds in `final4.py` to control recognition accuracy
- Update database path in scripts if needed

## Troubleshooting

| Issue | Solution |
|-------|----------|
| Camera not detected | Check camera permissions and ensure the device is connected |
| Poor recognition accuracy | Capture more images in `dataset1.py` and retrain the model |
| Database errors | Ensure `FaceBase.db` has proper read/write permissions |
| Face not detected | Ensure adequate lighting and adjust Haar Cascade parameters |

## Future Enhancements
- Add support for multiple face recognition algorithms (LBPH, Deep Learning)
- Implement web interface for easy attendance viewing
- Add email notifications for administrators
- Support for integration with existing attendance systems
- Real-time dashboard for attendance statistics

## Contributing
Contributions are welcome! Please follow these steps:
1. Fork the repository
2. Create a feature branch (`git checkout -b feature/YourFeature`)
3. Commit your changes (`git commit -m 'Add YourFeature'`)
4. Push to the branch (`git push origin feature/YourFeature`)
5. Open a Pull Request

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments
- OpenCV documentation and community
- Haar Cascade Classifier developers
- Contributors and users of this project

## Contact
For further inquiries or support, please contact:
- **Author**: Adit-Jana
- **GitHub**: [Adit-Jana](https://github.com/Adit-Jana)
- **Repository**: [smart-attendance-system-using-face-recognition](https://github.com/Adit-Jana/smart-attendance-system-using-face-recognition)