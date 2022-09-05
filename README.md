# butterfly
A detector using YOLOv7 model
## Dependencies
You can install all the dependencies by running the commands below

**Download YOLOv7 repository and install requirements**

For Colab
```bash
!git clone https://github.com/WongKinYiu/yolov7
%cd yolov7
!pip install -r requirements.txt`
```

For Windows
```bash
git clone https://github.com/WongKinYiu/yolov7 yolov7
pip install -r requirements.txt`
```

You would see similar file directories this (I was using Colab to do this task)

while 'final_project-2' is the dataset file downloaded from roboflow and yolov7.pt is the initial weights path

<img width="212" alt="image" src="https://user-images.githubusercontent.com/112830629/188335958-e31faeb2-165a-41e7-a9ce-bbef05f18f00.png">

Windows

<img width="249" alt="image" src="https://user-images.githubusercontent.com/112830629/188336750-5d13b6ad-33ca-41e6-9702-a23a9f701e34.png">

## Steps to get the detector

**Add `custom_detect.py` into /yolov7 file (i.e. we would use 'custom_detect.py' instead of 'detect.py')**

**Add `best.pt` into the /yolov7 file (This is the trained model from yolov7)**

**Run the following:**
For Colab
```bash
!python custom_detect.py --weights best.pt --conf 0.2 --source {path/to/your/butterfly/video.mp4}
```

For Window
```bash
python custom_detect.py --weights best.pt --conf 0.2 --source https://www.youtube.com/watch?v=6hyLdfYIcxI&ab_channel=WildlifeKingdom
```
or 

```bash
python custom_detect.py --weights best.pt --conf 0.2 --source {path/to/your/butterfly/video.mp4}
```

**There will return a video saved in the path `yolov7/runs/detect/exp/video.mp4`**

