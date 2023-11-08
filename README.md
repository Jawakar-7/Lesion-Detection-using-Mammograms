# Lesion-Detection-using-Mammograms
 The model will take as input a mammogram image and output a prediction of whether or not there is a cancerous lesion in the image. The goal is to create a system that can automatically classify images into predefined categories.

 A mammogram is an x-ray picture of the breast. Mammograms can be used to check for breast cancer in women who have no signs or symptoms of the disease. This type of mammogram is called a screening mammogram. Screening mammograms usually involve two or more x-ray pictures, or images, of each breast

 Here I'm  trying to classify the mammograms  as Malignant or benign (1 or 0) using Deep learning techniques.

 # Dataset Description
 This dataset consists of images from the DDSM [1] and CBIS-DDSM [3] datasets. The images have been pre-processed and converted to 299x299 images by extracting the ROIs. The data is stored as tfrecords files for TensorFlow.

The dataset contains 55,890 training examples, of which 14% are positive and the remaining 86% negative, divided into 5 tfrecords files

 # Preprocessing
 The dataset consists of negative images from the DDSM dataset and positive images from the CBIS-DDSM dataset. The data was pre-processed to convert it into 299x299 images.

The negative (DDSM) images were tiled into 598x598 tiles, which were then resized to 299x299.

The positive (CBIS-DDSM) images had their ROIs extracted using the masks with a small amount of padding to provide context. Each ROI was then randomly cropped three times into 598x598 images, with random flips and rotations, and then the images were resized down to 299x299.

The images are labeled with two labels:

label_normal - 0 for negative and 1 for positive


# Modelling 
Here I'm Using the transfer learning technique of VGG16 pretrained on 'imagenet' and adding two extra layers with a dense layer for training the data.
Due to limited time i have trained for only 10 epochs where the model achieved accuracy of 92%

<img width="597" alt="image" src="https://github.com/Jawakar-7/Lesion-Detection-using-Mammograms/assets/94454751/daa0f2aa-b170-4dc6-8821-5e25fc8040b3">

# Metrics 
I have used Classification metrics like Confusion matrix , precision , recall and F1 value
Confusion Matrix:
<img width="416" alt="image" src="https://github.com/Jawakar-7/Lesion-Detection-using-Mammograms/assets/94454751/178b6a99-6676-4245-aa88-3423f64f8732">

Precision: 0.92
Recall: 0.93
F1 Score: 0.92
