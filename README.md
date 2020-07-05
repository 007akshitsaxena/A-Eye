# AI powered automated attendance monitoring system
This project is an automated attendance monitoring system having a producer/consumer system architecture. First component(producer) is Android application feeds video stream over the internet to the second core component(consumer) a web-server(Flask), which runs machine learning algorithms to process received video feeds and finally generate attendance sheet.

## About Web-Server
- For running `student.py` as web service I used Flask microweb framework.
- A quick review of machine learning algorithms.
  - I have used face_recognition library (author: Adam Geitgey)
  - Pipeline of standard and Deep learning algorithms was designed in same order to solve face_recognition
    - Histogram of Oriented Gradients (HoG) : This algoritms is used to locate faces in whole image.
    - Facial Landmark estimation : To overcome the problem of different poses/posture of faces this algo marks 68 specific locations on every      face.
    - Convolutional Neural Network (CNN): This algorithms performs face encoding by generating embeddings(128-D feature matrix) for each face.
    - Support Vector Machine (SVM): This algorithm perform final classification task.
- If you want to try
  - Make sure you are using python=3.3 or greater version and better to make separate virtual environment
  - Refer this link to install face_recognition library: https://github.com/ageitgey/face_recognition
  - Once done move inside your directory where you clone and run this on shell `pip install -r requirements.txt`
  - Web-server is ready to use.

Interested in detail explanation of machine learning algorithms refer [this.](https://medium.com/@ageitgey/machine-learning-is-fun-part-4-modern-face-recognition-with-deep-learning-c3cffc121d78)
