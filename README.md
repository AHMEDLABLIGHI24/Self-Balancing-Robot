# 🤖 Self-Balancing Robot

A two-wheeled mobile robot that uses sensor feedback and control theory to maintain balance autonomously. This project demonstrates core principles of robotics, mechatronics, and real-time control systems. It is an excellent educational platform for learning about PID control, sensor fusion, and embedded programming.

![Self-Balancing Robot](sbf%20en%20(1).PNG)

---

## 📁 Project Structure

```
Self-Balancing-Robot/
├── Firmware/           # Arduino/ESP32 code
│   ├── Self_Balancing_Robot.ino
│   ├── PID.cpp
│   ├── MPU6050_Handler.cpp
│   └── Motor_Control.cpp
├── Hardware/           # Electronics and mechanical design
│   ├── Schematics/     # Circuit diagrams
│   ├── PCB/            # PCB design (if applicable)
│   ├── STL/            # 3D-printable parts
│   └── Datasheets/     # Component datasheets
├── Documentation/      # Project reports, tutorials, references
├── Images/             # Photos and diagrams
└── README.md
```

---

## ✨ Features

- 🤸 **Self-balancing** using MPU6050 (accelerometer + gyroscope)
- 🎮 **Optional wireless control** via Bluetooth (HC-05) or Wi-Fi (ESP32)
- ⚡ **Efficient motor control** with PWM and encoder feedback
- 🔧 **Modular and expandable** design for additional sensors or features
- 📊 **Real-time tuning** via Serial Monitor or Bluetooth

---

## 🛠️ Components Used

| Component | Quantity | Description |
|-----------|----------|-------------|
| Arduino Uno / ESP32 | 1 | Main microcontroller |
| MPU6050 | 1 | IMU (tilt and angular velocity) |
| DC Motors with Encoders | 2 | For movement and balance |
| Motor Driver (L298N / BTS7960) | 1 | Motor control |
| Li-ion Battery Pack | 1 | Power supply |
| HC-05 Bluetooth Module (optional) | 1 | Wireless control |
| 3D-Printed Chassis | 1 | Custom frame |

---

## 🧠 Working Principle

1. The **MPU6050** measures the robot’s tilt angle and angular velocity.
2. The **microcontroller** fuses sensor data and runs a **PID control algorithm**.
3. The **PID output** is sent to the **motor driver** to adjust motor speed and direction.
4. The **motors respond** to correct the robot’s posture in real time.
5. The process repeats in a **closed-loop feedback** system.

---

## 🚀 Getting Started

### 1. Hardware Assembly
- Print the chassis from `Hardware/STL/`
- Mount motors, wheels, and electronics
- Wire components as per `Hardware/Schematics/`

### 2. Upload the Code
- Open `Firmware/Self_Balancing_Robot.ino` in Arduino IDE
- Install required libraries:
  - `MPU6050` by Electronic Cats
  - `PID` by Brett Beauregard
- Upload to Arduino/ESP32

### 3. Calibration and Tuning
- Power on the robot and place it upright
- Open Serial Monitor (`Ctrl+Shift+M`)
- Adjust PID values using serial commands:
  - `Kp [value]`
  - `Ki [value]`
  - `Kd [value]`
- Tune until the robot stabilizes

### 4. Optional: Bluetooth Control
- Pair HC-05 with your phone
- Use a Bluetooth terminal app to send commands:
  - `F` = Forward
  - `B` = Backward
  - `L` = Left
  - `R` = Right
  - `S` = Stop

---

## 🧮 PID Tuning Tips

| Parameter | Effect |
|-----------|--------|
| **Kp** | Responsiveness to error (too high = oscillation) |
| **Ki** | Eliminates steady-state error (too high = drift) |
| **Kd** | Damps overshoot (too high = slow response) |

Start with low values and gradually increase until stable.

---

## 🧪 Applications

- 🎓 **Education**: Learn PID control, embedded systems, and robotics
- 🔬 **Research**: Platform for control algorithms and AI
- 🎮 **Hobby**: Fun and challenging DIY project
- 🤖 **Prototyping**: Base for autonomous navigation or IoT robots

---

## 📚 Documentation

- [MPU6050 Datasheet](Hardware/Datasheets/MPU6050.pdf)
- [L298N Motor Driver Tutorial](Documentation/L298N_Tutorial.pdf)
- [PID Theory Explained](Documentation/PID_Guide.pdf)

---

## 👥 Authors

- Developed as part of the **Mechatronics & Robotics** course
- Supervised by **Pr. [Name]**

---

## 📜 License

This project is open-source and available under the **MIT License**.

---

## 🤝 Contributing

Contributions are welcome! Feel free to:
- Submit issues and feature requests
- Open pull requests with improvements
- Share your own balancing robot projects

---

## 🙏 Acknowledgments

- Inspired by classic inverted pendulum control systems
- Thanks to the open-source community for libraries and tutorials
 printing
- Detailed wiring guide
- Video demonstration
