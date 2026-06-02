#  Tic-Tac-Toe Reinforcement Learning

A professional implementation of a Tic-Tac-Toe agent using **Temporal Difference (TD) Learning**. This project features a full game simulation environment and an interactive dashboard built specifically for Google Colab.

##  Project Overview
This project demonstrates how a Reinforcement Learning (RL) agent can learn optimal strategies through self-play. 
- **Algorithm**: Temporal Difference Learning (Value-based RL).
- **Architecture**: A `State` manager, a `Judger` for game rules, and a `Player` agent that updates its state-value estimations (`estimations`).
- **Convergence**: After 100,000 epochs of training, the agent achieves near-perfect play, where games between two optimal agents consistently result in a tie.

## Dashboard Preview
<img width="1548" height="757" alt="Screenshot 2026-06-03 003428" src="https://github.com/user-attachments/assets/eb89f49b-fb99-4a5a-b620-8413f8260992" />

##  Features
- **Interactive Dashboard**: A custom HTML/JS/CSS dashboard rendered directly in Colab.
- **Real-time KPI Tracking**: Monitor training epochs, win rates, and total states explored (5,478 unique states).
- **Visual Convergence**: Chart.js integration to visualize how win rates stabilize over time.
- **Human-vs-AI Mode**: Play against the trained model using a responsive 3x3 grid.

##  Getting Started

### Requirements
- Python 3.10+
- `numpy`
- `pickle` (for saving/loading policies)

### Running in Google Colab
1. Open the `.ipynb` notebook in Google Colab.
2. Run the main code cell to generate all possible states and train the model.
3. Execute the **Dashboard** cell to interact with the model visually.

##  How it Works
The agent uses the following formula to update its belief about the value of a state $s$:

$$V(s) \leftarrow V(s) + \alpha [V(s') - V(s)]$$

Where:
- $V(s)$ is the estimation of the current state.
- $\alpha$ is the learning rate (step size).
- $V(s')$ is the estimation of the next state.

## 📁 Repository Structure
- `TD_Learning_TicTacToe.ipynb`: The primary notebook containing logic and UI.
- `Dashboard.ipynb`: To visualize the game play.

--- 
