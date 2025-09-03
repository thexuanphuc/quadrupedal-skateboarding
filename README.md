# Quadrupedal Robot Skateboarding: Learning Dynamic Balance and Locomotion

## Overview

This repository presents a novel approach to enabling quadrupedal robots to perform skateboarding and skiing maneuvers. Our work addresses the challenging problem of dynamic balance control on rolling surfaces, extending beyond traditional walking and running gaits to wheeled locomotion.

## Abstract

Quadrupedal robots excel at terrestrial locomotion, but dynamic balance on rolling platforms like skateboards remains largely unexplored. We introduce a framework combining reinforcement learning and hierarchical control to enable mounting, balancing, steering, and dismounting behaviors. The control objectives are multi-objective: maximize stability, forward progress, energy efficiency, and smoothness. Our solution leverages a hierarchical architecture trained end-to-end, with real-world validation on physical hardware.

## Key Contributions

- **Dynamic Balance Control**: Novel algorithms for stability on moving skateboard platforms using ZMP and CoP feedback.
- **Multi-Modal Locomotion**: Seamless transition between walking and skateboarding modes.
- **Reinforcement Learning Framework**: End-to-end learning for complex maneuvers using domain randomization and curriculum learning.
- **Real-World Validation**: Successful deployment on physical quadrupedal robot hardware with high sim-to-real performance retention.
- **Theoretical Analysis**: Stability analysis of the coupled robot-skateboard system.

## Technical Approach

We use a hierarchical control system combining high-level planning, whole-body control, and joint-level stabilization. The learning framework is built on MuJoCo simulation, with curriculum learning and domain randomization for robustness. Proximal Policy Optimization (PPO) trains policies for mounting, balancing, steering, and speed control. The observation space includes proprioceptive and exteroceptive sensors, and the action space is continuous joint torques.

## Demonstrations

### Basic Skateboarding
![Front View](src/demo/matplotlib_front.gif)
*Front view demonstration of basic skateboarding locomotion*

![Isometric View](src/demo/matplotlib_iso.gif)
*Isometric view showing full body dynamics during skateboarding*

### Advanced Maneuvers
![Mounting](src/demo/mounting.gif)
*Autonomous mounting behavior from standing position*

![Turning](src/demo/turning.gif)
*Dynamic turning maneuvers with balance control*

### Real Robot Performance
![Real Front View](src/demo/real_front.gif)
*Real robot performance - front view*

![Real Isometric View](src/demo/real_iso.gif)
*Real robot performance - isometric view*

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
- Pavel Osinenko - p.osinenko@skoltech.ru

## Contact

For questions or collaborations, please contact:
- **Danil Belov**: danil.belov@skoltech.ru
- **AIDA Research Group**: Artificial Intelligence in Dynamic Action, Skoltech, Russia
