# OpenCV_new
explanation of the code:

import cv2: imports the OpenCV library.
cap = cv2.VideoCapture(0): creates a VideoCapture object to capture video from the default camera (with index 0).
while True:: creates an infinite loop that will keep running until a break statement is encountered.
ret, frame = cap.read(): reads a frame from the camera and stores it in the variable frame. The return value ret indicates whether the operation was successful or not.
inversed = ~frame: inverts the frame by taking the bitwise NOT operation of each pixel value. This results in a negative image.
cv2.imshow('frame', frame): displays the original frame in a window with the title 'frame'.
cv2.imshow('inversed', inversed): displays the inverted frame in a window with the title 'inversed'.
if cv2.waitKey(10) == 27 : break: waits for a key press for 10 milliseconds. If the key pressed is the escape key (27 in ASCII), the loop breaks.
cap.release(): releases the resources used by the VideoCapture object.
cv2.destroyAllWindows(): closes all the windows created by OpenCV.
