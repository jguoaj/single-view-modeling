## Single view metrology

### General Idea
This project is to create 3D texture-mapped models from a single image using the single view modeling method discussed in "Single View Metrology," by Criminisi, Reid, and Zisserman, ICCV 99.

### Reference Paper
[Single View Metrology](https://github.com/jguoaj/single-view-modeling/blob/master/Criminisi99.pdf)


### Methodology
1. Calculate the vanishing points by **Bob Collins' algorithm**
2. Calculate the Projective matrix, where the scales are computed with reference points and vanishing points
3. Use Homograph Matrix to get the texture map (for simplicity, we directly "hardcode" points this time)
4. Mark interesting points and get 3D coordinates
<img src = "./img/heightCal.png" width = "40%" height = "40%">

5. Generate VMRL model

### Results

#### Example 1, provided sony box
Source Image

<img src = "./img/SVM1.jpg" width = "40%" height = "80%">

Texture Maps

<img src = "./SingleViewModel/result/sony/xy_patch.jpg" width = "20%" height = "60%"><img src = "./SingleViewModel/result/sony/yz_patch.jpg" width = "33%" height = "100%"><img src = "./SingleViewModel/result/sony/xz_patch.jpg" width = "33%" height = "87%">

Results

<img src = "./img/1.png" width = "40%" height = "80%">

#### Example 2, my own box
Source Image

<img src = "./img/SVM2.jpg" width = "40%" height = "80%">

Texture Maps

<img src = "./SingleViewModel/result/jixin'sbox/xy_patch.jpg" width = "20%" height = "80%"><img src = "./SingleViewModel/result/jixin'sbox/yz_patch.jpg" width = "20%" height = "8%"><img src = "./SingleViewModel/result/jixin'sbox/xz_patch.jpg" width = "20%" height = "80%">

Results

<img src = "./img/3.png" width = "40%" height = "80%">

#### Example 3, Rubik's cube
Source Image

<img src = "./img/rubik.jpg" width = "40%" height = "80%">

Texture Maps

<img src = "./SingleViewModel/result/rubik/corner1.bmp" width = "20%" height = "70%"><img src = "./SingleViewModel/result/rubik/corner2.bmp" width = "20%" height = "70%"><img src = "./SingleViewModel/result/rubik/corner3.bmp" width = "20%" height = "70%">
<img src = "./SingleViewModel/result/rubik/face_corner.bmp" width = "20%" height = "70%"><img src = "./SingleViewModel/result/rubik/left_top.png" width = "14%" height = "3%"><img src = "./SingleViewModel/result/rubik/face_mid.bmp" width = "20%" height = "130%">

Results

<img src = "./img/2.png" width = "40%" height = "80%">

#### Example 4, artistic painting
Source Image

<img src = "./SingleViewModel/result/painting/painting.jpg" width = "40%" height = "80%">

Texture Maps

<img src = "./SingleViewModel/result/painting/deskleftside.jpg" width = "6%" height = "10%"><img src = "./SingleViewModel/result/painting/rightleg.jpg" width = "6%" height = "2%"><img src = "./SingleViewModel/result/painting/leftlegfront.jpg" width = "6%" height = "2%">
<img src = "./SingleViewModel/result/painting/deskrightslant.jpg" width = "6%" height = "12%"><img src = "./SingleViewModel/result/painting/deskrightside.jpg" width = "6%" height = "10%"><img src = "./SingleViewModel/result/painting/Hxy_image.jpg" width = "20%" height = "100%">


Results

<img src = "./img/4.png" width = "40%" height = "80%">

