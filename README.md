# Machine-Vision-with-MATLAB

#### **Objective:**
This project is designed to explore various advanced image processing and computer vision techniques using MATLAB. The project encompasses a wide range of tasks, from basic image handling and manipulation to more complex tasks such as video processing, camera calibration, and high dynamic range (HDR) imaging. The overall goal is to develop a comprehensive understanding of how to work with images and videos in MATLAB, and how to apply these techniques to practical applications in computer vision.

---

### **Task 1: Image Handling and Conversion**

#### **1.1 Reading, Displaying, and Saving Images**
- **Goal:** Learn to import, manipulate, and save images in different formats.
- **Subtasks:**
  - **Image Importing:** Use `imread` to load a compressed color image (e.g., JPG) into MATLAB and examine its data structure, data type, and value range.
  - **Image Metadata:** Retrieve detailed image information using `imfinfo`, and extract image dimensions.
  - **Image Exporting:** Save the image in a different format (e.g., PNG, TIF) and display it.

#### **1.2 Converting Images to Grayscale and Binary**
- **Goal:** Convert RGB images to grayscale and binary, and explore different image representations.
- **Subtasks:**
  - **Grayscale Conversion:** Manually convert an RGB image to grayscale by averaging color channels, ensuring the result is of type `uint8`.
  - **Bit Depth Reduction:** Save the grayscale image with reduced bit depth and examine the quantization effects.
  - **Binary Conversion:** Convert the grayscale image to binary using a threshold, and compare it with the grayscale version.
  - **HSV Conversion:** Convert the RGB image to HSV and explore the different channels.

#### **1.3 Image Representation Techniques**
- **Goal:** Visualize images using various colormaps and 3D surface plots.
- **Subtasks:**
  - **Colormaps:** Display a grayscale image using different colormaps with the `subplot` and `imshow` functions.
  - **3D Surface Plotting:** Create a 2D surface plot of an image using the `surf` function and project the image onto the surface.

#### **1.4 Video Processing from a USB Webcam**
- **Goal:** Capture and process video frames from a webcam, and manipulate image properties in real-time.
- **Subtasks:**
  - **Webcam Setup:** Identify available webcams, capture and display live images.
  - **Frame Manipulation:** Write a script to capture frames, adjust camera settings (e.g., brightness), and display modified images in real-time.
  - **Video Processing:** Implement a loop to continuously capture, process, and display frames, with the ability to manipulate camera properties dynamically.

---

### **Task 2: Advanced Image Manipulation**

#### **2.1 Displaying and Saving Image Sections**
- **Goal:** Learn to work with and manipulate specific regions within an image.
- **Subtasks:**
  - **Image Sections:** Load an image, extract specific sections, and display them.
  - **Gray Value Isolation:** Modify the image to highlight only grayscale values, setting other values to black.

#### **2.2 Creation of Artificial Test Images**
- **Goal:** Generate and manipulate synthetic images for testing purposes.
- **Subtasks:**
  - **Random Noise:** Create images with uniformly and normally distributed noise and examine the effects of varying mean and variance.
  - **Striped Pattern:** Generate an image with increasing stripe widths.
  - **Simulating Noise:** Apply different types of noise (e.g., Gaussian, Poisson) to an image and analyze the effects using the `imnoise` function.

#### **2.3 Visualization of Coordinates and Regions of Interest (ROI)**
- **Goal:** Learn to draw shapes and highlight regions within an image.
- **Subtasks:**
  - **Drawing Shapes:** Use `insertShape` to draw lines, rectangles, and circles in an image.
  - **Custom Cross Function:** Develop a function to draw a cross at specified coordinates.

#### **2.4 Drawing with the Bresenham Algorithm**
- **Goal:** Implement the Bresenham algorithm for efficient line drawing.
- **Subtasks:**
  - **Algorithm Implementation:** Create a function that computes the coordinates of a line using the Bresenham algorithm.
  - **Visualization:** Display the line on an image by setting the corresponding pixels to red.

