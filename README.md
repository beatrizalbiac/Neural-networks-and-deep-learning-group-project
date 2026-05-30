# AI-Powered Volleyball Analysis System 
It's an AI-powered sports analysis system that integrates five neural network architectures into a single end-to-end application for volleyball match analysis. Built entirely in Google Colab.

## What it does:
1. Detects players and the ball in real time using YOLO11n
2. Classifies each detected player into Team 1 or Team 2 using an MLP
3. Predicts player movement trajectories using an LSTM and overlays them as arrows on the video
4. Generates position heatmaps and a court presence indicator for each team
4. Answers natural language questions about any match frame using Gemma 4

## How to run it step by step:
The project runs entirely en Google Colab and it's advised against to use any other IDE such as Visual Studio Code as for the user to not have to manually label the images the files get automatically uploaded when their corresponding cell is ran. For this it's recommended to not use an important email, as you'll need to give Google Colab permissions to your Google Drive.

**To run:**

Follow the order of the cells and go one by one running them. 

**DON'T** use *"run all"* as the cells for the manual labeling of the teams won't let you keep going until you label the images (you can just stop the cell and skip them).<br>
<br>
<br>Each cell will have a specification on where and/or how to run in inside the own code win a comment at the very top, just below what's actually in that cell.

1. Install dependencies and download the dataset
2. Install and load Gemma 4
3. Download pretrained models
4. Load the MLP and LSTM
5. Launch the interface

## To use the interface:

Video Detection tab → upload a volleyball video, adjust the confidence threshold with the slider, and click Run Detection. The output video will show bounding boxes with team labels, trajectory arrows, a position heatmap and a court presence bar.
Training tab → retrain the YOLO detector from scratch with custom epochs, learning rate and batch size. Results are shown in the log.
VLM Assistant tab → upload a frame from a match, type a question and click Ask. The model will answer based on what it can see in the image.

## Dataset
VolleyBallYolo v1 → https://universe.roboflow.com/volleyballyolo/volleyballyolo/dataset/1

## Requeriments
None, everything runs on Google Colab. Although the T4 GPU session is recommended and encouraged.
