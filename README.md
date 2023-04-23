# EE104_Lab7_Yolo8v_BalloonFlight

Reference: Laboratory 8

About this lab: there are two parts in this lab, the first part is about using the YOLO5 to train the AI to recognize objects. The second one is the Balloon Flight python game.

1)	We will use YAMOv5 to train the AI this time. 
You need to install YOLO5 file from https://github.com/ultralytics/yolov5
Python 3.10.8
Latest CUDA from https://developer.nvidia.com/cuda-downloads
PyTorch from https://pytorch.org/get-started/locally/
PyCOCOTools from https://github.com/philferriere/cocoapi.git 
Labelling Repo from https://github.com/ivangrov/ModifiedOpenLabelling
And pip install -r requirements.txt
After all the installation, download the images you want to train to C:\ModifiedOpenLabelling-main\images
Then run the ‘python run.py’ in cmd to label images with different names. 
Then Split the data into training and validation in cmd with commend line ‘python train_test_split.py’
Drag files in train folder to train folder in C:\yolov5\datasets\coco128, and same with the files in lable folder.
In the end, you could train your model in yolo cmd with the command line ‘python train.py --img 415 --batch 16 --epochs 100--data datasets/coco128_ee104.yaml --weight yolov5s.pt –cache’
Wait for the computer to finish the 100 epochs. And you will get a command line shows that the trained result is saved to ‘run\train\exp(number)
Then run ‘python detect.py --source 0 --weights C:\yolov5\runs\train\exp2\weights\best.pt’ but remember to change the number of the exp. And the result will show on your computer screen!

2)	Game Development – Balloon flight
Based on the slide, I just add Lives, Speed it up, More high scores, and Add in Multiples of Each obstacle to the python code
Lives: I set 150 HP as lives, every time the balloon is hit, the HP will decrease depending on the time it hit the obstacles. 
Speed it up: add the speed from 2 to 4
More high scores: list 5 highest scores instead of 3
Multiples of Each obstacle: add one bird, one more tree, and one more house.


