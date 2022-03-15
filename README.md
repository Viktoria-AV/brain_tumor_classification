# Brain Tumor Classification using Cost-sensitive Neural Networks and Transfer Learning



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

The figure shows a sample of images from the dataset with a partially transparent tumor mask
indicating the location and shape of the tumors. We can see that the slices are from different
perspectives and different depths. The direction of the eyes is slightly changing per image, but
there seems to be a pattern. For example, images from the axial plane usually face the left side of
the image. The model can become sensitive to these image rotation settings and conclude a causal
relationship. Image augmentation needs to be done to make the model indifferent to the qualities
that are irrelevant for the classification.

<img src="https://user-images.githubusercontent.com/20649715/158368652-c4c05aa5-f575-4bad-8c67-ed19a626b9c8.png" width=40% height=40%>

The dataset is
first separated patent-wise into 75% for the model training and 25% for testing. The testing data
was not augmented, it was only resized. Data augmentation aids the model’s generalization and
robustness. As a result, augmenting the test set is unnecessary.


<img src="https://user-images.githubusercontent.com/20649715/158387434-f1f3c51f-5d23-4c89-bf43-fdc2c45df7bb.png" width=40% height=40%>



# Research Design

GPU for effective computation
When training the model, the programmer can be delayed by very long runtimes. With the help
of the cloud GPU service in Google Colab(https://colab.research.google.com/), this training time can be decreased to a fraction of
how long it takes on a regular CPU. The running time for the pretrained
EfficientNet base with a top layer being Convolutional Neural Network was one hour and ten
minutes on the CPU compared to three minutes on the Google Colab GPU.



