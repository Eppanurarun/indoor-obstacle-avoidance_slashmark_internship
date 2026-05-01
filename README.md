# indoor-obstacle-avoidance_slashmark_internship
# 🚁 UAV Autonomous Navigation using CNN

## 📌 Project Overview  
This project implements an autonomous drone navigation system using a Convolutional Neural Network (CNN) and the AirSim simulator. The model processes real-time images from the drone and predicts movement actions to control its flight path.

## 🧠 Key Features  
- Real-time image capture from UAV using AirSim  
- CNN-based prediction for navigation decisions  
- Autonomous control using predicted actions  
- Image preprocessing and normalization  
- Modular design with controller and model separation  

## 📂 Project Structure  
├── CNNController.py     # Controls drone using CNN predictions  
├── CNNModel.py          # Loads and runs trained CNN model  
├── Controller.py        # Base drone controller with AirSim API  
├── models/  
│   ├── CNNModel.json    # Model architecture  
│   ├── CNNWeight.hdf5   # Trained weights  
├── ResNet_UAV.ipynb     # Training / experimentation notebook  

## ⚙️ Technologies Used  
- Python  
- Keras / TensorFlow  
- OpenCV  
- NumPy  
- AirSim (Microsoft Drone Simulator)  

## 🚀 How It Works  
1. The drone captures real-time RGB images.  
2. Images are resized and normalized.  
3. CNN model predicts the next action: Left, Straight, or Right.  
4. The controller converts predictions into velocity and angle.  
5. Drone moves autonomously based on decisions.  

## ▶️ Usage  

### 1. Install Dependencies  
pip install numpy opencv-python keras airsim  

### 2. Run AirSim Simulator  
Make sure AirSim is running before executing the script.  

### 3. Run the Controller  
python CNNController.py  

## 🎯 Action Mapping  
- 0 → Straight  
- 1 → Left  
- 2 → Right  

## 📊 Model Details  
- Input Shape: 72 x 128 x 3  
- Preprocessing: Resize and Normalization  
- Output: Action probabilities  

## 🛠️ Future Improvements  
- Add obstacle avoidance  
- Improve model accuracy with larger datasets  
- Integrate reinforcement learning  
- Deploy on real UAV hardware  

## 📌 Conclusion  
This project demonstrates how deep learning can be applied to real-time autonomous drone navigation using simulation environments like AirSim.
