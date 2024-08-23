
# Color Space and Filters

This code contains simple tasks which are:

### **Channel Separation and Visualization**
   - Separates and visualizes the Red, Green, and Blue color channels of the image.

### **Grayscale and Binary Conversion**
   - Converts the image to grayscale and then to a binary format using thresholding which is implemented from scratch.

### **RGB to HSV Conversion**
   - Manually converts the image from RGB to HSV color space for better color-based analysis by calculating values.

### **Color Extraction Using HSV**
   - Extracts and displays the red regions of the image using HSV filtering.

### **Histogram Matching**
   - Matches the color histogram of one image to another for consistent color distribution.

### **Noise Reduction**
   - Applies a median filter to remove salt-and-pepper noise from the image.

### **Image Sharpening**
   - Enhances image details by applying sharpening filters.

### **Histogram Equalization**
   - Improves image contrast using histogram equalization techniques which is implemented from scratch.

### **Star Detection**
   - Detects and counts stars in a noisy image, using simple methods.

---

# Edge Detection and Sharpening

### Image Sharpening

1. **High-Pass Filtering**: Enhances edges by amplifying pixel differences using a convolutional filter.
1. **Laplacian Sharpening**: Sharpens the image by subtracting a Laplacian-filtered version from the original.
1. **Unsharp Masking**: Enhances details by subtracting a blurred image from the original.
1. **Frequency Domain Filtering**: Sharpens the image by applying a high-pass filter in the frequency domain.

### Edge Detection

1. **Canny Edge Detection**: Detects edges by identifying areas of rapid intensity change using the Canny algorithm.
1. **Adaptive Edge Detection**: Dynamically detects edges using threshold values based on the image's mean intensity.

---

# Road Lines Detection

This code extracts roads lines without using neural networks. First of all, a noise reduction is applied  on image using a Gaussian filter. The edges are identified using the Canny edge detection algorithm, which highlights areas with significant changes in intensity, typically corresponding to edges. To focus on the road, a specific region of interest (ROI) is defined, masking out irrelevant parts of the image so that only the edges within this area are considered. The Hough Transform technique is then applied to detect straight lines within the masked edges, which are likely to represent the road lines. These detected lines are filtered based on their slope to exclude any lines that do not align with the expected orientation of road lines, such as vertical or horizontal lines that may be irrelevant.

---
# Histogram of Oriented Gradients (HOG)

Detects and locate specific sub-images within a larger image using Histogram of Oriented Gradients (HOG) features and template matching. HOG is employed to extract edge and shape information from both the larger image and the smaller cropped images, capturing the structural details that make object detection effective. The code then uses template matching to compare the HOG representations of the cropped images against the original image, identifying the regions where these sub-images are most likely located. When a match with sufficient similarity is found, the code draws bounding boxes around the detected areas in the original image to highlight where each cropped image appears. Finally, it visualizes the results by displaying the original image with these bounding boxes and the matched cropped images, allowing for an intuitive understanding of the detection and localization process.

---

# Scale-Invariant Feature Transform (SIFT)

detect and match features between a reference image and a set of cropped images. The algorithm uses the SIFT (Scale-Invariant Feature Transform) method to extract distinctive keypoints and descriptors from both the reference image and the cropped images. Once keypoints and descriptors are extracted, a matching process is carried out using the FLANN (Fast Library for Approximate Nearest Neighbors) based matcher, which efficiently finds matches between the descriptors from the reference image and the cropped images. If sufficient good matches are found, the algorithm computes a homography matrix, which represents the transformation needed to align the cropped image with its corresponding part in the reference image.