# Synthetic Media Identification Using AI Using Deep Learning

## Project Overview

This project is a Synthetic Media Identification Using AI System built using Deep Learning
and Django that allows users to upload videos and detect whether they
are real or fake. The system uses trained models that analyze video
frames and provide prediction results through a web interface.

------------------------------------------------------------------------

## Project Directory Structure

Synthetic_Media_Identification_Using_AI │ ├── Django Application ├──
Model Creation └── Documentation

### Django Application

Contains the Django web app where users upload videos and get prediction
results.

### Model Creation

Contains scripts for preprocessing, training, and model building.

### Documentation

Contains reports, architecture diagrams, and project notes.

------------------------------------------------------------------------

## Model Results

  Model Name                              Videos   Frames   Accuracy
  --------------------------------------- -------- -------- ----------
  model_84_acc_10_frames_final_data.pt    6000     10       84.21%
  model_87_acc_20_frames_final_data.pt    6000     20       87.79%
  model_89_acc_40_frames_final_data.pt    6000     40       89.34%
  model_90_acc_60_frames_final_data.pt    6000     60       90.59%
  model_91_acc_80_frames_final_data.pt    6000     80       91.49%
  model_93_acc_100_frames_final_data.pt   6000     100      93.58%

------------------------------------------------------------------------

## System Requirements

-   Python \>= 3.6
-   Django \>= 3.0
-   CUDA \>= 10.0
-   NVIDIA GPU Required
-   GPU Compute Capability \> 3.0

------------------------------------------------------------------------

## Django Project Structure

ml_app → prediction logic (views.py)\
project_settings → settings and production configs\
static → CSS, JS, JSON files\
templates → HTML templates

Required folders to create before running: models/ uploaded_images/
uploaded_videos/

------------------------------------------------------------------------

## Run Using Docker

Run App Container: docker run --rm --gpus all -v
static_volume:/home/app/staticfiles/ -v
media_volume:/app/uploaded_videos/ --name=deepfakeapplication
abhijitjadhav1998/deefake-detection-20framemodel

Run Nginx Container: docker run -p 80:80 --volumes-from
deepfakeapplication -v static_volume:/home/app/staticfiles/ -v
media_volume:/app/uploaded_videos/
abhijitjadhav1998/deepfake-nginx-proxyserver

Open: http://localhost:80

------------------------------------------------------------------------

## Run Locally


Create Environment: python -m venv venv

Activate: Windows → venv`\Scripts`{=tex}`\activate  `{=tex} Linux/Mac →
source venv/bin/activate

Install Requirements: pip install -r requirements.txt

Run Server: python manage.py runserver

------------------------------------------------------------------------

## Features

-   Upload video detection
-   Deep learning prediction
-   Multiple trained models
-   Frame-based analysis
-   Web interface
-   Docker deployment

------------------------------------------------------------------------

## Workflow

1.  Upload video
2.  Extract frames
3.  Run model prediction
4.  Display result

------------------------------------------------------------------------

## Support

If you like this project, please star the repository.