#### **2.5 High Dynamic Range (HDR) Imaging**
- **Goal:** Create and process HDR images by combining images with different exposures.
- **Subtasks:**
  - **HDR Image Creation:** Capture or use provided images with varying exposures, combine them into an HDR image, and map the result back to the standard RGB color space.

---

### **Task 3: Camera Calibration and Pose Estimation**

#### **3.1 Decomposition of a Projection Matrix with RQ Decomposition**
- **Goal:** Decompose a projection matrix to extract camera calibration and rotation matrices.
- **Subtasks:**
  - **RQ Decomposition:** Implement the RQ decomposition by leveraging the QR decomposition method.
  - **Calibration Matrix Extraction:** Calculate the calibration matrix, rotation matrix, and translation vector, and verify the results.

#### **3.2 Camera Pose Estimation from Four Known Points**
- **Goal:** Estimate the camera's pose based on known 3D points and corresponding 2D image points.
- **Subtasks:**
  - **Normalization:** Convert pixel coordinates to normalized image coordinates.
  - **Homography Calculation:** Use Direct Linear Transformation (DLT) to compute the homography matrix.
  - **Pose Extraction:** Extract the camera's rotation matrix and translation vector from the homography.

#### **3.3 Webcam Calibration with MATLAB Camera Calibrator**
- **Goal:** Calibrate a webcam using a checkerboard pattern and MATLAB’s camera calibration tools.
- **Subtasks:**
  - **Calibration Setup:** Capture images of a checkerboard, calibrate the camera, and save the calibration parameters.
  - **Session Management:** Save the calibration session for future use.

#### **3.4 Camera Localization and Tracking**
- **Goal:** Track the camera's position relative to a visual landmark (checkerboard).
- **Subtasks:**
  - **Pose Calculation:** Use detected checkerboard points to calculate and visualize the camera’s pose.
  - **Real-Time Tracking:** Implement real-time camera pose tracking using live video feed.

---

### **Task 4: Image Enhancement and Analysis**

#### **4.1 Rearrangement of Color Values**
- **Goal:** Experiment with color manipulation and sorting techniques.
- **Subtasks:**
  - **Image Rotation:** Rotate and flip images without using the built-in `imrotate` function.
  - **Grayscale Conversion:** Convert a color image to grayscale and sort the pixel values.

#### **4.2 Homogeneous Point Operators and Lookup Tables**
- **Goal:** Apply point operators and enhance images using lookup tables.
- **Subtasks:**
  - **Constant Addition/Subtraction:** Modify image brightness and contrast by adding/subtracting constants.
  - **Scaling:** Scale the grayscale image to the full value range [0, 255].
  - **Contrast Spreading:** Adjust contrast within specified value ranges and observe the effects.
  - **Gray Value Compression:** Implement gamma compression and evaluate performance using lookup tables.

#### **4.3 Image Statistics and Histogram Analysis**
- **Goal:** Calculate basic image statistics and perform histogram-based contrast enhancement.
- **Subtasks:**
  - **Statistical Measures:** Compute the mean, standard deviation, and autocorrelation of an image.
  - **Histogram Equalization:** Enhance contrast using global and local histogram equalization techniques.

#### **4.4 Moving Silhouettes via Background Subtraction**
- **Goal:** Implement a basic motion detection algorithm by comparing frames from a video stream.
- **Subtasks:**
  - **Background Modeling:** Compute a dynamic background model using weighted averages of previous frames.
  - **Silhouette Extraction:** Subtract the background model from the current frame and threshold the result to highlight moving objects.
  - **Color Channel Processing:** Experiment with HSV channels for silhouette extraction.

---

### **Conclusion:**
This project provides a comprehensive exploration of image processing and computer vision techniques using MATLAB. By completing the tasks, you will gain practical skills in handling images, analyzing their properties, and applying advanced methods such as HDR imaging, camera calibration, and real-time video processing. The project serves as a robust foundation for further exploration in the field of computer vision.
