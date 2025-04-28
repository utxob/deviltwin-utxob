# deauther-eviltwin-utxob

# DevilTwin - ESP8266 WiFi Deauthentication & Evil Twin Attack

**DevilTwin** is a WiFi Deauthentication and Evil Twin Attack tool that runs on the ESP8266 microcontroller. It is specifically designed for testing the security of WiFi networks. However, if you intend to use it experimentally, please proceed with caution and only use it on your own networks.

## Features
- **WiFi Deauthentication Attack**: Disconnects users from a targeted WiFi network.
- **Evil Twin Hotspot**: Creates a fake hotspot with the same name as a selected WiFi network, potentially capturing user passwords.

## Requirements
1. **ESP8266 Development Board** (e.g., NodeMCU)
2. **Arduino IDE** or **PlatformIO** (your preferred development environment)
3. **WiFi Network Info** (SSID, Channel, BSSID)

## Setup and Flashing Process

### 1. **Install Arduino IDE**
First, you need to install the **Arduino IDE**. You can download it [here](https://www.arduino.cc/en/software).

### 2. **Install ESP8266 Board Support**
- Open the Arduino IDE.
- Go to "File" > "Preferences".
- In the "Additional Boards Manager URLs" field, add the following URL:

http://arduino.esp8266.com/stable/package_esp8266com_index.json

- Go to "Tools" > "Board" > "Boards Manager", search for **ESP8266**, and install it.

### 3. **Setup Project Files**
- Download the code from this repository.
- Open the code in Arduino IDE.
- Select "Tools" > "Board" > "NodeMCU 1.0 (ESP-12E Module)".
- Select your ESP8266 port under "Tools" > "Port".

### 4. **Install Required Libraries**
This project uses specific libraries that you need to install:
- **ESP8266WiFi** (Primary WiFi support for ESP8266)
- **DNSServer** (For DNS functionality)
- **ESP8266WebServer** (For web server functionality)

To install them:
- Go to "Sketch" > "Include Library" > "Manage Libraries".
- Search for and install **ESP8266WiFi**, **DNSServer**, and **ESP8266WebServer**.

### 5. **Flash the Code**
- After selecting the correct board and port, click the "Upload" button in Arduino IDE.
- The code will flash to your ESP8266 device. This will take a few seconds.

### 6. **Running the Code**
- SSID: DevilTwin.
- PASSWORD: 12345678.
- After successful flashing, open your web browser and navigate to **192.168.1.1**.
- You will be presented with a webpage showing a list of available WiFi networks.
- Select a network and input the password in the provided form.

## Usage Instructions

1. **WiFi Scanning**:
 - Initially, a WiFi scan will begin, showing the list of available networks.

2. **Deauthentication Attack**:
 - After selecting a network, you can initiate the Deauthentication Attack, which disconnects users from the network.

3. **Evil Twin Hotspot**:
 - You can create an Evil Twin Hotspot, mimicking a selected WiFi network and creating a fake hotspot.

4. **Password Collection**:
 - If the correct password is provided, you will successfully capture the network's password.

## Security Warning
- This project should only be used for research and security testing.
- Using this tool on someone else's network without permission is illegal and may result in legal consequences.
- Please ensure you only use this tool on your own networks.

## Resources and References
- [ESP8266 Official Documentation](https://arduino.esp8266.com/)
- [Arduino Website](https://www.arduino.cc/)



## License
This project is open-source and licensed under the MIT License.
