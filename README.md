# Vehicle Identification on Indian Roads 

This project focuses on enhancing road safety and traffic management on Indian roads. Leveraging a custom dataset curated for the unique complexities of the Indian traffic landscape, we employed YOLOv7, to develop a real-time image recognition model. It has applications in various fields like traffic management, public safety and urban planning.

Official yolov7 repository : https://github.com/WongKinYiu/yolov7


## Results

![App Screenshot](https://github.com/NikhilBhalla16/Vehicle-Identification-on-Indian-Roads/assets/109459445/f0e64777-1e51-48e0-a5c6-565b2b380d76)
![App Screenshot](https://github.com/NikhilBhalla16/Vehicle-Identification-on-Indian-Roads/assets/109459445/3979c47c-d985-4cb1-a642-6e7198af8db3)

## Custom Dataset 

https://drive.google.com/drive/folders/1Dl5QaSYkkirK0mizLs1xss_kghVgOCFm?usp=sharing
training data to be stored in data/train
validation data to be stored in data/val

## Weights file 

https://drive.google.com/file/d/1bKEa2Z_5ByYyQO_2UqBFLqeLwe2cbTBw/view?usp=sharing

## Installation

Install pytorch

```bash
  pip install -r requirements.txt
  pip install -r requirements_gpu.txt
```

## Training

Training the model 

```bash
  python train.py --workers 1 --device 0 --batch-size 4 --epochs 100 --data data/custom_data.yaml --hyp data/hyp.scratch.custom.yaml --cfg cfg/training/yolov7-custom.yaml --name yolov7-custom --weights yolov7.pt
```

## Using the model 


```bash
  python detect.py --weights runs/train/yolov7-custom/weights/best.pt --conf 0.5 --source imagename.jpg --view-img --no-trace
```
