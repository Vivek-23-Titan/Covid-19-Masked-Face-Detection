# Covid-19-Masked-Face-Detection-using-YoloFace
Covid-19 Masked Face Person Re-Identification using YoloFace and VggFace

This is a person Re-Identification project which was carried out by first Face Detection by MTCNN model and then Face Recognition by the VGGFace model. However, with the current pandemic senario, this project moved its focus to Masked Face (Occlusion) Detection. But in ding so, the MTCNN model did not fetch expected results hence, YoloFace model was introduced.(paper - https://link.springer.com/article/10.1007/s00371-020-01831-7)

## Process
1) The video is spit into frames then Faces are extracted using YoloFace.
2) An image of the person to be identified is provided and compared with the faces in the database via VGGFace. If it belongs to the known individual's database, the name of the person is displayed.
3) VGGFace is used to compare the person to be re-idetified with the video frames.

## Code
The code is available in Juypter notebook.

## Results
Face Detection comparison between MTCNN and YoloFace on Masked Faces.
![](images/Val_Acc_Comparision.PNG)

The comparison between the original dataset and the combined dataset is shown with the help of confusion matrix.

### Original Dataset Confusion Matrix (~90%)

![](images/Original_Confusion_Matrix.PNG)

### Combined Dataset Confusion Matrix (94.1%)

![](images/Combined_Confusion_Matrix.PNG)

The maximum accuracy attained by the combined training dataset was 94.1% which is an improvement of 4% over the original dataset.

### Requirements

TensorFlow version 2.2.0\
Keras version 2.3.1
