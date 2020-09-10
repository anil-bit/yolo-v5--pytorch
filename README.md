# yolo-v5--pytorch

In this repository i have implemented yolo v5 using pytorch.

1) download the zip file from this repository.

2) pip install -qr requirements.txt 

3) you need to edit the elephent.yaml file.according to your data location and number of classes.

# Create Labels

After using a tool like Labelbox, CVAT or makesense.ai to label your images, export your labels to YOLO format, with one *.txt file per image (if no objects in image, no *.txt file is required). The *.txt file specifications are:


1) One row per object
2) Each row is class x_center y_center width height format.
3) Box coordinates must be in normalized xywh format (from 0 - 1). If your boxes are in pixels, divide x_center and width by image width, and y_center and   height by image height.
4) Class numbers are zero-indexed (start from 0).


Each image's file should be /images/*.jpg with its pathname. An example would be:
     
     /home/anil/Videos/yolov5/data/image/750P02F-ZOSP1-N_191_A_1_NG10_10.jpeg
        
        
location of the txt file and jpeg file should be in the same folder.

# Train

Train a YOLOv5s model on your data  by specifying model config file --cfg models/yolo5s.yaml, and dataset config file --data data/elephant.yaml. Start training from pretrained --weights yolov5s.pt, or from randomly initialized --weights ''. Pretrained weights are auto-downloaded from Google Drive.
        
command line for trainining:

     $ python train.py --img 640 --batch 16 --epochs 5 --data ./data/coco128.yaml --cfg ./models/yolov5s.yaml --weights ''
     
# Testing

commnad line for testing:

     $ python detect.py --source ./inference/images/ --weights yolov5s.pt --conf 0.4
      
  
