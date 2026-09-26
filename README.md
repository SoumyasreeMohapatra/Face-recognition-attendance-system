# Face Recognition (Keras + OpenCV)

This project loads a trained face classification model (`fac.h5`) and detects faces using a Haar cascade to label faces from a camera endpoint (`shot.jpg`).

## What it expects
- A model file: `Face_Recognition_Attendance_System/fac.h5`
- A Haar cascade file: `Face_Recognition_Attendance_System/haarcascade_frontalface_default (1).xml`
- A camera/server that serves a JPEG at:
  - default: `http://192.168.1.38:8080/shot.jpg`


## Setup (Windows/Linux)
1. Install Python 3.9+.
2. Create and activate a virtual environment.
3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

## Run
```bash
python soumyashree/recognize.py
```

## Customize the camera URL
Edit `URL = "http://.../shot.jpg"` inside `soumyashree/recognize.py` (or change it to use an env var if you prefer).

## Notes
- The scripts are designed for local/offline camera endpoints and use `cv2.imshow()` for display.
- For GitHub deployment as a hosted service, the code would need a web API rewrite (Flask/FastAPI) rather than a desktop window + polling.

