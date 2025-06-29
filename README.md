# servo_gate_ultrasonic.ino
# 🚧 Ultrasonic Sensor Based Servo Gate Control

This project uses an **HC-SR04 ultrasonic distance sensor** to detect nearby objects and triggers a **servo motor** to rotate accordingly. Ideal for **automatic gate**, **dustbin lids**, or **obstacle-activated mechanisms**.

---

## 🧰 Components Required

- Arduino UNO  
- HC-SR04 Ultrasonic Sensor  
- Servo Motor (SG90 or similar)  
- Breadboard + Jumper Wires  
- (Optional) 5V external supply for servo

---

## 🔌 Pin Connections

| Component        | Arduino Pin |
|------------------|-------------|
| Ultrasonic Trig  | D3          |
| Ultrasonic Echo  | D5          |
| Servo Signal     | D9          |
| VCC/GND          | 5V / GND    |

---

## ⚙️ How It Works

1. The ultrasonic sensor sends a 10μs pulse and measures echo return time.
2. The code calculates distance in cm.
3. If an object is detected within `10 cm`:
   - Servo turns to **90°** (e.g., gate opens)
4. Else:
   - Servo returns to **0°** (gate closed)

---

## 📁 Project Files

- `code/servo_gate_ultrasonic.ino` – Main Arduino sketch

---

## 📈 Sample Output (Serial Monitor)

```text
Distance: 12 cm
Distance: 9 cm
[Servo rotates]
Distance: 15 cm
