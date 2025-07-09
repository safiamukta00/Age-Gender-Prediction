# Age and Gender Prediction from Faces

## Project Overview
This project uses pretrained Convolutional Neural Networks (CNNs), loaded through OpenCV’s DNN module, to detect human faces from an image and predict:
- **Gender**: Male / Female
- **Age group**: e.g., (0–2), (25–32), (60–100)

All models are pre-trained using the Caffe framework and require no training or dataset preparation by the user.

---

## Model Files Used
- **Face Detection**:
  - `opencv_face_detector.pbtxt`
  - `opencv_face_detector_uint8.pb`
- **Age Prediction**:
  - `age_deploy.prototxt`
  - `age_net.caffemodel`
- **Gender Prediction**:
  - `gender_deploy.prototxt`
  - `gender_net.caffemodel`

### Class Labels
- **Age Groups**: `(0-2)`, `(4-6)`, `(8-12)`, `(15-20)`, `(25-32)`, `(38-43)`, `(48-53)`, `(60-100)`
- **Gender**: `Male`, `Female`

---

## Dependencies
- Python
- OpenCV (`opencv-python`)
- Pretrained Caffe models (provided in `models/` folder)

### Install Requirements
```bash
pip install opencv-python
```

---

## How to Run the Code
1. Clone this repository and download all required model files into a `models/` folder.
2. Place an image file (e.g., `flower.jpg`) in the project directory.
3. Run the Python script:
```bash
python age_gender_predictor.py
```

4. The output will display the image with:
   - Detected face boxes
   - Predicted gender and age group written above each face

---

## Output Example
![sample](sample_output.jpg)  
> Detected face → "Female, (25–32)"

---

## Model Performance
These models are trained by researchers and benchmarked as follows:
- **Gender prediction accuracy**: ~91–94%
- **Age group prediction error (MAE)**: ±4–5 years

---

## Project Structure
```
├── age_gender_predictor.py
├── flower.jpg
├── models/
│   ├── age_deploy.prototxt
│   ├── age_net.caffemodel
│   ├── gender_deploy.prototxt
│   ├── gender_net.caffemodel
│   ├── opencv_face_detector.pbtxt
│   └── opencv_face_detector_uint8.pb
└── README.md
```

---

## Notes
- Models are used as-is; no training or fine-tuning is needed.
- Accuracy may vary based on lighting and face visibility.
- Works best on front-facing, clear face images.

---

## Author
[Safia Sultana Muktha]
