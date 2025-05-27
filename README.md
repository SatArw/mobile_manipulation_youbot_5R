# Mobile Manipulation Capstone

This project is my implementation of the [Mobile Manipulation Capstone](https://hades.mech.northwestern.edu/index.php/Mobile_Manipulation_Capstone) from the Modern Robotics course by Northwestern University. The task involves commanding a mobile manipulator to pick up a cube from an initial location and place it at a final location using coordinated motion across its base, arm, and gripper.

## 🎥 Simulation

👉 **[Watch Simulation Video](#)**  
*(Add your YouTube or Drive link here)*

## 🛠 Simulation Tool

Optionally, the task can be visualized and tested in [CoppeliaSim](https://www.coppeliarobotics.com/), a versatile robotics simulator for modeling, control, and physics-based validation.

## 🧠 Concepts Used

### 🔄 Trajectory Generation
- SE(3) trajectories generated using time-parametrized cubic or quintic polynomial interpolation.
- Cube and end-effector trajectories are defined in multiple phases (approach, grasp, standoff, etc.) and stored as a sequence of desired poses and gripper states.

### 🤖 Kinematics
- **Forward Kinematics**: Computes the end-effector pose using the Product of Exponentials (PoE) formula for the robotic arm.
- **Inverse Kinematics**: Approximated through trajectory tracking; base and arm motions are computed separately and combined in task space.

### 🧩 Controller
- **Feedback Control Law**:  
  \( V = X_{err}^* K_p + \dot{X}_{err}^* K_d + V_{desired} \)  
  where:
  - \( X_{err} \) is the twist error between desired and actual end-effector pose.
  - \( K_p \), \( K_d \) are gain matrices.
  - \( V \) is the commanded twist in the end-effector frame.
- The computed twist is mapped to base and joint velocities using the body Jacobian and mobile base kinematics.

### ✋ Gripper Control
- Gripper state is managed via a simple state machine.
- Open/close actions are triggered at appropriate points in the trajectory.

## 📄 License

This project is released under the [MIT License](LICENSE). You are free to use, modify, and share it — just give proper credit.

---

© [Your Name], 2025
