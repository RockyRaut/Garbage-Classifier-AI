# WasteSenseAI

WasteSenseAI is an Android app for real-time garbage classification using on-device AI. It uses a TensorFlow Lite model to classify waste as "Recyclable" or "Non-Recyclable" (or more classes, depending on your model and label file).

## Features
- Real-time camera classification
- Photo import and classification
- Modern Material UI
- On-device TensorFlow Lite inference
- Customizable model and label support

## Requirements
- Android Studio (latest recommended)
- Android device or emulator (API 21+)
- TensorFlow Lite model (`model.tflite`)
- Label file (`label.txt`)

## Setup
1. **Clone or download this repository.**
2. **Add your model and label file:**
   - Place your `model.tflite` and `label.txt` in `app/src/main/assets/`.
   - `label.txt` should have one class name per line (e.g., "Recyclable", "Non-Recyclable").
3. **Open the project in Android Studio.**
4. **Build and run the app** on your device or emulator.

## Model & Label File
- The app supports both classification and detection models, but is currently set up for classification (e.g., [1, 2] output for binary classification).
- Make sure your `label.txt` matches the number and order of classes your model predicts.
- For best results, use a TFLite model trained for your specific waste classes.

## Usage
- Launch the app.
- Grant camera permissions.
- Use the camera to classify waste in real time, or import a photo from your gallery.
- The top predicted class and confidence will be shown in the UI.

## Customization
- To use a different model or more classes, replace `model.tflite` and update `label.txt` accordingly.
- For object detection models, additional code changes may be required.

## Troubleshooting
- If you see "Model or labels not loaded", check that your files are in `app/src/main/assets/` and named correctly.
- If you see "Unsupported model output", your model's output shape may not be supported by the current code.
- Check Logcat for detailed error messages.

## License
This project is for educational and research purposes. See LICENSE for details.

---

**Developed by:**
- Kushal Kunwar
- Rocky Raut
- Utsab Baral
- Prajwal Lamsal
