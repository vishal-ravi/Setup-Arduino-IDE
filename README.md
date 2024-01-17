# Arduino IDE Setup for NODEMCU ESP8266

This repository provides a guide on setting up the Arduino IDE for NODEMCU ESP8266 development. Follow the steps below to get started:

## Step 1: Installing Arduino IDE Software
Download and install the Arduino IDE software from [Arduino's official website](http://www.arduino.cc/en/main/software).

![image](https://github.com/vishal-ravi/Setup-Arduino-IDE-/assets/98887033/cd406258-1a33-43af-acd4-9916d273c976)



## Step 2: Arduino IDE Icon
After installing Arduino IDE, an icon will be created on your desktop. Use this icon to open the Arduino IDE.

## Step 3: Opening Arduino IDE
Click on the Arduino IDE icon to open the Arduino window.

![image](https://github.com/vishal-ravi/Setup-Arduino-IDE-/assets/98887033/696cfe1b-c5c8-4ca1-acac-af1b740a6908)


## Step 4: Preferences
Open the "File" menu and click on "Preferences" as shown in the figure.

![image](https://github.com/vishal-ravi/Setup-Arduino-IDE-/assets/98887033/7aee8b37-6287-4d28-90af-ef79d5125d17)


## Step 5: Adding ESP8266 Board Manager

![image](https://github.com/vishal-ravi/Setup-Arduino-IDE-/assets/98887033/c0d88ff8-0e80-4db3-9e8a-863631229e28)

In the "Additional Boards Manager URLs" field, enter the following URL:
```
http://arduino.esp8266.com/stable/package_esp8266com_index.json
```
Click "OK" to save.

## Step 6: Selecting Board

![image](https://github.com/vishal-ravi/Setup-Arduino-IDE-/assets/98887033/72400739-4cd5-46f6-b191-c1fff01c457c)

Open the "Tools" menu, go to "Board," and select "Arduino/Genuino Uno." Then, click on "Boards Manager" as shown in the figure.

## Step 7: ESP8266 Board Package

![image](https://github.com/vishal-ravi/Setup-Arduino-IDE-/assets/98887033/8a55e8d7-9f94-4d7b-aa30-ff351dca1f06)

In the Boards Manager window, scroll to the bottom until you find the module with the name "ESP8266." Select the module, choose the version, and click "Install." Once installed, it will display "Installed," and you can close the window.

## Step 8: Selecting ESP8266 Arduino Board
![image](https://github.com/vishal-ravi/Setup-Arduino-IDE-/assets/98887033/4478d95c-07aa-44f3-85de-405e1792dc16)

To use ESP8266 with Arduino, select the Board: "Arduino/Genuino Uno" and change it to "NodeMCU 1.0 (ESP-12E Module)" or other ESP8266 modules based on your hardware. Scroll down to find the appropriate option.

## Step 9: Connecting ESP8266 to the PC
Connect the ESP8266 module to your computer using a USB cable. When the module is connected, a COM port will be detected (e.g., COM5), as shown in the figure.

## Step 10: Test the below Program in Arduino IDE

```c
// Test code
void setup() {
  // initialize digital pin LED_BUILTIN as an output.
  pinMode(LED_BUILTIN, OUTPUT);
}

// the loop function runs over and over again forever
void loop() {
  digitalWrite(LED_BUILTIN, HIGH);  // turn the LED on (HIGH is the voltage level)
  delay(1000);                      // wait for a second
  digitalWrite(LED_BUILTIN, LOW);   // turn the LED off by making the voltage LOW
  delay(1000);                      // wait for a second
}
```

## Step 11: Selecting COM Port

![image](https://github.com/vishal-ravi/Setup-Arduino-IDE-/assets/98887033/53c40ed9-0cc8-4f30-bcc7-5e57e305d5a7)


Click on "Tools" and select the port under "Port" based on the ESP8266 module connected to your computer. Refer to the previous steps for selecting the COM port.

## Step 12: Uploading the Program to ESP8266 Module

![image](https://github.com/vishal-ravi/Setup-Arduino-IDE-/assets/98887033/8b6eb733-63ee-4dc1-aa94-01b30e1f7b52)


1. In the Blink example code, change all instances of the pin number "13" to "16."

```c
void setup() {
  // initialize digital pin 16 as an output.
  pinMode(16, OUTPUT);
}

// the loop function runs over and over again forever
void loop() {
  delay(10);
  digitalWrite(16, HIGH);   // turn the LED on (HIGH is the voltage level)
  delay(1000);               // wait for a second
  digitalWrite(16, LOW);    // turn the LED off by making the voltage LOW
  delay(1000);               // wait for a second
}
```

2. Click on the right arrow button (upload button) as shown in the figure to upload the program to the module.


This will start the blinking LED on the onboard LED of the NODEMCU module connected to pin D0 (GPIO16). You have successfully uploaded and run a basic program on your NODEMCU ESP8266 module using the Arduino IDE.

Feel free to explore and modify the code for more complex projects!

Now you're ready to start programming your NODEMCU ESP8266 using the Arduino IDE. Happy coding!
