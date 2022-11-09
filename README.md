# My Solution

To solde the problem of person object detection, i have choice the Yolov7 architecture found here : [YOLOv7: Trainable bag-of-freebies sets new state-of-the-art for real-time object detectors](https://arxiv.org/abs/2207.02696)

## How it work ?

### Annontation
First i have use Roboflow as website in order to annontate the images

Roboflow can found [here](https://roboflow.com/)

### test

I have made a notebook which can be run in [Google Colab](https://colab.research.google.com) in the folder google_colab

### Download models
- Coco Models

```sh
# Download trained weights
wget https://github.com/WongKinYiu/yolov7/releases/download/v0.1/yolov7-tiny.pt
# this model can detect all the coco classe (80)
```
- Person models
```sh
wget https://github.com/WongKinYiu/yolov7/releases/download/v0.1/yolov7-w6-person.pt

```
- Test with coco models
```sh
python detect.py --weights ./yolov7-tiny.pt --conf 0.25 --img-size 1920 --source image_test/1660626000.jpg
```

- Test with person models
```sh
python detect.py --weights ./yolov7-w6-person.pt --conf 0.25 --img-size 1920 --source image_test/1660626000.jpg
```

## Licence

Seyf Eddine




