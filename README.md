# YOLOv10 Deployment Sample

This repository contains a sample deployment of YOLOv10, a real-time object detection model. Follow the instructions below to set up and run the model on your system.

## Table of Contents
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Usage](#usage)
- [Configuration](#configuration)
- [Results](#results)
- [License](#license)

## Prerequisites
Make sure you have the following installed:
- Python 3.8+
- PyTorch
- CUDA (if using a GPU)
- OpenCV
  
## Installation

    ```bash
    git clone https://github.com/THU-MIG/yolov10
    ```

## Usage

1. Download the pre-trained weights and place them in the `weights/` directory. You can find the weights [here](https://example.com/yolov10-weights).

2. Run the inference script:
    ```bash
    python detect.py --weights weights/yolov10.pth --source data/test.jpg
    ```

3. To run inference on a video file:
    ```bash
    python detect.py --weights weights/yolov10.pth --source data/test.mp4
    ```

4. For real-time detection using your webcam:
    ```bash
    python detect.py --weights weights/yolov10.pth --source 0
    ```

## Configuration

You can customize the model's behavior using the command-line options:

- `--weights`: Path to the weights file (default: `weights/yolov10.pth`)
- `--source`: Input source (image, video file, or webcam)
- `--conf-thres`: Confidence threshold for detection (default: 0.25)
- `--iou-thres`: IoU threshold for NMS (default: 0.45)

Refer to the `detect.py` script for more details.

## Results

Results will be saved in the `output/` directory. You will find:
- Processed images with bounding boxes
- Videos with object detections
- Logs and performance metrics

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
