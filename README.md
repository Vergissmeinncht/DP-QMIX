# DP-QMIX 🧠🤖

Welcome to the **DP-QMIX** repository! This project provides an implementation of a Multi-Agent Reinforcement Learning (MARL) algorithm based on QMIX. 

Building upon the classic QMIX architecture, this project introduces an **adaptive death mechanism** to address the **dynamic state space problem** in multi-agent cooperative environments. It achieves excellent performance in environments such as the StarCraft Multi-Agent Challenge (SMAC).

## 🛠️ Tech Stack & Dependencies

This project is primarily written in Python, with some Shell scripts for automated training and evaluation. Main dependencies include:
* Python 3.7+
* PyTorch (1.8+ recommended)
* NumPy
* Gym / SMAC (depending on your specific test environments)

## 📁 Repository Structure

* `src/` or `agents/`: Core network architectures and agent logic for the DP-QMIX algorithm.
* `envs/`: RL environment configurations and wrappers.
* `scripts/`: `.sh` scripts for launching training or evaluation experiments.
* `utils/`: Utility functions, logging, and data processing code.

*(Note: Feel free to adjust the directory names above if your actual structure differs slightly)*

## 🚀 Quick Start

### 1. Installation

First, clone this repository to your local machine:
```bash
git clone https://github.com/Vergissmeinncht/DP-QMIX.git
cd DP-QMIX
```

It is highly recommended to use `conda` to create a virtual environment and install the dependencies:
```bash
conda create -n dp-qmix python=3.8
conda activate dp-qmix
pip install -r requirements.txt
```

### 2. Training

We provide convenient shell scripts to run experiments. You can modify the parameters inside the script to adjust hyperparameters or switch environments:

```bash
# Grant execution permission
chmod +x train.sh

# Start training
bash train.sh
```

Alternatively, you can run the python command directly:
```bash
python main.py --env-config=sc2 --config=qmix --map=3m
```
*(Note: Please replace the command above with your actual execution commands and parameters if they are different)*

### 3. Evaluation

After training is complete, you can load the saved model weights for testing or video rendering:
```bash
python main.py --evaluate --load-dir ./results/models/...
```

## 📚 References

This project is built upon or inspired by the following excellent open-source repositories:
* [pymarl2](https://github.com/hijkzzz/pymarl2)
* [unmas](https://github.com/James0618/unmas)

## 🤝 Contributing

We welcome anyone interested in Multi-Agent Reinforcement Learning (MARL) to discuss issues or submit Pull Requests to improve the code! If you find this project helpful for your research or learning, please consider giving it a Star ⭐!
