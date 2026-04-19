# 🤖 17-DOF Humanoid Robot – STM32 Embedded Control

A fully custom-built 17-degree-of-freedom (DOF) humanoid robot designed and developed using an STM32 microcontroller. This project demonstrates real-time embedded control, coordinated multi-servo actuation, and system-level debugging for stable humanoid motion.

---

## 📌 Project Overview

This project focuses on building a **humanoid robotic platform** capable of coordinated limb movement using 17 servo motors. The system is controlled by an STM32 microcontroller, where embedded C firmware handles:

- Real-time joint control
- Motion sequencing
- Synchronization of multiple actuators
- Stable posture and locomotion logic

The robot structure includes legs, arms, and upper body joints, enabling complex motion patterns.

---

## 🎯 Key Features

- 17 DOF articulated humanoid structure
- Real-time PWM-based servo control using STM32 timers
- Coordinated multi-joint motion
- Modular joint control architecture
- Embedded C firmware with low-level hardware control
- Debugging using SWD interface and STM32CubeIDE

---

## 🖼️ Project Demo

### Humanoid Structure & Joint Layout
![Robot Front View](./images/front_view.jpg)

### Side View & Leg Mechanism
![Robot Side View](./images/side_view.jpg)

### Upper Body Assembly
![Upper Body](./images/top_view.jpg)

### Full System with Controller
![Full System](./images/full_setup.jpg)

> 📹 **Demo Videos**
- Add your walking / motion videos here:

https://drive.google.com/drive/folders/1fGD9OJGQfUPJuz-Li884oJtyvLW7TFRm?usp=sharing
---

## 🧠 System Architecture
    +----------------------+
    |     STM32 MCU        |
    |  (Main Controller)   |
    +----------+-----------+
               |
    PWM Signals (Timers)
               |
    +----------v-----------+
    |   Servo Motor Array  |
    |   (17 DOF Control)   |
    +----------+-----------+
               |
        Mechanical Joints
               |
        Humanoid Movement


---

## 🔩 Hardware Components

- STM32 Microcontroller (e.g., STM32F103 / STM32F4 series)
- 17x Servo Motors (High torque for legs)
- Servo Driver / PWM Interface
- Power Supply (External for motors)
- Mechanical brackets & joints
- Connecting wires and PCB / breadboard

---

## 💻 Tech Stack

- **Embedded C**
- **STM32CubeIDE**
- **STM32 HAL Drivers**
- PWM using **hardware timers**
- SWD Debugging

---

## ⚙️ How It Works

1. **PWM Generation**
   - STM32 timers generate PWM signals for each servo motor.
   - Pulse width determines joint angle.

2. **Joint Mapping**
   - Each servo is assigned a joint ID (1–17).
   - Logical mapping ensures coordinated movement.

3. **Motion Sequencing**
   - Predefined sequences control walking / posture.
   - Smooth transitions implemented using incremental angle updates.

4. **Synchronization**
   - Multiple joints move together using timing control loops.
   - Ensures balance and natural motion.

---

## 🔌 Setup & Wiring

1. Connect all servo motors to PWM output pins of STM32
2. Use external power supply for motors (important ⚠️)
3. Common ground between STM32 and motor supply
4. Flash firmware using STM32CubeIDE
5. Power system and observe motion sequences

---

## 🚧 Challenges & Solutions

### 1. Servo Synchronization
**Problem:** Jitter and uncoordinated movement  
**Solution:** Implemented timed motion sequences and gradual angle transitions

### 2. Power Instability
**Problem:** Voltage drops due to multiple servos  
**Solution:** Used external regulated power supply for motors

### 3. Balance & Stability
**Problem:** Robot tipping during motion  
**Solution:** Tuned joint angles and introduced stable posture sequences

### 4. Timing Issues
**Problem:** Inconsistent PWM signals  
**Solution:** Used hardware timers instead of software delays

---

## 📈 Results

- Achieved synchronized multi-joint movement
- Stable standing posture
- Successful execution of motion sequences
- Modular and scalable architecture for future improvements

---

## 🚀 Future Improvements

- Add IMU sensor for balance (closed-loop control)
- Implement inverse kinematics
- Integrate ROS for higher-level control
- Add vision system for environment interaction

---

## 👨‍💻 Author

**Raj Kumar Jha**  
Embedded Systems & Robotics Engineer  

- GitHub: https://github.com/yourusername  
- LinkedIn: https://linkedin.com/in/yourprofile  

---

## ⭐ If you like this project

Give it a star ⭐ and feel free to connect!