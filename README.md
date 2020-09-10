# yolo-v5--pytorch

In this repository i have implemented yolo v5 using pytorch.

1) download the zip file from this repository.

2) pip install -qr requirements.txt 

3) you need to edit the anil.yaml file.according to your data location and number of classes.

# Create Labels

After using a tool like Labelbox, CVAT or makesense.ai to label your images, export your labels to YOLO format, with one *.txt file per image (if no objects in image, no *.txt file is required). The *.txt file specifications are:


1) One row per object
2) Each row is class x_center y_center width height format.
3) Box coordinates must be in normalized xywh format (from 0 - 1). If your boxes are in pixels, divide x_center and width by image width, and y_center and   height by image height.
4) Class numbers are zero-indexed (start from 0).


Each image's file should be /images/*.jpg with its pathname. An example would be:

        dataset/images/train2017/000000109622.jpg  # image
        
location of the txt file and jpeg file should be in the same folder         
        


  
  
