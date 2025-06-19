# NovaSight
# NovaSight: Intelligent Object Detection for Space Stations

NovaSight is an intelligent object detection system designed to identify and track critical tools inside a space station — including toolboxes, oxygen tanks, and fire extinguishers — using only synthetic data from Duality AI’s Falcon platform. Going beyond basic detection, NovaSight introduces context-aware prioritization, where detection focus shifts based on environmental conditions like oxygen levels or temperature. The system features a self-improving feedback loop that identifies weak performance areas (e.g., occlusion, lighting issues) and uses Falcon to generate improved synthetic data for retraining. As a bonus, we propose a lightweight AR-based mobile companion app to assist astronauts in real-time tool identification, even in emergencies or low visibility. NovaSight is scalable, adaptive, and built with real deployment in mind. It showcases how synthetic data, combined with smart design, can build robust AI solutions for safety-critical environments like space stations.

---

## Table of Contents

- [Features](#features)
- [Step-by-Step Instructions](#step-by-step-instructions)
- [Reproducing Final Results](#reproducing-final-results)
- [Environment and Dependencies](#environment-and-dependencies)
- [Expected Outputs and Interpretation](#expected-outputs-and-interpretation)
- [Additional Notes](#additional-notes)

---

## Features

- **Robust object detection** for toolboxes, oxygen tanks, and fire extinguishers
- **Context-aware prioritization**: Focuses detection based on environmental data (e.g., low oxygen, high temperature)
- **Self-improving feedback loop**: Identifies weak spots and retrains using new synthetic data from Falcon
- **AR-based mobile companion app** for real-time tool identification and emergency assistance
- **Scalable and adaptive** for real-world deployment in space environments

---

## Step-by-Step Instructions

1. **Clone the Repository**
https://github.com/harshithaps11/NovaSight.git


2. **Set Up the Environment**
- (Recommended) Create and activate a virtual environment:
  ```
  python3 -m venv venv
  source venv/bin/activate
  ```
- Install dependencies:
  ```
  pip install -r requirements.txt
  ```

3. **Prepare the Dataset**
- Place the Falcon-generated synthetic dataset in the `data/` directory. Organize as:
  ```
  data/
    images/
    labels/
  ```

4. **Train the Model**
python train.py --data data/dataset.yaml --epochs 100 --img 640 --batch 16 --weights yolov8n.pt

5. **Test/Evaluate the Model**


6. **Run Inference**


7. **Engage Feedback Loop for Self-Improvement**


8. **Launch AR Companion App (Optional)**
- Follow instructions in `ar_app/README.md` to deploy the mobile AR app for real-time tool identification.

---

## Reproducing Final Results

- Use the provided training and evaluation scripts with the same hyperparameters and data splits as in `config.yaml` and `data/dataset.yaml`.
- The final, best-performing model weights are in `runs/train/exp/weights/best.pt`.
- For context-aware evaluation, use:



