TACO_ALERT
!! BEST.PT AND LAST.PT ADDED AS A RELEASE DUE TO FILE SIZE LIMITATIONS !!


YOLOv8-based waste detection and geolocation in natural environmentsSamsung Innovation Campus Capstone Project – Final Report (April–May 2025)

Introduction

Litter accumulation in natural and urban environments poses serious risks to ecosystems, public health and quality of life. TACO_ALERT applies deep learning–powered computer vision to automatically detect, classify and geolocate waste items in real time, contributing to more efficient cleanup efforts and raising environmental awareness.

Objectives

Apply deep-learning techniques (YOLOv8) to detect and classify litter in images.

Develop a real-time inference system accessible via any web-enabled camera.

Classify detected items according to the TACO dataset taxonomy (60 classes).

Integrate geolocation to generate actionable alerts for NGOs, institutions or citizens.

Provide an easy-to-use interface on both desktop and mobile devices.

Features

Real-time inference via a Flask back end and JavaScript front end.

Geolocation alerts: capture and transmit latitude/longitude with each detection.

Lightweight model: optimized YOLOv8-n for fast performance on GPU-equipped hosts.

Interactive notebooks:

prueba.ipynb – end-to-end demo of the inference pipeline

ploter.ipynb – visualization of training metrics (F1 curves, PR curves, confusion matrices)

Installation

Clone the repository

git clone https://github.com/jAImezs33/TACO_ALERT.git
cd TACO_ALERT

Create a virtual environment

python3.12 -m venv .venv
source .venv/bin/activate    # Windows: .venv\Scripts\activate

Install dependencies

pip install -r requirements.txt

Usage

Run inference

python run_inference.py --weights best.pt --data data.yaml --source path/to/images_or_video

Launch web interface

python app.py

Then open http://localhost:5000 in your browser, grant camera and location permissions, and start detecting.

Project Structure

TACO_ALERT/
├── best.pt               # Trained YOLOv8-n weights
├── last.pt               # Last checkpoint weights
├── data.yaml             # Class definitions and dataset config
├── prueba.ipynb          # Notebook demo for inference
├── ploter.ipynb          # Notebook for metrics visualization
├── run_inference.py      # CLI script for batch inference
├── app.py                # Flask application entry point
├── requirements.txt      # Python dependencies
├── proyecto.pdf          # Final project report
├── cover.png             # Cover image extracted from report
└── .gitignore

Performance Metrics

Metric

Value

Precision

29.8 %

Recall

16.4 %

mAP@0.5

13.5 %

mAP@0.5–0.95

10.5 %

F1 (max)

0.12

Confidence @ F1ₘₐₓ

0.37

Despite high confidence in top predictions, the overall recall and F1 indicate room for improvement.

Team

Jaime Zamorano Sanz – Dataset selection & validation, model training, UX/UI design, real-time alert generation, testing & support.

Ramón Balboa Gómez – Project coordination, environment setup, model development & training, web & Android development, deployment, documentation.

Nahuel Ignacio Argiró Angeleri – Technical documentation, material organization, research support and validation.

Contact

For questions or support:✉️ jaime.zamorano.sanz@gmail.com

License

No specific license (course project – all dependencies and data used are open source).
