# 🛰️ Spacecraft Vision: Low-Light & Optical Turbulence AI Classifier

An interactive computer vision and deep learning prototype designed to classify orbital spacecraft silhouettes under severe physical degradations. 

This project simulates ground-based and space-based telescope observations—incorporating simulated optical contrast attenuation, atmospheric blur, and sensor read noise—to train and evaluate a lightweight **PyTorch Convolutional Neural Network (CNN)**.

## 🌌 Research Context & Motivation

In Space Situational Awareness (SSA) and orbital sustainability, identifying and tracking space objects is severely limited by:
1. **Photon-limited conditions:** Faint solar reflections against dark space backgrounds.
2. **Atmospheric turbulence:** Wavefront distortions that blur ground-based telescope observations.
3. **Sensor noise:** Background thermal and read noise on high-gain imaging sensors.

By bridging **computational mathematics** with **practical deep learning**, this project programmatically models these physical optical constraints to evaluate how neural networks generalize when resolving heavily degraded geometric silhouettes.

---

## 🛠️ Features

* **Programmatic Silhouette Generation:** OpenCV-powered generation of 2D spacecraft profiles (CubeSat, Hubble Space Telescope, and International Space Station) using clean geometric and vector math.
* **Physics-Based Optical Degradation Pipeline:** Real-time simulation of:
  * **Gaussian Blur:** To model atmospheric wavefront disturbance.
  * **Gaussian Noise:** To model sensor read noise.
  * **Optical Contrast Scale:** To model varying exposure rates and light attenuation.
* **Lightweight PyTorch CNN:** A custom, fast-converging CNN architecture optimized for edge or constrained hardware.
* **Interactive Streamlit Web Dashboard:** A live visual environment featuring real-time sliders for noise, blur, and contrast, displaying side-by-side visual comparisons and instant AI model classification confidence.

---

## 🏗️ Technical Stack

* **Language:** Python 3.10+
* **Deep Learning Framework:** PyTorch
* **Computer Vision & Math:** OpenCV (cv2), NumPy, Pillow
* **UI & Deployment:** Streamlit

---

## 📦 Project Structure

```text
├── dataset_generator.py   # Handles programmatic vector shapes and optical distortions
├── train_model.py         # Handles custom PyTorch Dataset, CNN architecture, and training
├── app.py                 # Interactive Streamlit dashboard UI
├── requirements.txt       # Dependencies for cloud deployment
└── README.md              # Project documentation
