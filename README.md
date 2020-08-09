# Session 14-15 - Data creation For Monocular Depth Estimation and Segmentation
#  Goal
Create a customized image dataset for monocular depth estimation and segmentation.


## Dataset Creation Steps
### Step 1: Background Images
- "scene" images. Like malls, hotel
- 100 images of malls and hotel lobbys were downloaded from the internet.
- Each image was resized to 128 x 128
- Number of images: 100
Background:![alt text](https://github.com/ashkash2476/EVA_Session14_15/blob/master/Final_images/BG_list.png)

### Step 2: Foreground Images
- Images of objects with transparent background
- 100 images of people were downloaded from the internet.
- Using GIMP, the foreground was extracted. The background was deleted by adding an alpha layer.
- Each image was rescaled to keep height 50 and resizing width while maintaining aspect ratio.
- Number of images: 100
Foreground:![alt text](https://github.com/ashkash2476/EVA_Session14_15/blob/master/Final_images/fg_img.png)

### Step 3: Foreground Masks
- For every foreground its corresponding mask was created
- Using GIMP, the foreground was filled with white and the background was filled with black.
- Image was stored as a grayscale image.
- Each image was rescaled to keep height 50 and resizing width while maintaining aspect ratio.
- Number of images: 100

Masks:![alt text](https://github.com/ashkash2476/EVA_Session14_15/blob/master/Final_images/masks.png)

### Step 4: Foreground Background Overlayed
- For each background
- Overlay each foreground randomly 20 times on the background
- Flip the foreground and again overlay it randomly 20 times on the background
- Number of images: 100*100*2*20 = 400,000
Foreground Background Overlayed:![alt text](https://github.com/ashkash2476/EVA_Session14_15/blob/master/Final_images/FG_BG_overlayed.png
)


### Step 5: Foreground Background Masks
- For every foreground overlayed on background, its corresponding mask was created.
- The mask was created by pasting the foreground mask on a black image at the same position the foreground was overlayed.
- Image was stored as a grayscale image.
Number of images: 400,000
Foreground Background Masks:![alt text](https://github.com/ashkash2476/EVA_Session14_15/blob/master/Final_images/fg_bg_masks.png
)

### Step 6: Foreground Background Depth Maps
- For every foreground overlayed on background, its corresponding depth mask was created.
- A pre-trained monocular depth estimation model DenseDepth was used to generate the depth maps.
- Image was stored as a grayscale image.
Number of images: 400,000
Foreground Background Masks:![alt text](https://github.com/ashkash2476/EVA_Session14_15/blob/master/Final_images/fg_bg_masks.png
)




#### Dataset Link https://drive.google.com/drive/folders/1cC5Rd1Nr34BjsefEjsNgBXDPXadaUB2D?usp=sharing
