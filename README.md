ESP32-CAM Telegram Bot Project
Overview

This project demonstrates how to configure an ESP32-CAM microcontroller to connect to WiFi and communicate with a Telegram bot. The ESP32-CAM captures images and sends them directly through Telegram commands using the Telegram Bot API.

The project introduces IoT concepts including:

WiFi communication
Web-based messaging
Camera integration
Telegram Bot API interaction
ESP32 microcontroller programming
YOUR_NAME : NOTES FOR CSN150
Purpose

The purpose of this project was to learn how to:

Configure and program an ESP32-CAM board
Connect the ESP32 to a WiFi network
Create and use a Telegram bot
Send images from the ESP32-CAM to Telegram
Understand basic IoT communication between hardware and cloud services
Equipment Used
ESP32-CAM (AI Thinker)
USB cable
FTDI programmer / onboard USB programmer
Computer or laptop
WiFi network
Smartphone with Telegram installed
Tools Used
Arduino IDE
Telegram
BotFather
myidbot
GitHub
GPT-4 / ChatGPT
ESP32 Board Package
UniversalTelegramBot Library
ArduinoJson Library

Steps I Followed

1. Installed Arduino IDE

Downloaded and installed Arduino IDE on my computer.

2. Installed ESP32 Board Package
In Arduino IDE:
Opened Preferences
Added the ESP32 board manager URL
Installed ESP32 boards through Board Manager

3. Connected the ESP32-CAM
Connected the ESP32-CAM to the computer using USB
Selected:
Board: AI Thinker ESP32-CAM
Correct COM Port

5. Created a Telegram Bot
Opened Telegram
Searched for BotFather
Used /newbot
Created a bot name and username
Copied the bot token

7. Retrieved Telegram Chat ID
Opened myidbot
Sent /getid
Copied the Chat ID

9. Installed Required Libraries

Installed:

UniversalTelegramBot
ArduinoJson

using Arduino IDE Library Manager.

7. Updated the Arduino Code

Modified the code by:

Adding WiFi SSID and password
Adding Telegram bot token
Adding Chat ID

Example:

const char* ssid = "SpectrumSetup-****";
const char* password = "***************";

String BOTtoken = "7697246797:AAFoIZigBSovICWMZIIUtzwD4-7aKPHgUTE";
String CHAT_ID = "93372553";
8. Uploaded the Code
Verified the sketch
Uploaded it to the ESP32-CAM
Opened Serial Monitor at 115200 baud
9. Tested the Telegram Bot

Sent the following commands to the bot:

/start
/photo

The ESP32-CAM successfully captured and sent a photo through Telegram.

Problems / Solutions
Problem 1: ESP32 Would Not Connect to WiFi

Cause: I was using a 5GHz WiFi network.

Solution: Switched to a 2.4GHz WiFi network because ESP32 only supports 2.4GHz.


Problem 3: Upload Failed

Cause: ESP32-CAM entered incorrect boot mode.

Solution: Held the BOOT button while uploading the code.


Final Report

This project successfully demonstrated communication between an ESP32-CAM and Telegram using WiFi and the Telegram Bot API. The ESP32-CAM was able to connect to the local network, receive commands from Telegram, capture photos, and send them back through the messaging platform.

Through this project, I learned how IoT devices communicate with cloud-based applications and how microcontrollers can be integrated with messaging services for remote monitoring and automation. I also gained experience troubleshooting hardware, WiFi connectivity, and software configuration issues.

The project showed the practical applications of IoT systems and improved my understanding of embedded systems programming using Arduino IDE.




