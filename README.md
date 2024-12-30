# EmotionGenderClassification
# Instructions

Run real-time emotion demo:
python3 video_emotion_color_demo.py

Run real-time guided back-prop demo:
python3 image_gradcam_demo.py

Make inference on single images:
python3 image_emotion_gender_demo.py <image_path>
e.g.
python3 image_emotion_gender_demo.py ../images/test_image.jpg

Running with Docker
With a few steps one can get its own face classification and detection running. Follow the commands below:
docker pull ekholabs/face-classifier
docker run -d -p 8084:8084 --name=face-classifier ekholabs/face-classifier
curl -v -F image=@[path_to_image] http://localhost:8084/classifyImage > image.png
