# Face-mask-detector
This project is an idea that popped up when COVID-19 pandemic was spreading violently. When offline classes were about to start at our college, me and my professor worked on a code to monitor the students and allow only those who wore masks. This involved analysing the real-time data with the help of the model and approve entry only if the students have masks and deny if they don't. I would like to appreciate and thank my professor Prasad who helped me to complete this project.

Import necessary packages, including TensorFlow, OpenCV, and imutils for video handling and image processing.

Define a function called detect_and_predict_mask that takes a frame, a face detection model (faceNet), and a face mask detection model (maskNet) as input. This function detects faces in the frame, extracts them, and then uses the maskNet to predict whether the detected faces are wearing masks or not.

Load a pre-trained face detection model (faceNet) and a pre-trained face mask detection model (maskNet) from disk. These models are used to detect faces in the frame and classify whether each detected face is wearing a mask.

Initialize a video stream using the VideoStream class from the imutils library.

Start a loop to continuously process frames from the video stream.

Inside the loop, read a frame from the video stream and resize it to have a maximum width of 400 pixels.

Call the detect_and_predict_mask function to detect faces in the resized frame and predict whether they are wearing masks or not.

Iterate over the detected face locations and their corresponding predictions. For each detected face, determine the class label ("Mask" or "No Mask") based on the prediction probabilities. Draw a bounding box around the face and display the label with the associated probability on the frame.

Show the output frame with bounding boxes and labels.

Continuously check for the "q" key press. If the "q" key is pressed, break from the loop.

Perform cleanup by closing the OpenCV windows and stopping the video stream.

This code allows you to run real-time face mask detection using your webcam or camera feed. It uses deep learning models for face detection and mask classification, providing visual feedback on whether individuals in the video feed are wearing masks or not.
