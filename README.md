# Real-Time Object Detection with SSD and MobileNet

This project demonstrates a real-time object detection system using the **Single Shot Multibox Detector (SSD)** with a pre-trained **MobileNet** model. The code uses the OpenCV Deep Neural Network (DNN) module to perform detection on a video stream.

## Features

- **Real-Time Detection**: Detect objects in real-time from live video or a pre-recorded video file.
- **GPU Acceleration**: Utilizes CUDA for enhanced performance (if available).
- **Pre-Trained Model**: MobileNet SSD, trained on 20 object categories.

## Prerequisites

- Python 3.x
- OpenCV (`cv2`) with DNN module
- NumPy
- imutils

## Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/your-username/object-detection-ssd.git
   cd object-detection-ssd
   ```

2. Install the required Python packages:

   ```bash
   pip install opencv-python imutils numpy
   ```

3. Download the pre-trained model files:
   - `MobileNetSSD_deploy.prototxt`
   - `MobileNetSSD_deploy.caffemodel`

   Place these files in the `ssd_files/` directory.

## Usage

1. Modify the script as needed:
   - To enable live video detection, set `live_video = True`.
   - To use a pre-recorded video file, place it in the same directory as the script and set the path in `cv2.VideoCapture('test.mp4')`.

2. Run the script:

   ```bash
   python Obj_detection_SSD.py
   ```

3. Press `ESC` to exit the live detection window.

## Object Categories

The model can detect the following categories:
- aeroplane, bicycle, bird, boat, bottle, bus, car, cat, chair, cow
- dining table, dog, horse, motorbike, person, potted plant, sheep
- sofa, train, TV monitor

## Example Output

The detection results will display bounding boxes and confidence scores for each detected object on the video stream.

## Performance

- The script measures and prints the elapsed time and frames per second (FPS) after detection.

## Troubleshooting

- **Error loading model**: Ensure the model files are correctly placed in the `ssd_files/` directory.
- **Low FPS**: Check if GPU acceleration is enabled and the system supports CUDA.

## Acknowledgements

This project utilizes the MobileNet SSD model, an efficient and lightweight network architecture suitable for embedded and real-time applications.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---
