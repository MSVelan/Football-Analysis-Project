# Football-Analysis-Project

## Things implemented

- This project detects and tracks players, referees and football across the whole video using YOLO. I have fine tuned the YOLOv8 model for this specific purpose.
- The players are assigned to teams according to the t-shirt colors they are wearing. For this, I have segmented the player and cluster pixels with KMeans
  to only choose t-shirt pixels from the players' bounding box.
- I have also measured the team's ball acquisition in the match.
- I have used optical flow to measure the camera movement from one frame to another to precisely measure a player's movement.
- I have used Perspective Transformation to take the camera's distorted view point of the 3D world and accurately represent the scene's depth and perspective.
  This is useful in representing the movement of player in meters
- The distance and speed of a player is measured and represented in the video.

## Setup

1. Clone this repository.

2. Run the football_training_yolo_v5.ipynb file inside the training/ directory to produce the football-players-detection-1/ directory. I have already uploaded this folder in this project, so this step is not necessary. (Optional)

3. Run the Google_Colab_fine_tuning.ipynb file in Google Colab or in your pc(whichever has powerful gpu).
   Copy the best.pt and last.pt models into the models/ directory of this project.

4. For testing purposes, we can download the yolov8x model to check what's the output and how the best.pt model is just fine tuned for this particular task of football analysis. This can be done by running the yolo_inference.py file and changing the model inside it. (Optional)

5. Run the main.py file to produce the output video file in the output_videos/ directory.

## Results

### Input

https://github.com/MSVelan/Football-Analysis-Project/assets/92083282/321fbb9e-e9d7-428a-9476-12f8b28d437a

### Output

The actual output video(.avi file) is being converted to mp4 for preview purposes

https://github.com/MSVelan/Football-Analysis-Project/assets/92083282/c87b939f-307b-4fea-a480-aa4e21bf2997
