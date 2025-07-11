# Two_Layer_Security_SystemTo develop a robust access control system that verifies a user’s identity through two sequential security checks—RFID tag scanning via EM-18 sensor and a secondary password/keypad verification.

🔧 Hardware Requirements
| Component | Description | 
| EM-18 RFID Reader | Reads RFID tags using 125kHz frequency | 
| RFID Tags/Cards | Predefined authorized unique IDs | 
| Arduino Uno/Nano | Microcontroller for processing and control | 
| 16x2 LCD Display | Displays instructions and status messages | 
| Keypad (4x4 Matrix) | For second-level password input | 
| Relay Module | Controls door lock or motor | 
| Buzzer | Alerts for incorrect or unauthorized attempts | 
| Power Supply | 12V or USB depending on microcontroller | 



⚙️ Connections Overview
🔹 EM-18 RFID Reader
- TX → Arduino RX (Pin 0)
- GND → Arduino GND
- VCC → Arduino 5V
🔹 Keypad (4x4)
- Connect 8 digital pins to Arduino D2–D9
- Use keypad library to map rows and columns for input
🔹 LCD Display (16x2)
- Use I2C Module to simplify wiring:
- SDA → A4
- SCL → A5
- VCC → 5V
- GND → GND
🔹 Relay Module
- IN → Arduino D10
- VCC → 5V
- GND → GND
🔹 Buzzer
- Positive → Arduino D11
- Negative → GND

📜 Project Flow
- EM-18 scans RFID tag.
- If tag ID is authorized:
- LCD prompts for password.
- User inputs password via keypad.
- If password is correct:
- Relay activates and door unlocks.
- LCD shows “Access Granted”
- If either RFID or password fails:
- LCD shows “Access Denied”
- Buzzer sounds

✅ Optional Enhancements
- Add logging with SD card or cloud platform (e.g., Firebase)
- Time-based access or one-time passwords (OTP)
- Face recognition with camera module for third-layer security

I can help you with the Arduino code next, or whip up a schematic diagram to visualize the setup. Just say the word! 😊
                      
