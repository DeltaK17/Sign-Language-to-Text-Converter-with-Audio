# Sign Language to Text Converter with Audio

This project bridges communication gaps by converting sign language gestures into text and audio, improving accessibility for individuals who use sign language. The system uses real-time gesture recognition and text-to-speech technology to facilitate seamless communication.

---

## Features

- **Gesture Recognition**: Detects and classifies hand gestures using a CNN model.
- **Text-to-Speech Conversion**: Converts recognized text into audio.
- **Real-time Processing**: Processes input from a webcam and generates output in real-time.
- **User-friendly Interface**: Intuitive GUI for displaying detected characters, suggestions, and sentences.
- **Suggestions**: Displays word suggestions for improved text accuracy.
- **Audio Output**: Allows the generated text to be spoken aloud.

---

## Installation

### 1. Clone the Repository
First, clone this repository to your local system:
```bash
git clone https://github.com/DeltaK17/Sign-Language-to-Text-Converter-with-Audio.git
cd Sign-Language-to-Text-Converter-with-Audio
```

---

### 2. Install Anaconda
Download and install Anaconda from the [official website](https://www.anaconda.com/products/distribution).

---

### 3. Set Up the Conda Environment
You can either create a new environment manually or use the provided Conda environment file.

####  Create a New Conda Environment
1. Create the environment with Python 3.8.20:
   ```bash
   conda create -n signlang_env python=3.8.20
   ```
2. Activate the environment:
   ```bash
   conda activate signlang_env
   ```
3. Install dependencies:
   ```bash
   conda install numpy opencv keras matplotlib mediapipe scipy
   pip install pyttsx3 cvzone pyenchant
   ```


---

### 4. Install Missing Dependencies
If any libraries are missing, install them manually:
```bash
conda install numpy opencv keras matplotlib mediapipe scipy
pip install pyttsx3 cvzone pyenchant
```

---

### 5. Configure PyCharm
If you're using **PyCharm** for development, follow these steps:

1. **Open Your Project**: Launch PyCharm and open the folder containing your project files.
2. **Configure the Conda Environment**:
   - Go to **File** > **Settings** (or **PyCharm** > **Preferences** on macOS).
   - Navigate to **Project: <project_name>** > **Python Interpreter**.
   - Click the gear icon ⚙️ and select **Add...**.
   - Choose **Conda Environment** and select the `signlang_env` you created.
3. **Install Missing Packages**: Use the PyCharm terminal to install any missing dependencies:
   ```bash
   conda install numpy opencv keras matplotlib mediapipe scipy
   pip install pyttsx3 cvzone pyenchant
   ```
4. **Configure the Run Script**:
   - Go to **Run** > **Edit Configurations...**.
   - Click **+ Add New Configuration** and select **Python**.
   - Set the script path to `final_pred.py`.
   - Set the working directory to your project folder.
   - Select your Conda environment as the interpreter.

---

## Running the Project

### 1. Run the Script in PyCharm
- Click the **Run** button (green triangle) in PyCharm.
- The GUI will launch, allowing you to interact with the application.

### 2. Run the Script in Terminal
- Navigate to your project folder.
- Activate the Conda environment:
  ```bash
  conda activate signlang_env
  ```
- Run the application:
  ```bash
  python final_pred.py
  ```

---

## Technical Details

### Requirements
- **Python Version**: 3.8.20 or python version > 3.8
- **Dependencies**:
  - Mediapipe, NumPy, OpenCV, Keras, Matplotlib, Scipy
  - Additional packages: Pyttsx3, Cvzone, PyEnchant

### Components
1. **Hand Tracking**: Detects hand landmarks using Mediapipe.
2. **Gesture Recognition**: Uses a CNN model (`cnn8grps_rad1_model.h5`) for gesture classification.
3. **GUI**: Built with Tkinter for displaying text, suggestions, and output.
4. **Text-to-Speech**: Converts recognized text into audio using Pyttsx3.

---

## Folder Structure

```plaintext
├── final_pred.py         # Main application script
├── cnn8grps_rad1_model.h5 # Pre-trained model for gesture recognition
├── white.jpg             # Background image for processing gestures
├── requirements.txt      # pip requirements file
```

---

## Future Improvements

- Support for additional languages and gestures.
- Enhance gesture recognition accuracy.
- Implement dynamic gesture recognition for phrases.
- Optimize processing speed for real-time applications.

---

## License

This project is licensed under the MIT License. See the `LICENSE` file for details.

