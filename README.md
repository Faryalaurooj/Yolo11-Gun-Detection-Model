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


