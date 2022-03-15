# Brain Tumor Classification using Cost-sensitive Neural Networks and Transfer Learning

readme under construction


Currently, diagnosis and categorization of brain tumors are still reliant on histopathological eval-
uation of biopsy samples. Current methods are intrusive, time demanding,
and subject to human error. These drawbacks highlight the critical nature of developing an au-
tomated system to classify brain tumors using deep learning. This research aims to develop a
binary classification system for the early diagnosis of the most common malignant (cancerous)
tumor using a cost-sensitive convolutional neural network and transfer learning with EfficientNet
architecture.


<img src="https://user-images.githubusercontent.com/20649715/158368324-00df0d35-6ef2-4562-a6f5-121de4bdcf74.png" width=40% height=40%>



# Dataset

The chosen dataset contains 3064 T1-weighted contrast-enhanced MRI images from 233 patients
with three kinds of brain tumor: glioma, meningioma, and pituitary tumors. All data used is
publicly available at https://figshare.com/articles/dataset/brain_tumor_dataset/1512427/5. The slices are from 3 different planes: sagittal, axial, and coronal. Each patient has a different amount of pictures.

# Descriptive
The figure shows a sample of images from the dataset with a partially transparent tumor mask
indicating the location and shape of the tumors. We can see that the slices are from different
perspectives and different depths. The direction of the eyes is slightly changing per image, but
there seems to be a pattern. For example, images from the axial plane usually face the left side of
the image. The model can become sensitive to these image rotation settings and conclude a causal
relationship. Image augmentation needs to be done to make the model indifferent to the qualities
that are irrelevant for the classification.


<img src="https://user-images.githubusercontent.com/20649715/158368652-c4c05aa5-f575-4bad-8c67-ed19a626b9c8.png" width=80% height=40%>









