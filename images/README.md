# Computer Vision & OpenCV Images Directory (`images/`)

This directory houses dedicated image assets utilized across the `08_opencv` interactive Jupyter notebook curriculum.

## Catalog of Assets

| File Name | Format | Dimensions | Channels | Description & Pedagogical Usage |
| :--- | :--- | :--- | :--- | :--- |
| **`landscape.jpg`** | JPEG | 480 × 640 | 3 (BGR) | Rich outdoor scene featuring twilight sky gradient, sun, mountain silhouettes, shoreline trees, and water reflections. Used for **Color Spaces (RGB, HSV, LAB)**, **Luminance Channel Extraction**, and **Histogram Equalization / CLAHE**. |
| **`shapes.png`** | PNG | 500 × 600 | 3 (BGR) | Multi-colored high-contrast geometric shapes (circle, rectangle, triangle, star, pentagon). Used for **Contour Detection**, **Douglas-Peucker Polygon Approximation (`approxPolyDP`)**, **Oriented Bounding Boxes**, and **HSV Color Masking**. |
| **`document.png`** | PNG | 620 × 480 | 3 (BGR) | Simulated business analytics invoice with header bar, text lines, table cells, and uneven directional shadow illumination. Used for **Global vs. Adaptive Thresholding**, **Morphological Illumination Correction**, and **Perspective Deskewing**. |
| **`noisy_sample.png`** | PNG | 400 × 500 | 3 (BGR) | Structured concentric discs degraded with additive Gaussian noise and Salt-and-Pepper impulse noise. Used for **Filter Comparison (Gaussian vs. Median vs. Bilateral Filtering)**. |
| **`query_object.png`** | PNG | 160 × 160 | 3 (BGR) | Distinctive high-frequency geometric emblem badge. Serves as the template query for **Feature Detection (ORB)**, **Descriptor Matching**, and **Multi-Scale Template Matching**. |
| **`scene_search.jpg`** | JPEG | 500 × 700 | 3 (BGR) | Cluttered desktop scene with background grid, distractors, and `query_object.png` embedded with affine rotation and scaling. Used for **ORB Keypoint Matching (BFMatcher / FLANN)** and **RANSAC Homography Localization**. |
| **`coins_cells.png`** | PNG | 420 × 540 | 3 (BGR) | Clustered and touching circular discs/cells on a dark background. Used for **Euclidean Distance Transform (`distanceTransform`)** and **Watershed Segmentation Algorithm** to separate overlapping objects. |

---

## Loading Images in Python Notebooks

All notebooks implement dynamic path resolution to ensure seamless execution from either the repository root or module subfolders:

```python
import os
import cv2
import matplotlib.pyplot as plt

# Dynamic path resolution
img_dir = "images" if os.path.exists("images") else "../images"
img_path = os.path.join(img_dir, "landscape.jpg")

# Load image in BGR format
bgr_img = cv2.imread(img_path)

# Convert to RGB for proper rendering with Matplotlib
rgb_img = cv2.cvtColor(bgr_img, cv2.COLOR_BGR2RGB)

plt.figure(figsize=(8, 5))
plt.imshow(rgb_img)
plt.axis("off")
plt.show()
```
