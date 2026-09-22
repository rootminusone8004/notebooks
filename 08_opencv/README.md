# Module 08: OpenCV for Computer Vision & Machine Learning

Welcome to **Module 08: OpenCV for Computer Vision & Machine Learning**. This module bridges visual data processing, mathematical geometry, classical feature engineering, and statistical machine learning workflows.

---

## Pedagogical Progression

The curriculum spans **6 progressively structured interactive notebooks** designed to build deep competence in image arrays, spatial transformations, morphological processing, feature extraction, and ML integration:

```text
08_opencv/
├── 01_image_basics_io_and_colorspaces.ipynb
├── 02_geometric_transformations_and_drawing.ipynb
├── 03_filtering_blurring_and_morphology.ipynb
├── 04_edge_detection_and_contours.ipynb
├── 05_feature_detection_and_matching.ipynb
├── 06_practical_computer_vision_and_ml.ipynb
└── README.md
```

---

## Notebook Syllabus & Key Concepts

| Notebook | Focus Area | Foundational Concepts | Advanced & ML Applications |
| :--- | :--- | :--- | :--- |
| [**01_image_basics_io_and_colorspaces.ipynb**](01_image_basics_io_and_colorspaces.ipynb) | Image Representation, I/O & Color Spaces | • NumPy array image representation ($H \times W \times C$, `uint8`)<br>• `cv2.imread()` & `cv2.imwrite()` flags<br>• The BGR vs. RGB channel ordering pitfall<br>• ROI slicing, channel splitting & merging | • Color Spaces: RGB, HSV ($0 \le H \le 179$), and perceptually uniform LAB ($L^*a^*b^*$)<br>• **HSV Color Segmentation Pipeline** via `cv2.inRange()` and bitwise masking<br>• **CLAHE** on luminance ($L^*$) channel for natural contrast enhancement |
| [**02_geometric_transformations_and_drawing.ipynb**](02_geometric_transformations_and_drawing.ipynb) | Geometry, Resizing & Augmentation | • Drawing primitives (lines, bounding boxes, circles, text with `LINE_AA`)<br>• `cv2.resize()` with interpolation algorithms (`INTER_NEAREST`, `INTER_LINEAR`, `INTER_CUBIC`, `INTER_AREA`)<br>• Translation ($2 \times 3$), center rotation (`cv2.getRotationMatrix2D`), flipping | • **4-Point Perspective Transformation (Homography)** via `cv2.getPerspectiveTransform()` & `cv2.warpPerspective()` for document deskewing<br>• **VisionAugmenter Pipeline**: random flips, rotations, and affine scaling with synchronized bounding box transforms |
| [**03_filtering_blurring_and_morphology.ipynb**](03_filtering_blurring_and_morphology.ipynb) | Convolution, Filtering & Morphology | • 2D Spatial Convolution & custom kernels (`cv2.filter2D`)<br>• Smoothing: Average Blur, Gaussian Blur, Median Blur on salt-and-pepper noise<br>• Thresholding: Global, Adaptive Gaussian, and Otsu's bimodal thresholding | • **Bilateral Filtering** (`cv2.bilateralFilter`) for edge-preserving denoising<br>• Mathematical Morphology: Structuring elements, Erosion, Dilation, Opening, Closing, Morphological Gradient<br>• **Document Illumination Normalization Pipeline** to eliminate severe shadow gradients |
| [**04_edge_detection_and_contours.ipynb**](04_edge_detection_and_contours.ipynb) | Gradients, Canny & Contour Analysis | • Directional Sobel Gradients ($G_x, G_y$), Gradient Magnitude, and Laplacian<br>• Multi-stage Canny Edge Detection (Gaussian, NMS, Hysteresis)<br>• Contour retrieval (`cv2.findContours`) and visualization | • Spatial moments & centroids: $(\bar{x}, \bar{y}) = (M_{10}/M_{00}, M_{01}/M_{00})$<br>• **Douglas-Peucker Polygon Approximation** (`approxPolyDP`) for automated shape classification<br>• **Industrial Dimension Measurement Pipeline** with rotated minimum area rectangles (`cv2.minAreaRect`) and orientation angles |
| [**05_feature_detection_and_matching.ipynb**](05_feature_detection_and_matching.ipynb) | Invariant Features & Homography | • Corner detection: Harris response function $R = \det(M) - k(\text{Tr}(M))^2$ vs. Shi-Tomasi eigenvalue score<br>• Modern invariant feature extraction: **ORB** (Oriented FAST and Rotated BRIEF)<br>• Binary descriptor matching: Brute-Force (`NORM_HAMMING`) and FLANN | • **Lowe's Ratio Test** on $k$-Nearest Neighbors ($k=2$, distance ratio $< 0.75$)<br>• **Robust Object Localization via RANSAC Homography** (`cv2.findHomography` with `cv2.RANSAC`) to project target boundaries into cluttered scenes |
| [**06_practical_computer_vision_and_ml.ipynb**](06_practical_computer_vision_and_ml.ipynb) | ML Pipelines, HOG & Watershed | • Multi-scale image pyramid template matching (`cv2.matchTemplate`)<br>• **Marker-Controlled Watershed Algorithm** with Euclidean Distance Transform (`cv2.distanceTransform`) to segment touching objects<br>• HOG (Histogram of Oriented Gradients) feature extraction (`cv2.HOGDescriptor`) | • **End-to-End Scikit-Learn Image Classifier**: HOG feature vectors + Support Vector Classifier (`SVC`), evaluated with Confusion Matrix and classification reports<br>• **Deep Learning Vision Inference with OpenCV DNN (`cv2.dnn`)**: 4D NCHW input blob construction via `cv2.dnn.blobFromImage` |

---

## Image Asset Integration

All notebooks dynamically resolve paths to the dedicated root [`images/`](../images) directory:

```python
import os
import cv2

# Dynamic path resolution
img_dir = "images" if os.path.exists("images") else "../images"
img_bgr = cv2.imread(os.path.join(img_dir, "landscape.jpg"))
```

Refer to [`images/README.md`](../images/README.md) for full asset specifications, color spaces, and resolution details.
