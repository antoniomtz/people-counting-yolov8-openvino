# People Counting System using YoloV8 and OpenVINO

In this project, I utlized YOLOV8 Object Counting class to develop a real-time people counting system using the YOLOv8 object detection model, optimized for Intel's OpenVINO toolkit to enhance inferencing speed. This system effectively monitors the number of individuals entering and exiting a room, leveraging the optimized YOLOv8 model for accurate people detection under varied conditions.

By utilizing the OpenVINO runtime on Intel hardware, the system achieves significant improvements in processing speed, making it ideal for applications requiring real-time data, such as occupancy management and traffic flow control in public spaces and commercial settings.

References:

- YoloV8 Object counting documentation: <a href="https://docs.ultralytics.com/guides/object-counting/" target="_blank">https://docs.ultralytics.com/guides/object-counting/</a>
- OpenVINO Jupyter Notebooks: <a href="https://github.com/openvinotoolkit/openvino_notebooks/" target="_blank">https://github.com/openvinotoolkit/openvino_notebooks/</a>

<div align="center"><img src="people-count.gif" width=900/></div>

## Open in Google Colab

<a href="https://colab.research.google.com/github/antoniomtz/people-counting-yolov8-openvino/blob/main/people-counting.ipynb" target="_blank"><img src="https://camo.githubusercontent.com/f5e0d0538a9c2972b5d413e0ace04cecd8efd828d133133933dfffec282a4e1b/68747470733a2f2f636f6c61622e72657365617263682e676f6f676c652e636f6d2f6173736574732f636f6c61622d62616467652e737667" alt="Colab" data-canonical-src="https://colab.research.google.com/assets/colab-badge.svg" style="max-width: 100%;"></a>

## Performance

In this clip, you can see the difference (Inference time and FPS) between running yoloV8 natively with pyTorch vs optimized with OpenVINO using my personal laptop with 11th Gen Intel® Core™ i9-11900H @ 2.50GHz × 16

<div align="center"><img src="optimized.gif" width=900/></div>

## Docker Installation

### Build docker image

```
$ docker build . -t people-count
```

### Run docker container

```
docker run -it --device=/dev/dri --device=/dev/video0 --privileged --group-add=$(stat -c "%g" /dev/dri/render* | head -n 1) -p 8888:8888 people-count
```

It will prompt the jupyter lab URL on the console, copy and paste it on your browser:

```
Or copy and paste one of these URLs:
        http://localhost:8888/lab?token=<token>
```

## Run it locally

Run the following commands to create a virtual env on your local system

```
python3 -m venv jup1
source jup1/bin/activate
pip install jupyterlab
```

Run jupyter notebook:

```
jupyter lab people-counting.ipynb
```