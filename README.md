# YOLOv1_from_scratch
My implementation of YOLOv1 from scratch in pytorch

Stuff i've done so far
* Read in class data from folders
* Darkne19 backbone architecture

## Logic that needs implementing:

# Predictions
* Divide the input image into an S × S grid.
* Each grid cell predicts 2 bounding boxes (wide, tall) and objectness confidence scores for those boxes
* i.e [x1,y1,w1,h1,C1,x2,y2,w2,h2,C2]
* Each grid cell predicts 4 class probability ( 4 "animal" classes ) [p1,p2,p3,p4]
* So we have [x1,y1,w1,h1,C1,p11,p12,p13,p14,x2,y2,w2,h2,C2,p21,p22,p23,p24] as our prediction
* Zero out predictions below adjustable threshold - IOU thresh, Conf thresh

# Loss function
* Implement loss function
* Implement IOU loss
