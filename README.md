# Machine-Learning-Sec.4
## Background
Recognize a person’s face by comparing facial images to that of a known person. The algorithm projects the image onto a “face space” composed of a complete basis of eigenfaces.”，人脸识别项目

## Dataset
* There are 10 different images of 40 distinct subjects.
* For some of the subjects, the images were taken at different times, varying lighting slightly, facial expressions (open/closed eyes, smiling/non-smiling) and facial details (glasses/no-glasses).
* All the images are taken against a dark homogeneous background and the subjects are in up-right, frontal position (with tolerance for some side movement).
* The files are in PGM format. Python does offer some image libraries, including OpenCV with which the files can be loaded.
* The size of each image is 92x112, 8-bit grey levels.
* The images are organized in 40 directories (one for each subject) named as: sX, where X indicates the subject number (between 1 and 40). In each directory there are 10 different images of the selected subject named as: Y.pgm, where Y indicates which image for the specific subject (between 1 and 10).

## Tasks
1. （求特征脸）Generate five random numbers (e.g., 2, 5, 7, 9, 10) and use them to select five images (i.e., 2nd, 5th, 7th, 9th, and 10th images) from each subject. Using those images to calculate the eigenfaces (if out of memory, please use 20 subjects in the whole homework).
  * a. Plot the eigenfaces.
  * b. Plot the eigenvalues out and select the cut down value by the figure; say keep only

those principal components preserving 90% or more variance of the dataset.

2. （KNN分类算法，识别人脸并报告准确度）Using kNN (k=1) perform classification. Here, the dataset should be randomly split into training and test (80%-20%). Please report combined classification accuracy, and per subject classification accuracy on the test dataset.

3. （5层交叉验证法）Using 5-fold cross validation to do task 2.

4. （改变图片大小重复上述步骤）Resize the images from 92x112 to 46x56 and repeat tasks 1-3. Compare the new results to the results using un-resized images.

5. （SVM支持向量机的性能）Can Support Vector Machines outperform any of the kNN results? Please implement the SVM algorithm by yourself, and report its performance. 

6. Apply your SVM on the original image dataset without using PCA, and report its performance.
