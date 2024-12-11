We will detect guns with help of a pre-trained Yolov11 model

# Setup
Clone the repository
```
git clone https://github.com/Faryalaurooj/Yolo11-Gun-Detection-Model.git
```

Create a new environment
```
conda create -n yolo11_env
```

Activate the environment
```
conda activate yolo11_env
```

Change your directory
```
cd Yolo11-Gun-Detection-Model
```

Install all requirements
```
pip install -r requirements.txt
```

# Inference 
To run inference on desired video streams write this in terminal

```
yolo detect predict model=model.pt source=./test_videos/gun3.mp4
```

And to test on images

```
yolo detect predict model=model.pt source=./test_images/images
```
# Train
In order to train the pre-trained model on another weapons datset we can run this command

```
yolo detect train data=gun2.yaml model=yolo11x.yaml epochs=100  batch=8  imgsz=416
```

we have to be sure that datset is placed in this format and we have a yaml file that defines the paths


guns_dataset/
├── images/
│   ├── train/
│   │   ├── img1.jpg
│   │   ├── img2.jpg
│   │   └── ...
│   ├── val/
│   │   ├── img1.jpg
│   │   ├── img2.jpg
│   │   └── ...
├── labels/
│   ├── train/
│   │   ├── img1.txt
│   │   ├── img2.txt
│   │   └── ...
│   ├── val/
│   │   ├── img1.txt
│   │   ├── img2.txt
│   │   └── ...
└── guns_dataset.yaml

