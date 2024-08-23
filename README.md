
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

# Edge Detection and Sharpening

### Image Sharpening

1. **High-Pass Filtering**: Enhances edges by amplifying pixel differences using a convolutional filter.
1. **Laplacian Sharpening**: Sharpens the image by subtracting a Laplacian-filtered version from the original.
1. **Unsharp Masking**: Enhances details by subtracting a blurred image from the original.
1. **Frequency Domain Filtering**: Sharpens the image by applying a high-pass filter in the frequency domain.

### Edge Detection

1. **Canny Edge Detection**: Detects edges by identifying areas of rapid intensity change using the Canny algorithm.
1. **Adaptive Edge Detection**: Dynamically detects edges using threshold values based on the image's mean intensity.

