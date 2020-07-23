# Session 14 - Dataset For Monocular Depth Estimation and Segmentation
#  Objective
Create a custom dataset for monocular depth estimation and segmentation simultaneously.

Since we do not have access to a depth camera, we use a pre-trained depth model to generate the depth maps which will be used as the ground truth for our model.

## Dataset Samples
### Background Images
- "scene" images. Like the front of shops, etc.
- 100 images of streets were downloaded from the internet.
- Each image was resized to 224 x 224
- Number of images: 100
Background:![alt text](https://github.com/ashkash2476/EVA_Session14_15/blob/master/Final_images/BG_list.png)

Foreground:![alt text](https://github.com/ashkash2476/EVA_Session14_15/blob/master/Final_images/fg_img.png)

Masks:![alt text](https://github.com/ashkash2476/EVA_Session14_15/blob/master/Final_images/masks.png)

Foreground Background Overlayed:![alt text](https://github.com/ashkash2476/EVA_Session14_15/blob/master/Final_images/FG_BG_overlayed.png
)

Foreground Background Masks:![alt text](https://github.com/ashkash2476/EVA_Session14_15/blob/master/Final_images/fg_bg_masks.png
)






