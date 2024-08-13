## REAL TIME FACE RECOGNITION SYSTEM 
***

## STEP-1
Firstly open terminal and type:
- pip install -r requirements.txt

## Step-2

# 1. face_taker.py
### Purpose: Capture and save 30 images of a user's face. It also saves the user ID and name in a names.json file.

### Usage:

### Run the script:

### bash
### Copy code
python face_taker.py
### Enter the user name when prompted.

### Ensure your face is centered in the camera frame. The script will automatically save 30 images of your face to the images folder.

### The names.json file will be updated with the association between the ID number and user name.

# 2. face_train.py
### Purpose: Train a face recognition model using the images captured by face_taker.py and save the trained model to trainer.yml.

### Usage:

### Run the script:

### bash
### Copy code
python face_train.py
### The script will read images from the images folder, train the model, and save it as trainer.yml.

# 3. face_recognizer.py
### Purpose: Recognize faces using the trained model. The script will display the recognized names based on the ID numbers.

### Usage:

### Run the script:

### bash
### Copy code
python face_recognizer.py
### The script will use the trainer.yml file to recognize faces and display the corresponding names. Make sure the names.json file is in the same directory for name-to-ID mapping.


## Notes
Ensure the haarcascade_frontalface_default.xml file is available in the directory for face detection.
The system uses OpenCV's LBPH (Local Binary Pattern Histograms) face recognizer. Ensure opencv-contrib-python is installed.


## Troubleshooting
AttributeError: If you encounter issues related to cv2.face.LBPHFaceRecognizer_create(), ensure you have the correct version of opencv-contrib-python installed.
Image Saving Issues: Ensure the images folder exists and has write permissions.