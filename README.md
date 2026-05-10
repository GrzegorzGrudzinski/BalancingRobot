# Self-Balancing Robot

## Project Goals:

A two-wheeled self-balancing robot powered by BLDC motors.
The robot can interface with a simulation as a **"Digital Twin"**.

The objective of this project is to learn and expand knowledge in:

* **BLDC motors** and their control
* Using **simulations in robotics**
* **Sim-to-Real** transfer
* **AI and Reinforcement Learning (RL)**
* Practical application of various **controllers/regulators**

## Bill of Materials (BOM):

**Drive System (Actuators):**

* **Motors:** 2x Flycat iRotor 5010 360kV BLDC
* **Motor Driver:** MKS DualFOC v3.2 Plus + ESP32
* **Encoders:** 2x AS5047P (operating in ~~ABI~~ SPI mode)

**Control System:**

* **MCU:** STM32F401CC (Blackpill)
* **IMU:** MPU6050

Inter-board communication (STM32 to ESP32) is handled via **UART**.

## Simulator Description:

* **Physics Engine:** PyBullet

**Simulator Features:**

* Enables testing robot behavior with different **controllers and tuning parameters** before deployment on physical hardware.
* Provides an environment for **reinforcement learning**.

**The simulator can operate in several modes:**

* **Standalone:** 100% simulated environment.
* **Hardware-in-the-loop (Slave):** The main robot controller connects to the simulation – the physical MCU calculates the control parameters, while the simulator executes the physics and movement.

## Project Status

...