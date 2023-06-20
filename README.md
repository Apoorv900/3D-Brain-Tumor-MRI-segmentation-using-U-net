# 3D-Brain-Tumor-MRI-segmentation-using-U-net
Problem definiton
Segmentation of gliomas in pre-operative MRI scans.

Each pixel on image must be labeled:

Pixel is part of a tumor area (1 or 2 or 3) -> can be one of multiple classes / sub-regions
Anything else -> pixel is not on a tumor region (0)
The sub-regions of tumor considered for evaluation are: 1) the "enhancing tumor" (ET), 2) the "tumor core" (TC), and 3) the "whole tumor" (WT) The provided segmentation labels have values of 1 for NCR & NET, 2 for ED, 4 for ET, and 0 for everything else


Step 1: Dataset Preparation
To begin, I collected a dataset of brain MRI images . The images consist of both tumor and non-tumor cases. I ensured that the dataset was diverse and representative of different types of brain tumors.

Step 2: Data Preprocessing
Next, I preprocessed the MRI images . This involved resizing the images to a consistent resolution, normalizing the pixel values, and converting them to a suitable format for model training. I also performed data augmentation techniques such as random rotations, flips, and brightness adjustments to increase the dataset size and enhance the model's ability to generalize.

Step 3: U-Net Architecture
For this task, I chose the U-Net architecture, which is a popular choice for image segmentation tasks. The U-Net architecture consists of an encoder path and a decoder path. The encoder path is responsible for capturing high-level features from the input image, while the decoder path upsamples the features to generate the final segmentation map.

Step 4: Model Training
I split the dataset into training and validation sets. Then, I trained the U-Net model using the training set. During training, I used the Dice coefficient as the loss function, which measures the similarity between the predicted segmentation and the ground truth. I also utilized an optimization algorithm such as Adam or SGD to iteratively update the model's parameters and minimize the loss.

Step 5: Model Evaluation
Once the model finished training, I evaluated its performance on the validation set. I computed evaluation metrics such as the Dice coefficient, accuracy, precision, recall, and F1 score to assess the model's segmentation accuracy and generalization capabilities. I also visually inspected the model's predictions on sample validation images to gain a qualitative understanding of its performance.

Step 6: Inference and Post-processing
After the model was trained and evaluated, I utilized it for segmenting brain tumors in new MRI images. I fed the test images through the trained model, which produced a segmentation map for each image. To refine the segmentation output, I applied post-processing techniques like thresholding, morphological operations, and connected component analysis to improve the final segmentation accuracy and remove any potential artifacts.

Step 7: Results Analysis
Lastly, I analyzed and interpreted the segmentation results. I compared the model's predictions with the ground truth masks and computed various evaluation metrics to measure its performance. I visualized the segmented tumor regions overlaid on the original MRI images to gain insights into the model's accuracy and identify any potential areas of improvement.

By following these steps, I successfully developed a brain tumor MRI segmentation model using the U-Net architecture. I believe this explanation will help you document the process on your GitHub repository. Feel free to customize and expand upon the details based on your specific implementation and findings. Good luck!





