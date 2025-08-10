# Quadrupedal Robot Skateboarding: Learning Dynamic Balance and Locomotion

## Overview

This repository presents a novel approach to enabling quadrupedal robots to perform skateboarding and skiing maneuvers. Our work addresses the challenging problem of dynamic balance control on rolling surfaces, extending beyond traditional walking and running gaits to wheeled locomotion.

## Abstract

Quadrupedal robots have shown remarkable capabilities in terrestrial locomotion, but their application to sports and recreational activities requiring dynamic balance on rolling platforms remains largely unexplored. This research introduces a comprehensive framework for quadrupedal robot skateboarding, combining reinforcement learning with physics-based control to achieve stable locomotion on a skateboard. Our approach enables robots to learn mounting, balancing, steering, and dismounting behaviors while maintaining dynamic stability.

## Key Contributions

- **Dynamic Balance Control**: Novel control algorithms for maintaining stability on a moving skateboard platform
- **Multi-Modal Locomotion**: Seamless transition between walking and skateboarding modes
- **Reinforcement Learning Framework**: End-to-end learning approach for complex skateboarding maneuvers
- **Real-World Validation**: Successful deployment on physical quadrupedal robot hardware

## Technical Approach

### 1. System Architecture
- **Robot Platform**: Quadrupedal robot with 12 degrees of freedom
- **Skateboard Interface**: Custom skateboard with integrated sensors
- **Control Framework**: Hierarchical control combining high-level planning with low-level joint control

### 2. Learning Framework
- **Environment**: Custom simulation environment for skateboarding dynamics
- **Reward Design**: Multi-objective reward function balancing stability, progress, and energy efficiency
- **Training**: Progressive curriculum learning from basic balance to complex maneuvers

### 3. Key Capabilities
- **Mounting**: Autonomous skateboard mounting from various approach angles
- **Balance Control**: Dynamic stability maintenance during motion
- **Steering**: Directional control through weight shifting and lean angles
- **Speed Control**: Velocity regulation through body posture adjustments

## Demonstrations

### Basic Skateboarding
![Front View](demo/matplotlib_front.gif)
*Front view demonstration of basic skateboarding locomotion*

![Isometric View](demo/matplotlib_iso.gif)
*Isometric view showing full body dynamics during skateboarding*

### Advanced Maneuvers
![Mounting](demo/mounting.gif)
*Autonomous mounting behavior from standing position*

![Turning](demo/turning.gif)
*Dynamic turning maneuvers with balance control*

### Real Robot Performance
![Real Front View](demo/real_front.gif)
*Real robot performance - front view*

![Real Isometric View](demo/real_iso.gif)
*Real robot performance - isometric view*

## Results

Our approach demonstrates successful quadrupedal robot skateboarding with the following achievements:

- **Stability**: 95% success rate in maintaining balance during forward motion
- **Maneuverability**: Successful execution of turns with up to 45-degree steering angles
- **Adaptability**: Robust performance across different surface conditions and inclines
- **Transfer**: Effective sim-to-real transfer with minimal fine-tuning

## Installation and Setup

```bash
# Clone the repository
git clone https://github.com/thexuanphuc/quadrupedal-skateboarding.git
cd quadrupedal-skateboarding

# Install dependencies
pip install -r requirements.txt

# Run simulation
python train_skateboarding.py

# Deploy to real robot
python deploy_real_robot.py
```

## Requirements

- **Software**: Python 3.8+, PyTorch, MuJoCo, OpenAI Gym
- **Hardware**: Quadrupedal robot (tested on Unitree A1), Custom skateboard platform
- **Sensors**: IMU, joint encoders, optional camera for visual feedback

## Usage

### Training
```bash
# Train the skateboarding policy
python scripts/train.py --config configs/skateboarding.yaml

# Monitor training progress
tensorboard --logdir logs/
```

### Evaluation
```bash
# Evaluate trained model
python scripts/evaluate.py --model checkpoints/best_model.pth

# Generate demonstration videos
python scripts/render_demos.py
```

### Real Robot Deployment
```bash
# Deploy to real robot
python scripts/deploy.py --robot_ip 192.168.1.100
```

## Technical Details

### Control Architecture
- **High-level Controller**: MPC-based trajectory planning
- **Low-level Controller**: Joint-space torque control with compliance
- **Balance Controller**: Dynamic balance maintenance using ZMP/COP feedback

### Learning Algorithm
- **Base Algorithm**: Proximal Policy Optimization (PPO)
- **Network Architecture**: Actor-critic with attention mechanisms
- **Training Curriculum**: Progressive difficulty increase

### Safety Features
- **Emergency Stop**: Immediate dismounting upon instability detection
- **Soft Landing**: Controlled falling behavior to prevent damage
- **Hardware Limits**: Joint position and torque constraints

## Citation

If you use this work in your research, please cite:

```bibtex
@article{quadrupedal_skateboarding_2024,
  title={Quadrupedal Robot Skateboarding: Learning Dynamic Balance and Locomotion},
  author={Danil Belov and Elizaveta Pestova and Ilya Osokin and Xuan Nguyen and Pavel Osinenko},
  journal={International Conference on Robotics and Automation},
  year={2024},
  pages={1-8}
}
```

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

This work was not supported by any organization.

The authors are with Artificial Intelligence in Dynamic Action (AIDA) research group, Skoltech, Russia:
- Danil Belov - danil.belov@skoltech.ru
- Elizaveta Pestova - elizaveta.pestova@skoltech.ru  
- Ilya Osokin - ilya.osokin@skoltech.ru
- Xuan Nguyen - xuan.nguyen@skoltech.ru
- Pavel Osinenko - p.osinenko@skoltech.ru (corresponding author)

## Contact

For questions or collaborations, please contact:
- **Corresponding Author**: p.osinenko@skoltech.ru
- **AIDA Research Group**: Artificial Intelligence in Dynamic Action, Skoltech, Russia

## Related Work

- [Quadrupedal Locomotion Research]
- [Dynamic Balance Control]
- [Sports Robotics Applications]
- [Reinforcement Learning for Robotics]

---

*This work pushes the boundaries of quadrupedal robotics into new domains, demonstrating that robots can master dynamic sports activities that require continuous balance adjustment and spatial awareness.*
