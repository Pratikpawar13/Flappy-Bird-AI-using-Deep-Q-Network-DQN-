# 🐦 Flappy Bird AI using Deep Q-Network (DQN)

> A Deep Reinforcement Learning project that trains an autonomous AI agent to play Flappy Bird using a Deep Q-Network (DQN) implemented from scratch in PyTorch.

![Python](https://img.shields.io/badge/Python-3.10+-blue.svg)
![PyTorch](https://img.shields.io/badge/PyTorch-Deep%20Learning-red)
![Gymnasium](https://img.shields.io/badge/Gymnasium-RL-green)
![License](https://img.shields.io/badge/License-MIT-yellow)

---

## 📌 Overview

This project implements a **Deep Q-Network (DQN)** agent that learns to play **Flappy Bird** through trial and error using Reinforcement Learning.

The agent interacts with the Gymnasium Flappy Bird environment, stores experiences in a replay buffer, and updates its neural network using mini-batch gradient descent. A separate target network is maintained to improve training stability.

The project is implemented entirely in **PyTorch** without using high-level reinforcement learning libraries.

---

## ✨ Features

- Deep Q-Network (DQN) implementation from scratch
- Experience Replay Buffer
- Target Network Synchronization
- Epsilon-Greedy Exploration Strategy
- GPU (CUDA/MPS) Support
- Hyperparameter Configuration using YAML
- Model Checkpoint Saving
- Command Line Training & Testing
- Flappy Bird Gymnasium Environment
- PyTorch-based Neural Network

---

## 🏗️ Project Structure

```
.
├── agent.py                # Training & inference pipeline
├── dqn.py                  # Deep Q-Network model
├── experience_replay.py    # Replay memory implementation
├── game_flappy_bird.py     # Manual Flappy Bird gameplay
├── parameters.yaml         # Hyperparameters
└── README.md
```

---

## 🧠 Reinforcement Learning Workflow

```
Environment
      │
      ▼
 Current State
      │
      ▼
 Deep Q-Network
      │
      ▼
 Select Action
(Epsilon-Greedy)
      │
      ▼
Take Action in Environment
      │
      ▼
Receive Reward + Next State
      │
      ▼
Store Experience
      │
      ▼
Replay Memory
      │
      ▼
Sample Mini-Batch
      │
      ▼
Compute Target Q-Values
      │
      ▼
Backpropagation
      │
      ▼
Update Policy Network
      │
      ▼
Synchronize Target Network
```

---

## 🧩 Tech Stack

- Python
- PyTorch
- Gymnasium
- Flappy Bird Gymnasium
- NumPy
- PyYAML

---

## ⚙️ Deep Q-Network Architecture

The agent uses a simple fully connected neural network.

```
Input Layer
      │
      ▼
Linear Layer
      │
      ▼
ReLU
      │
      ▼
Output Layer
(Q-values for each action)
```

---

## ⚙️ Hyperparameters

The hyperparameters are stored inside **parameters.yaml**.

| Parameter | Value |
|------------|-------|
| Learning Rate | 0.001 |
| Gamma | 0.99 |
| Initial Epsilon | 1.0 |
| Minimum Epsilon | 0.05 |
| Epsilon Decay | 0.9995 |
| Replay Memory | 100000 |
| Batch Size | 32 |
| Target Sync Rate | 10 |

---

## 🚀 Installation

### Clone Repository

```bash
git clone https://github.com/yourusername/flappy-bird-dqn.git

cd flappy-bird-dqn
```

### Create Virtual Environment

```bash
python -m venv venv
```

Windows

```bash
venv\Scripts\activate
```

Linux / Mac

```bash
source venv/bin/activate
```

### Install Dependencies

```bash
pip install -r requirements.txt
```

---

## ▶️ Train the Agent

```bash
python agent.py flappybirdv0 --train
```

During training the agent will

- Explore the environment
- Store experiences
- Sample replay memory
- Optimize the DQN
- Save the best model

---

## 🎮 Run Trained Agent

```bash
python agent.py flappybirdv0
```

This loads the saved model and lets the trained AI play Flappy Bird.

---

## 🎯 Manual Gameplay

```bash
python game_flappy_bird.py
```

Press **Spacebar** to flap.

---

## 🧠 DQN Algorithm

The training process follows the standard Deep Q-Network algorithm:

1. Observe current state
2. Choose action using epsilon-greedy policy
3. Execute action
4. Store transition in replay memory
5. Sample a random mini-batch
6. Compute target Q-values using target network
7. Minimize Mean Squared Error loss
8. Periodically synchronize target network

---

## 📈 Future Improvements

Planned enhancements include:

- Double DQN
- Dueling DQN
- Prioritized Experience Replay
- TensorBoard Integration
- Training Visualizations
- Reward Curve Plotting
- ONNX Export
- Streamlit Dashboard
- FastAPI Deployment
- Model Benchmarking

---

## 📚 Concepts Used

- Reinforcement Learning
- Markov Decision Process (MDP)
- Deep Q-Learning
- Bellman Equation
- Neural Networks
- Experience Replay
- Target Networks
- Exploration vs Exploitation
- Epsilon Decay
- PyTorch

---

## 👨‍💻 Author

**Pratik Pawar**

---