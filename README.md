# YoloV3
________
YoloV3 Simplified for training on Colab with custom dataset. 

_A Collage of Training images_
![image](https://github.com/abhinavdayal/YoloV3/blob/master/train_batch0.png)

_A Collage of Test images_
![image](https://github.com/abhinavdayal/YoloV3/blob/master/test_batch0.png)


Full credit goes to [this](https://github.com/ultralytics/yolov3), and if you are looking for much more detailed explainiation and features, please refer to the original [source](https://github.com/ultralytics/yolov3). 

We created custom dataset for detecting Guns. As conmpared to animated character, we felt it is mor challenging given to different types and shapes of guns:
1. We annotated using: https://github.com/miki998/YoloV3_Annotation_Tool
2. The images are in
```
data
  --gundata
    --images/
      --img0001.jpg
      --img0002.jpg
      --...
    --labels/
      --img0001.txt
      --img0002.txt
      --...
    custom.data #data file
    names.txt #your class names
    customtrain.txt #list of name of the images to be trained on.
    customtest.txt #list of name of the images to be tested on.
```

As you can see in the collage image above, a lot is going on, and if you are creating a set of say 500 images, you'd get a bonanza of images via default augmentations being performed. 


**Results**
After training for 300 Epochs, results look awesome!

![image](https://github.com/theschoolofai/YoloV3/blob/master/output/image005.jpeg)
