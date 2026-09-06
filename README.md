# 🏎️ Analog Line-Following Robot

An autonomous line-following robot built entirely with hardware logic—no microcontrollers involved. This project uses IR sensors for detection and an operational amplifier (Op-Amp) as a comparator to control the motor drivers, demonstrating fundamental control systems and circuit design.

## ⚙️ How It Works (Hardware Logic)
Instead of writing C++ or Python to process sensor data, this robot relies on analog voltage comparisons:
* **Sensing:** Two IR sensor modules face the ground to differentiate between the dark line and the light surface.
* **Logic (Comparator):** An LM358 Op-Amp continuously compares the voltage from the IR sensors against a reference voltage (set via potentiometers).
* **Actuation:** When a sensor detects the line, the Op-Amp outputs a high/low signal to the motor driver (e.g., L293D or L298N), turning off the corresponding motor to steer the robot back on track.

## 📂 Repository Contents
* `Proteus_Simulation/` - Contains the `.pdsprj` file. You can run this simulation to see the Op-Amp comparator logic and motor response before building the physical circuit.


## 🛠️ Bill of Materials (BOM)
* LM358 Operational Amplifier
* 2x IR Sensor Modules
* L298N (or L293D) Motor Driver Module
* 2x DC Gear Motors with Wheels
* Robot Chassis & Caster Wheel
* Power Supply / Battery Pack
* Resistors & Jumper Wires

## 🚀 How to View the Simulation
1. Clone this repository: `git clone https://github.com/YourUsername/analog-line-follower.git`
2. Open the `.pdsprj` file in **Proteus**.
3. Run the simulation. You can interact with the logic states on the IR sensor inputs to watch the motor rotation directions change in real-time.
