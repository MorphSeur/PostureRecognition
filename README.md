# Posture Recognition
Using Tiny-YOLO oneclass to detect each person in the frame and use 
[AlphaPose](https://github.com/MVIG-SJTU/AlphaPose) to get skeleton-pose and then use [ST-GCN](https://github.com/yysijie/st-gcn) model to predict action from every 30 frames of each person tracks.  

Labels: Standing, Walking, Sitting, Lying Down, Stand up, Sit down, Fall Down.  

Check [README.md](https://github.com/MorphSeur/PostureRecognition/tree/master/archive/README.md) located in archive for more details.

## Pre-trained Models
Download the folder with the pre-trained models from this [link](https://mega.nz/folder/Zr4ASSDA#jkJPvnk-YyueRRBNLNCMEQ). And put all the folders in the ./Models/ folder.

## Requirements
Please refer to [requirement.txt](https://github.com/MorphSeur/PostureRecognition/blob/master/requirement.txt).

## Notebook
### mainFrameProcessing.ipynb
- First cell splits the input video located in ./input/ to frames stored ./input/frame/.  
- Second cell read frame by frame located in ./input/frame/, predict labels, put predicted labels in the dedicated frame as text.  
- Third cell read the recognized frames located in ./input/frame/ and build video stored in ./output.