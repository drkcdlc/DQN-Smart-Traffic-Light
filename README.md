## 🚦 Smart Traffic Light Control with Deep Q-Network (DQN)

This project analyzes Google Maps screenshots of traffic junctions and trains a Deep Q-Network (DQN)-based model to optimize traffic light control.  
It uses the publicly available dataset [**kavsakdata**](https://www.kaggle.com/datasets/kutayertrk/kavsakdata/versions/3), which contains real intersection images and annotations.

---

### 📁 Project Structure

| File | Description |
|------|--------------|
| `junction-analyzer.ipynb` | Analyzes and preprocesses a single intersection image using computer vision techniques. |
| `multiple-junction-analyzer.ipynb` | Handles multiple intersections simultaneously, performing batch analysis and feature extraction. |
| `one-junction.ipynb` | Simulates traffic flow and signal control for a single junction. |
| `multiple-junctions.ipynb` | Implements DQN-based reinforcement learning to manage multiple connected intersections. |

---

### 🧠 Methodology

1. **Data Collection**
   - Intersection images were obtained from Google Maps and labeled using the [kavsakdata](https://www.kaggle.com/datasets/kutayertrk/kavsakdata) dataset.
   - Each intersection contains traffic light positions, vehicle density, and directional flow.

2. **Preprocessing**
   - Image segmentation and region-of-interest (ROI) extraction.
   - Object detection (vehicles, traffic lanes, lights) using OpenCV and custom filters.

3. **Simulation Environment**
   - Synthetic traffic flow is modeled based on extracted features.
   - State representation includes queue lengths, signal states, and arrival rates.

4. **Reinforcement Learning (DQN)**
   - The agent observes the current traffic state and decides the next signal phase.
   - Reward function penalizes waiting time and congestion, while rewarding throughput improvement.
   - Trained with experience replay and target network updates.

---

### ⚙️ Technologies Used

- **Python 3.10+**
- **TensorFlow / PyTorch**
- **OpenCV**
- **NumPy / Pandas**
- **Matplotlib / Seaborn**
- **Gym-like custom environment for traffic simulation**

---

### 📊 Results

- The DQN model successfully learned adaptive signal control policies.  
- Compared to fixed-time scheduling, average vehicle waiting time decreased by **up to 35%** in simulation.  
- Multi-junction coordination improved overall throughput in dense traffic scenarios.

---

### 🧩 Future Work

- Integration with **SUMO** or **CARLA** simulators for realistic traffic behavior.
- Real-time image input from live cameras.
- Transfer learning for different city layouts.

---

### 🔗 Dataset Reference

> **Kaggle Dataset:** [kavsakdata](https://www.kaggle.com/datasets/kutayertrk/kavsakdata/versions/3)  
> Kutay Ertürk, 2024 — Contains labeled Google Maps intersection screenshots.

---

### 👨‍💻 Authors

- **Kutay Ertürk**, **Furkan Altınışık**, **Yusuf Karakaya**

---

### 📜 License

This project is released under the MIT License.  
Feel free to use, modify, and distribute with attribution.
