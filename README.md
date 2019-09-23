# handwriting-detect
The aim of the project is to use machine learning to build a handwriting detector which will detect sample handwriting and finds its corresponding author 
i.e. to classify the given handwritten character by its writer. 

NIST Special Database 19 Hand-printed Forms and Characters 2nd Edition which consists of NIST's entire collection of training data for handwritten document and character recognition is used for this project.
Complete Dataset can be found here- https://www.nist.gov/srd/nist-special-database-19
This code works for five writers i.e approximately 829 images are considered (dataset1)

Various attributes considered are :
1. Histogram of Oriented Gradients (HOG) 
    Python library used -   Using OpenCV we can compute the hog descriptor. 
                            Using skimage.learn we can import hog which provides the necessary method.
2. Blob Detector 
    Python Library-
      Using skimage, we can use skimage.feature.blob\_log(),for detecting blobs. 

3. Scale-invariant feature transform (SIFT)
    Python Library-
      Using OpenCV function, sift.detect() we can obtain the keypoints in the images. 
      Another OpenCV function, cv2.drawKeyPoints() helps to obtain small circles at the keypoint's location.
 
 And various others (in total 22 attributes were obtained by applying PCA) which were combined to form CSV file (namely, s)
 
 On those attributes, various Machine Learning Algorithms were applied and there accuracy was computed and is visualised.
 The impact of a single attribute like Blob and Hog was computed to be compared with all accuracy of all  attributes.
 
 The project was implemented on Jupiter (Anaconda) using Python and various libraries used were :
 numpy, pandas, skimage.io, opencv,
 sklearn.naivebayes import GaussianNB,
 sklearn.neighbors import KNeighborClassifier and various others(can be found in accuracy file).
