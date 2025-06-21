# 🛡️ Airbag Deployment System – CANoe Simulation

This CANoe-based project models the behavior of an automotive airbag deployment system in response to a simulated crash event. It showcases a full simulation environment, including CAN database design, virtual dashboard panel, CAPL scripting, and realistic vehicle dynamics to emulate crash logic and safety mechanisms.

![image](https://github.com/user-attachments/assets/6a2f8c56-914b-4d0e-8ad3-b3a29370c9c3)


---

##  What is an Airbag System?
![Screenshot 2025-06-22 010600](https://github.com/user-attachments/assets/df4f48e6-99f8-437c-95b0-a0ae96cc36e8)


An airbag system is a passive vehicle safety feature designed to rapidly inflate during a collision. It provides a cushioning effect that reduces the risk of severe injuries by absorbing the force of impact. Airbags are typically triggered by electronic crash sensors that detect sudden deceleration or impact forces.

---

##  Advantages of Airbag Systems

- **Reduces the likelihood of critical injuries** during collisions by cushioning the head and chest.
- **Deploys automatically and rapidly**, minimizing the need for user action in emergencies.
- **Improves vehicle safety ratings**, meeting legal requirements and boosting consumer confidence.

---

##  Why Passenger Airbags Can Be Turned Off

- **To ensure the safety of children** or infants in rear-facing child seats, which could be harmed by airbag force.
- **When the passenger seat is unoccupied or detects a lightweight occupant**, to prevent unnecessary deployment and reduce maintenance costs.

---

##  System Behavior – How This Simulation Works

![ScreenRecording2025-06-22004825-ezgif com-video-to-gif-converter](https://github.com/user-attachments/assets/53cc4b52-87eb-46f9-860d-2fa07afa96b2)


This simulation reflects realistic airbag behavior with CAN-based messaging and logic flow:

1. **Engine Start**: Vehicle system is initialized with ignition signal ON.  
2. **Gear Engagement**: Car is shifted into forward gear to signal intent to move.  
3. **Stationary State**:  
   - Seatbelt warning light is ON.  
   - Central locking dashboard indicator is ON.  
4. **Speed Threshold Reached**:  
   - At 20 km/h, speed-sensitive locking activates.  
   - Central locking sign turns OFF to reflect locked state.  
5. **Seatbelt Use**:  
   - Driver manually fastens the seatbelt.  
   - Seatbelt warning indicator turns OFF.  
6. **Vehicle Acceleration**: Simulates dynamic driving conditions before crash.  
7. **Crash Simulation**:  
   - Airbag is deployed based on triggering logic.  
   - Speedometer freezes at the last speed value before impact.  
   - Airbag dashboard indicator stays ON post-deployment to signify activation.

---

##  Project Components

### 1. Simulation  
![Screenshot 2025-06-22 000720](https://github.com/user-attachments/assets/4a19df7f-d19e-4a96-acba-ac753fc0c874)
![Screenshot 2025-06-22 000731](https://github.com/user-attachments/assets/a42a38d1-df41-4323-9742-9b930c91d7d5)

Real-time CAN-based simulation of pre-crash, crash, and post-crash vehicle behavior.

### 2. Database Creation  
![Screenshot 2025-06-22 000603](https://github.com/user-attachments/assets/3b61f155-db6b-4922-9af2-fd3b58f56d5c)

Custom DBC file defining all relevant CAN messages, signals, and attributes for engine status, seatbelt, speed, crash detection, and airbag deployment.

### 3. Panel Design  

![Screenshot 2025-06-22 004651](https://github.com/user-attachments/assets/6552a9a9-9553-4619-b1b6-62ff1e5cae2a)


Graphical dashboard panel developed using CANoe Panel Designer, with indicators for:  
- Engine ignition  
- Gear state  
- Speedometer  
- Seatbelt and airbag lights  
- Crash trigger  
- Central locking system

### 4. CAPL Script
![Screenshot 2025-06-22 012403](https://github.com/user-attachments/assets/9b03cff4-65f9-4411-bc7c-e15e4b116cf0)

Event-driven CAPL script implementing:  
- State transitions (Idle → Driving → Crash)  
- Signal evaluation and response  
- Logging of crash event and speed capture  
- Persistent airbag indicator logic after deployment

---

##  Getting Started

1. Clone this repository.  
2. Open the CANoe configuration file (`.cfg`) in your CANoe environment.  
3. Load the DBC and panel files.  
4. Run the simulation and interact with the panel controls to test behavior.


---

## 📄 License

Open Source – Feel free to adapt and expand on this for your own automotive simulation projects.
