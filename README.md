#Advanced Lane Finding

Advanced road lane finding based on conventional image processing methods.

##Undistorting Images

To undistort the effect of camera lense on images, I use OpenCV and chessboard images to find distortion matrix and calibration coefficient. For this purpose, two arrays namely objpoints and imgpoints are defined. Objpoints stores the 3D points of the real world, but since we are taking 2D reference, z value is alway zero in this case. Imgpoint stores the values of found corners in each chess board image. The corners are appended each time to the end of the imgpoints array. The function used to find the corners is cv2.findChessboardCorners and the finction to calculate distortion matrix is cv2.calibrateCamera. Moreover, a function named undistort() is defined, which accepts an image and outputs the undistorted one. Here is the result of such transformation:

![Distorted Iage](report/undistorted_image.png) 



