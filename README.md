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

### Foreground Masks
- For every foreground its corresponding mask was created
- Using GIMP, the foreground was filled with white and the background was filled with black.
- Image was stored as a grayscale image.
- Each image was rescaled to keep height 105 and resizing width while maintaining aspect ratio.
- Number of images: 100

Masks:![alt text](https://github.com/ashkash2476/EVA_Session14_15/blob/master/Final_images/masks.png)

### Foreground Background Overlayed
- For each background
- Overlay each foreground randomly 20 times on the background
- Flip the foreground and again overlay it randomly 20 times on the background
- Number of images: 100*100*2*20 = 400,000
Foreground Background Overlayed:![alt text](https://github.com/ashkash2476/EVA_Session14_15/blob/master/Final_images/FG_BG_overlayed.png
)


### Foreground Background Masks
- For every foreground overlayed on background, its corresponding mask was created.
- The mask was created by pasting the foreground mask on a black image at the same position the foreground was overlayed.
- Image was stored as a grayscale image.
Number of images: 400,000
Foreground Background Masks:![alt text](https://github.com/ashkash2476/EVA_Session14_15/blob/master/Final_images/fg_bg_masks.png
)






