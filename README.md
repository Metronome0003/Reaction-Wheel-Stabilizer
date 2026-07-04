# Reaction-Wheel-Stabilizer
# Reaction Wheel Attitude Control Demonstrator

## Project Objective
This project is a benchtop spacecraft attitude stabilizer acting as an inverted pendulum, balanced entirely by a single reaction wheel. The goal is to successfully integrate embedded hardware, real-time sensor fusion, and physical manufacturing to demonstrate orbital control mechanics.

## System Architecture
The control system relies on real-time feedback loop management to maintain physical equilibrium:
* **Sensors:** An `MPU6050 IMU` captures pitch and roll rates. An `AS5048A Magnetic Encoder` tracks the motor's exact position.
* **Processing:** An `ESP32` microcontroller processes sensor data, utilizing an Extended Kalman Filter to mitigate sensor noise and drift.
* **Control Logic:** A Cascaded PID controller computes the required torque to correct deviations from center.
* **Actuation:** A `SimpleFOC` driver sends phase commands to the BLDC motor to accelerate/decelerate the reaction wheel, producing the stabilizing physical torque.

## Bill of Materials (BOM)
* **Microcontroller:** ESP32 Development Board
* **Motor:** iPower GM4108H-120T Brushless DC (BLDC) Gimbal Motor
* **Motor Driver:** SimpleFOC Mini / compatible BLDC driver
* **Sensors:** MPU6050 (6-axis IMU), AS5048A (14-bit Magnetic Encoder)
* **Hardware:** Custom 3D-printed components (flywheel, pivot, motor mount)

## Development Phases
- [ ] **Phase 1: Component Sourcing & System Architecture Planning** (Current Phase)
- [ ] **Phase 2: Mechanical Design & CAD** (Drafting the pivot and balancing the flywheel in Fusion 360)
- [ ] **Phase 3: 3D Printing & Physical Assembly**
- [ ] **Phase 4: Embedded C++ Integration** (Wiring harness fabrication and reading raw sensor data)
- [ ] **Phase 5: Control Theory Application** (Tuning the Kalman filter and PID loops for stable balance)
