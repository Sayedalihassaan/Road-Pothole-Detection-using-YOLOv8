# Road Pothole Detection using YOLOv8
This project implements a real-time road pothole detection system using the YOLOv8 model for object detection and segmentation. It processes video input, identifies potholes on roads, and visualizes them with bounding boxes and segmentation masks. The project is built using Python, OpenCV, and the Ultralytics YOLO library.
Table of Contents

## Project Overview
Features
Requirements
Installation
Usage
Project Structure
Model Details
Contributing
License
Acknowledgements

Project Overview
The Road Pothole Detection project aims to enhance road safety by automatically detecting potholes in real-time from video feeds. The system uses a pre-trained YOLOv8 model (best.pt) to perform segmentation and classification of potholes in video frames. The detected potholes are highlighted with contours and labeled on the video output.
Features

Real-time pothole detection using YOLOv8 segmentation.
Visualization of potholes with contours and bounding boxes.
Customizable video input processing (e.g., resizing frames).
Support for video files (e.g., .mp4).
Easy-to-use Python script with OpenCV for video processing.

Requirements
To run this project, you need the following:

Python 3.11 or higher
A compatible video file (e.g., p.mp4)
A pre-trained YOLOv8 model file (best.pt)

Python Libraries

opencv-python
ultralytics
cvzone
numpy

Installation
Follow these steps to set up the project locally:

Clone the Repository
git clone https://github.com/your-username/road-pothole-detection.git
cd road-pothole-detection


Set Up a Virtual Environment (recommended)
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate


Install Dependencies
pip install -r requirements.txt


Download the Pre-trained Model

Place the best.pt YOLOv8 model file in the project root directory.
You can train your own model or download a pre-trained one from your source.


Prepare Video Input

Place your video file (e.g., p.mp4) in the project directory or update the video path in the script.



Usage

Ensure the best.pt model and video file (p.mp4) are in the project directory.
Run the pothole detection script:python road_pothole_detection.py


The script will:
Load the video and process it frame by frame.
Detect potholes and display them with contours and labels.
Show the output in a window titled "Road Pothole Detection".


Press q to exit the video processing.

Example Output
The output window displays the video with:

Red contours around detected potholes.
Yellow text labels indicating the class (roadpothole).
Performance metrics (e.g., inference time) printed in the console.

Project Structure
road-pothole-detection/
├── best.pt                   # Pre-trained YOLOv8 model
├── p.mp4                     # Input video file
├── road_pothole_detection.py # Main script for pothole detection
├── Road Pothole Detection.ipynb # Jupyter notebook with the code
├── requirements.txt          # List of Python dependencies
├── README.md                 # Project documentation

Model Details

Model: YOLOv8 (segmentation variant)
Input Size: Frames resized to 1020x700 pixels
Classes: Single class (roadpothole)
Performance: Inference time ~250-350ms per frame (varies by hardware)
Output: Segmentation masks and bounding boxes for detected potholes

To train your own model, refer to the Ultralytics YOLOv8 documentation for dataset preparation and training instructions.
Contributing
Contributions are welcome! To contribute:

Fork the repository.
Create a new branch (git checkout -b feature-branch).
Make your changes and commit (git commit -m "Add feature").
Push to the branch (git push origin feature-branch).
Open a Pull Request.

Please ensure your code follows the project's coding style and includes relevant tests.
License
This project is licensed under the MIT License. See the LICENSE file for details.
Acknowledgements

Ultralytics YOLOv8 for the YOLO implementation.
OpenCV for video processing and visualization.
cvzone for enhanced visualization utilities.

For any questions or issues, please open an issue on the GitHub repository.
