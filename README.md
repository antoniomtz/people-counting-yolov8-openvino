# people-counting-yolov8-openvino
People Counting System using YoloV8 and OpenVINO

In this project, I utlized YOLOV8 Object Counting class to develop a real-time people counting system using the YOLOv8 object detection model, optimized for Intel's OpenVINO toolkit to enhance inferencing speed. This system effectively monitors the number of individuals entering and exiting a room, leveraging the optimized YOLOv8 model for accurate people detection under varied conditions.

By utilizing the OpenVINO runtime on Intel hardware, the system achieves significant improvements in processing speed, making it ideal for applications requiring real-time data, such as occupancy management and traffic flow control in public spaces and commercial settings.

References:

- <a href="https://docs.ultralytics.com/guides/object-counting/" target="_blank">https://docs.ultralytics.com/guides/object-counting/</a>
- <a href="https://github.com/openvinotoolkit/openvino_notebooks/" target="_blank">https://github.com/openvinotoolkit/openvino_notebooks/</a>

<div align="center"><img src="people-count.gif" width=900/></div>

## Open in Google Colab

<a href="https://colab.research.google.com/github/antoniomtz/people-counting-yolov8-openvino/blob/main/people-counting.ipynb" target="_blank"><img src="https://camo.githubusercontent.com/f5e0d0538a9c2972b5d413e0ace04cecd8efd828d133133933dfffec282a4e1b/68747470733a2f2f636f6c61622e72657365617263682e676f6f676c652e636f6d2f6173736574732f636f6c61622d62616467652e737667" alt="Colab" data-canonical-src="https://colab.research.google.com/assets/colab-badge.svg" style="max-width: 100%;"></a>

## Pre-requisites (Ubuntu)

1. Install Python,Git, GPU drivers

```bash
sudo apt-get update
sudo apt-get upgrade
sudo apt-get install python3-venv build-essential python3-dev git-all libgl1-mesa-dev
```

2. Create Virtual Env

```
python3 -m venv openvino_env
source openvino_env/bin/activate
```

3. CLone the repository

```
git clone https://github.com/antoniomtz/people-counting-yolov8-openvino.git
cd people-counting-yolov8-openvino
```

4. Install the packages

```
python -m pip install --upgrade pip
pip install wheel setuptools
pip install -r requirements.txt
```

5. Launch the Notebook

```
jupyter lab people-counting.ipynb
```