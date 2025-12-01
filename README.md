Gender and Age Detection Using Deep Learning

This project is a deep learning–based system that predicts a person’s gender and age group from an input image using a pre-trained convolutional neural network (CNN). The model takes a face image as input, processes it, and outputs:

Gender: Male / Female

Age Range: e.g., 0–2, 4–6, 8–12, 15–20, 25–32, 38–43, 48–53, 60+

🚀 Features

Detects faces in an image using OpenCV Haar Cascades / DNN face detector

Classifies gender (Male/Female)

Predicts age range

Works on images, webcam feed, and video files

Lightweight and fast inference

Clean folder structure for easy training and deployment

📁 Project Structure
gender-age-detection/
│
├── models/
│   ├── age_deploy.prototxt
│   ├── age_net.caffemodel
│   ├── gender_deploy.prototxt
│   ├── gender_net.caffemodel
│
├── images/
│   └── sample1.jpg
│
├── src/
│   ├── detect.py
│   ├── utils.py
│
├── requirements.txt
├── README.md
└── main.py

🛠️ Technologies Used

Python 3.x

OpenCV

NumPy

Pre-trained Caffe Deep Learning Models

DNN-based face detection

⚙️ Installation
1. Clone this repository
git clone https://github.com/your-username/gender-age-detection.git
cd gender-age-detection

2. Install dependencies
pip install -r requirements.txt

▶️ Usage
Run on Webcam
python main.py

Run on an Image
python main.py --image images/sample1.jpg

Run on Video
python main.py --video input.mp4

📊 Model Details
Gender Model

Architecture: CNN (Caffe)

Output: Male, Female

Age Model

Output Ranges:

['(0-2)', '(4-6)', '(8-12)', '(15-20)',
 '(25-32)', '(38-43)', '(48-53)', '(60-100)']

Face Detector

OpenCV DNN model: res10_300x300_ssd_iter_140000.caffemodel

🧪 Sample Output

Input: Image with a face
Output:

Gender: Male
Age: 25–32


Bounding boxes and labels are drawn on the image.

🤖 How It Works

Detect face → crop face region

Preprocess input

Pass through Gender Model

Pass through Age Model

Display predictions

📌 Future Improvements

Train with custom datasets

Add emotion detection

Improve accuracy with TensorFlow / PyTorch models

Build a web UI using Flask/React
