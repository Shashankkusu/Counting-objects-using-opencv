# Counting Objects Using OpenCV

A simple Python/OpenCV project to detect and count objects in images using computer vision techniques.

## 🚀 Features

- Load an image using OpenCV  
- Convert to grayscale and apply blurring  
- Detect edges (e.g., using Canny)  
- Threshold and process the image (binary, flood‑fill, erosion/dilation)  
- Find and filter contours to count distinct objects  
- Visualize count and bounding outlines directly on the image  

## 📋 Requirements

- Python 3.x  
- OpenCV (`opencv-python`)  
- Pillow (PIL fork)  
- Tkinter (usually bundled with Python)

## 🛠 Installation

```bash
git clone https://github.com/Shashankkusu/Counting-objects-using-opencv.git
cd Counting-objects-using-opencv
```

If you don’t have a `requirements.txt`, just run:

```bash
pip install opencv-python pillow
```

## ⚙️ Usage

```bash
python counting_objects.py --image path/to/your/image.jpg
```

This runs the image-processing pipeline:

1. Read and display the input image  
2. Convert to grayscale and blur to reduce noise  
3. Detect edges using Canny (with dynamic thresholding)  
4. Threshold the image (binary + Otsu if desired)  
5. Optionally: flood-fill to remove background  
6. Morphological ops (erosion, dilation) to clean up  
7. Identify contours, filter out noise, and compute convex hull  
8. Count and annotate objects on output image  
9. Display or save the final result with annotated count  

## 🧠 How It Works

- **Grayscale & Blur:** Prepares image for edge detection  
- **Edge Detection:** Canny with adaptive thresholds (median-based)  
- **Threshold & Flood-Fill:** Segment foreground vs. background  
- **Morph Ops:** Clean small artifacts/noise  
- **Contour Detection:** External contours, filter by area  
- **Convex Hull:** Unified outline for overlapping shapes  
- **Counting:** Final count displayed on image with bounding box  

## 🔍 Tips for Better Object Detection

- Use grayscale + blur to minimize noise before edge detection
- Adaptive thresholding (like Otsu) improves segmentation
- Flood-fill helps remove fully connected backgrounds
- Tune contour area thresholds depending on object sizes
- Morph operations (open, close) help refine the final shapes



## 💡 Next Steps

- Add GUI (Tkinter) to choose images or directories interactively
- Support batch processing of image folders
- Switch to video input or live webcam
- Integrate ML-based detection (e.g., SSD, YOLO, Faster‑RCNN) for improved accuracy with complex images

## 📄 License & Credits

**Author:** Shashankkusu
