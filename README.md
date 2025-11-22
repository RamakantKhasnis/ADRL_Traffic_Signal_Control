# 🚦 ADRL Traffic Signal Control  
### Adaptive Deep Reinforcement Learning for Smart Traffic Optimization

This project implements an **Adaptive Deep Reinforcement Learning (ADRL)**–based traffic signal controller using **D3QN (Double Deep Q-Network + Dueling + Prioritized Replay)** to optimize traffic flow at intersections.  
The system interacts with a simulation environment (SUMO or custom), observes traffic states, and learns an optimal traffic light policy to reduce congestion and waiting times.

---

## 🚀 Features

- **D3QN Agent** with:
  - Double Q-Learning  
  - Dueling Architecture  
  - Prioritized Experience Replay  
- **SUMO-based traffic simulation** (optional)  
- **Custom Python environment** for testing RL logic  
- Dynamic traffic phase switching  
- Logging and performance evaluation  
- Easily extendable for multi-intersection control  

---

## 📁 Project Structure

ADRL_Traffic_Signal_Control/
│
├── src/
│ ├── agent.py # RL agent (D3QN)
│ ├── networks.py # Neural network architectures
│ ├── replay.py # Prioritized replay buffer
│ ├── env_sim.py # Custom traffic simulation
│ ├── env_sumo.py # SUMO environment interface
│ ├── train.py # Training loop
│ ├── evaluate.py # Evaluation scripts
│ └── utils.py # Helper utilities
│
├── data/ # Optional traffic logs or configs
├── models/ # Saved trained models
├── runs/ # Training logs, plots
├── requirements.txt # Python dependencies
└── README.md # Documentation

yaml
Copy code

---

## 🧠 Algorithm Used — D3QN

The project uses a hybrid of improvements on the standard DQN:

✔ **Double DQN**  
✔ **Dueling Networks**  
✔ **Target Networks**  
✔ **Prioritized Experience Replay**  

These upgrades help the agent:

- Learn stable policies  
- Avoid overestimation  
- Converge faster  
- Handle large state spaces  

---

## 🧪 How Training Works

1. Environment provides traffic state:
   - Vehicle counts  
   - Waiting time  
   - Queue length  
2. Agent selects an action:
   - Switch phase  
   - Extend green  
   - Change to next cycle  
3. Model receives reward:
   - Minimize queue length  
   - Minimize delay  
4. Agent updates Q-values  
5. Over many episodes, the system learns to **optimize traffic flow**  

---

## 📦 Installation (Local)

```bash
git clone https://github.com/RamakantKhasnis/ADRL_Traffic_Signal_Control.git
cd ADRL_Traffic_Signal_Control
pip install -r requirements.txt
▶️ Usage
Train the model
bash
Copy code
python src/train.py
Evaluate trained model
bash
Copy code
python src/evaluate.py
📊 Results (Expected)
Reduced total waiting time

Reduced queue length

Faster intersection clearing

More stable traffic flow

Performance varies depending on the traffic pattern and SUMO configuration.

📝 Notes
SUMO installation is optional; custom Python env included.

This project is GPU-ready if using PyTorch.

All code is modular and extendable for multi-intersection traffic networks.

👨‍💻 Author
Ramakant Khasnis
Deep Learning | Reinforcement Learning | Computer Vision

