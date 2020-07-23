# Session 14 - Dataset For Monocular Depth Estimation and Segmentation
#  Objective
Create a custom dataset for monocular depth estimation and segmentation simultaneously.

Since we do not have access to a depth camera, we use a pre-trained depth model to generate the depth maps which will be used as the ground truth for our model.

## Dataset Samples
### Background Images
- "scene" images. Like the front of shops, etc.
- 100 images of streets were downloaded from the internet.
- Each image was resized to 128 x 128
- Number of images: 100
Background:![alt text](https://github.com/ashkash2476/EVA_Session14_15/blob/master/Final_images/BG_list.png)

### Foreground Images
- Images of objects with transparent background
- 100 images of people were downloaded from the internet.
- Using GIMP, the foreground was cutout. and the background was made transparent by adding an alpha layer.
- Each image was rescaled to keep height 100 and resizing width while maintaining aspect ratio.
- Number of images: 100
Foreground:![alt text](https://github.com/ashkash2476/EVA_Session14_15/blob/master/Final_images/fg_img.png)

Masks:![alt text](https://github.com/ashkash2476/EVA_Session14_15/blob/master/Final_images/masks.png)

Foreground Background Overlayed:![alt text](https://github.com/ashkash2476/EVA_Session14_15/blob/master/Final_images/FG_BG_overlayed.png
)

Foreground Background Masks:![alt text](https://github.com/ashkash2476/EVA_Session14_15/blob/master/Final_images/fg_bg_masks.png
)






