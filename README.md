# Description

	Obstacle detection or tracking moving objects is one of the most interesting topics in computer vision. 
	This problem could be solved in two steps:
  
	1, Detecting moving objects in each frame
	2, Tracking historical objects with some tracking algorithms
  
	An assignment problem is used to associate the objects detected by detectors and tracked by trackers.
  
	We can found some introduction of this framework here,

	https://towardsdatascience.com/computer-vision-for-tracking-8220759eee85
  
	An intriduction with matlab code,
  
	https://www.mathworks.com/help/vision/examples/motion-based-multiple-object-tracking.html

	Here I implemented a highly efficient and scalable C/C++ framework to combine the state of art deep-learning based detectors 
	(Yolo3 is used here) and correlation filters based tackers (KCF, Kalman is also implemneted). The assignment problem is 
	solved by hungrian algorithm.
  
# Detectors: Yolo3 

	Yolo3 is trained for detecting bottles, cans and hands in this demo. It is trained with a Keras model and compiled with 
	tensorflow C++ into a DLL (YOLO3.DLL under bin folder).

# Trackers: Kalman Filter and KCF

	Kalman filter is fast but less accurate. KCF is accurate but more accurate. 
	They are implemnted with exactly same external interface, so we can choose one in the project.

# Live Camera Capture: OpenCV

	OpenCV is used to capture live video frames and used for image preprocessing.