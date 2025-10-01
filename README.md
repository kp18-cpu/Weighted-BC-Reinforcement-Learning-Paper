# Weighted-BC-Reinforcement-Learning-Paper

# Density-Ratio Weighted Behavioral Cloning: Learning Control Policies from Corrupted Datasets

## Authors
- Shriram Karpoora Sundara Pandian (Rochester Institute of Technology, NY)
- Ali Baheri (Rochester Institute of Technology, NY)

## Overview

This paper introduces **Density-Ratio Weighted Behavioral Cloning (Weighted BC)**, a robust offline reinforcement learning approach for building control policies from datasets contaminated by adversarial attacks, system errors, or low-quality samples. Traditional Behavioral Cloning (BC) and offline RL algorithms commonly treat all data equally, leading to degraded performance when data includes corruptions.

Weighted BC leverages a small clean reference dataset to train a binary discriminator that identifies corrupted samples. These density ratios are then used as weights, prioritizing trusted trajectories and automatically down-weighting or removing suspicious data, all **without requiring prior knowledge of the contamination mechanism**.

<img width="758" height="642" alt="image" src="https://github.com/user-attachments/assets/a1a03cdc-4628-4dbc-88e8-26d7c08e194b" />


## Key Contributions

- **Robustness to Data Poisoning:** Weighted BC maintains near-optimal performance even at high levels of data corruption, outperforming classic BC, BCQ, and BRAC on continuous control environments.
- **Trajectory-Level Density Ratios:** Utilizes discriminator confidence scores to estimate trustworthiness at the trajectory level, ensuring cleaner policy learning.
- **Theoretical Guarantees:** Provides finite-sample bounds and convergence proofs under various contamination protocols.
- **Evaluation Protocol:** Benchmarks robust imitation learning across reward, state, transition, and action poisoning scenarios, using standard D4RL datasets.

## Experimental Highlights

- Weighted BC consistently outperforms baselines in environments contaminated by reward, state, action, and transition poisoning—even at 80-100% contamination.
- Demonstrates minimal computational overhead compared to other robust RL algorithms.
- Retains over 80% performance at moderate contamination rates and remains stable under extreme dataset noise.

## Applications

- Safer imitation learning for autonomous vehicles, robotics, and industrial control systems where trusted data is scarce and noisy.
- Defense against cyber-physical attacks and sensor failures in real-world control infrastructure.

## Citation

If you reference this work, please cite:

