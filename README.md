# Count Number of Faces using Python - OpenCV

A simple computer vision project that detects human faces in an image and counts how many are present. Instead of extracting detailed facial features (eyes, nose, mouth, etc.), the goal is to obtain **bounding boxes** around each detected face — the coordinates are then used to determine and display the total number of faces found.

## 🧠 How It Works

1. An image is captured (via webcam, using JavaScript embedded in Google Colab).
2. The image is converted to grayscale for faster and more accurate detection.
3. [`dlib`](http://dlib.net/)'s frontal face detector locates faces in the image and returns bounding box coordinates for each one.
4. A green rectangle is drawn around every detected face.
5. The total number of faces detected is printed to the console.

## ✨ Features

- Real-time webcam image capture (Google Colab compatible)
- Face detection using `dlib`'s HOG-based frontal face detector
- Bounding box visualization with OpenCV
- Face count output

## 📦 Requirements

- Python 3.x
- [OpenCV](https://pypi.org/project/opencv-python/) (`opencv-python`)
- [dlib](http://dlib.net/)
- NumPy
- Google Colab environment (for webcam capture via `IPython.display` and `google.colab`)

Install the dependencies:

```bash
pip install opencv-python dlib numpy
```

> **Note:** The webcam capture function in this script relies on `google.colab.output` and `google.colab.patches`, so it is designed to run inside a **Google Colab notebook**. If you want to run it locally (outside Colab), you'll need to replace the `capture_image()` function with a local webcam capture method (e.g. `cv2.VideoCapture(0)`) and swap `cv2_imshow()` for `cv2.imshow()`.

## 🚀 Usage

### On Google Colab

1. Open the notebook in [Google Colab](https://colab.research.google.com/).
2. Run all cells.
3. Grant camera permission when prompted by the browser.
4. The webcam will activate, capture a frame after ~2 seconds, and the script will:
   - Detect all faces in the captured image
   - Draw bounding boxes around them
   - Print the total number of faces detected
   - Display the annotated image

### Running the Script

```bash
python count_number_of_faces_using_python_opencv.py
```

## 📁 Project Structure

```
Count-number-of-Faces-using-Python---OpenCV/
├── count_number_of_faces_using_python_opencv.py   # Main script
└── README.md
```

## 📝 Example Output

```
Faces detected: 2
```

The captured image is displayed with green rectangles drawn around each detected face.

## 🔧 Possible Improvements

- Add support for local webcam capture (no Colab dependency)
- Use a more robust detector (e.g. `dlib`'s CNN-based detector or `MTCNN`) for better accuracy in varied lighting/angles
- Add support for detecting faces from uploaded images or video streams
- Save annotated output images to disk

## 📄 License

This project currently has no license specified. Consider adding one (e.g. MIT) if you'd like others to reuse this code.

## 🙋 Author

**Vicky Rana** 
