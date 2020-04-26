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

![image](https://raw.githubusercontent.com/abhinavdayal/YOLOV3/master/output/img260.jpg)
![image](https://raw.githubusercontent.com/abhinavdayal/YOLOV3/master/output/img409.jpg)

**VIDEO**

[![Alt text](https://img.youtube.com/vi/eXjxy_7W7GQ/0.jpg)](https://www.youtube.com/watch?v=eXjxy_7W7GQ)

**Training Performance**

![training perf](https://raw.githubusercontent.com/abhinavdayal/YOLOV3/master/results.png)

## Observations
We had following observations as we did this project:
1. The network trained for classes and bbox from beginning as opposed to first 100 iterations only classes and then bbox. Probably this is due to us using transfer learning
2. We calculated oour own kmeans [anchor boxes](https://raw.githubusercontent.com/abhinavdayal/YOLOV3/master/anchors/anchors9.txt) However when we u sed those the model did not train. Again because we are using transfer learning we had to use the same bbox as the base model was trained for.
3. We tried other image augmentations, but RICAP itself is good and adding more did not help, instead it deteriorated the performance.
4. Given more data it will probably perform even better
