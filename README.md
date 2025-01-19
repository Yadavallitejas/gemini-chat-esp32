# Gemini Chat Assistant on ESP32

This project demonstrates the integration of the **Gemini API** with an **ESP32 development board** to create a simple chat assistant. It allows users to input text commands through the Serial Monitor and receive AI-generated responses in real time. This project is perfect for IoT and AI enthusiasts interested in combining embedded systems with AI capabilities.

---

## Table of Contents
- [Features](#features)
- [Hardware and Software Requirements](#hardware-and-software-requirements)
- [Setup Instructions](#setup-instructions)
- [How It Works](#how-it-works)
- [Dependencies](#dependencies)
- [Example Usage](#example-usage)
- [Acknowledgments](#acknowledgments)

---

## Features
- **Wi-Fi Enabled**: Connects to a Wi-Fi network to communicate with the Gemini API.
- **Real-Time Chat**: Allows real-time input and output via the Serial Monitor.
- **Lightweight**: Designed to run efficiently on ESP32 with minimal resource requirements.
- **Customizable**: Modify the code to extend functionality or adapt to other APIs.

---

## Hardware and Software Requirements

### Hardware
- **ESP32 Development Board**: Compatible with ESP32 DevKit V1 or similar boards.
- **Micro-USB Cable**: For programming and powering the board.

### Software
- **Arduino IDE**: Latest version recommended.
- **ESP32 Board Support**: Install via Arduino Board Manager.
- **Gemini API Key**: A valid API key from Gemini.

---

## Setup Instructions

### Step 1: Clone the Repository
Download the project files:
```bash
git clone https://github.com/yadavallitejas/gemini-chat-esp32.git
cd gemini-chat-esp32
```
### Step 2: Install Arduino IDE and Libraries
1. **Download Arduino IDE**:
   - [Arduino IDE Official Download Page](https://www.arduino.cc/en/software)
2. **Install ESP32 Board Support**:
   - Go to **File > Preferences** in the Arduino IDE.
   - Add the following URL to "Additional Board Manager URLs":
     ```
     https://dl.espressif.com/dl/package_esp32_index.json
     ```
   - Go to **Tools > Board > Boards Manager**, search for "ESP32", and install it.
3. **Install Required Libraries**:
   - Open **Tools > Manage Libraries** and install the following:
     - **WiFi**
     - **HTTPClient**
     - **ArduinoJson**

### Step 3: Configure the Code
1. Open `gemini_on_esp32.ino` in Arduino IDE.
2. Update the following variables in the code:
   ```cpp
   const char* ssid = "your_wifi_name";        // Your Wi-Fi SSID
   const char* password = "your_wifi_password"; // Your Wi-Fi password
   const char* Gemini_Token = "your_gemini_api_key"; // Your Gemini API key
   const char* Gemini_Max_Tokens = "200";      // Maximum token limit for responses
   ```

### Step 4: Upload the Code
1. Connect your ESP32 to your computer via a USB cable.
2. Select your board and port in Arduino IDE:
   - **Board:** ESP32 Dev Module.
   - **Port:** Select the correct COM port.
3. Click the **Upload** button to compile and upload the code to your ESP32.

### Step 5: Open Serial Monitor
1. After uploading the code, open the Serial Monitor in Arduino IDE.
2. Set the baud rate to `115200`.
3. Wait for the ESP32 to connect to your Wi-Fi network.
4. Input queries or commands in the Serial Monitor and observe the AI-generated responses.

---

## How It Works
1. **Wi-Fi Connection**: The ESP32 connects to the specified Wi-Fi network using the provided credentials.
2. **User Input**: Input is entered via the Serial Monitor and sent to the Gemini API.
3. **API Request**: The ESP32 sends an HTTP POST request to the Gemini API with the user input.
4. **Response Handling**: The API's response is received, parsed using ArduinoJson, and displayed on the Serial Monitor.

---

## Dependencies
Ensure the following libraries are installed in Arduino IDE:
- **WiFi**: Built-in library for ESP32 to handle Wi-Fi connectivity.
- **HTTPClient**: For making HTTP requests to the Gemini API.
- **ArduinoJson**: For parsing JSON responses from the API.

---

## Example Usage

### Input
In the Serial Monitor, enter:
```
Hello! What's the weather today?
```

### Output
The Serial Monitor will display:
```
The weather today is sunny with a high of 28°C.
```

This demonstrates how the ESP32 communicates with the Gemini API to process user queries and generate responses.

---

---

## Acknowledgments
- **Gemini API**: For powering the AI functionality.
- **Arduino**: For providing a robust platform for IoT development.
- **ESP32 Community**: For extensive documentation and support.

---

```

