# Keypoint-detection-and-Eye-and-face-detection

Implement the advanced vision methods: neural network units, feature detection with ORB (replacement for SIFT), and Haar cascade face and eye detection.

**Neural Network Units**

  * Implement a single sigmoid neural network unit with weights of [-1.2, -1.1, 3.3, -2.1]
  * Calculate the outputs for two training examples:
      * Example 1: [0.9, 10.0, 3.1, 1]
      * Example 2: [0.9, 2.1, 3.7, 1]
  * Note that you don't have to explicitly include a threshold or bias since the examples include a last element of 1 which means that the last weight effectively operates as a threshold.
  * Assuming that a sigmoid unit response >0.5 denotes a positive class and <0.5 is negative class, is example 1 positive or negative?  is example 2 positive or negative?
  * Create a single ReLU unit and provide the outputs for those examples.
  * Calculate the derivative of the sigmoid with respect to net input for both examples
  * Calculate the derivative of the ReLU with respect to net input for both examples
  
  **Keypoint Detection with ORB**

  * Read https://opencv24-python-tutorials.readthedocs.io/en/latest/py_tutorials/py_feature2d/py_orb/py_orb.html (Links to an external site.)  and
https://opencv24-python-tutorials.readthedocs.io/en/latest/py_tutorials/py_feature2d/py_matcher/py_matcher.html (Links to an external site.)
  * Copy the example face image to Google drive and mount the drive
  * Load the example
  * Convert it to grayscale
  * Iterate through the keypoints and print the (x,y) location of the keypoints (hint: look at the documentation for the Keypoint class)
  * Create a version of the image that is rotated by 45 degrees using cv2.getRotationMatrix2D and cv2.warpAffine
  * Use cv2.BFMatcher() to find the descriptor matches between the two images
  * use cv2.drawMatches() to create an image that shows the correspondence. It will be easier to see the correspondences if you only show the best 20 matches
  
  **Face and Eye Detection using Haar Cascades**

  * Review the documentation on the Haar Cascade face detection system https://docs.opencv.org/3.4.15/db/d28/tutorial_cascade_classifier.html (Links to an external site.)
  * Create a face  Download faceand eye  Download eyecascade using these pretrained xml files
  * Read input image and convert to greyscale
  * Use detectMultiScale method to detect faces and eyes
  * Draw rectangles around the detected regions and show image
  * Provide the list of false positives (regions that were incorrectly detected as faces or eyes) and false negatives (faces and eyes that were missed by the detectors.  Do this by hand rather than attempting to write a program.
