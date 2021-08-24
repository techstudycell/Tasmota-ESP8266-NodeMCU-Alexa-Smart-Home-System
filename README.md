# Tasmota NodeMCU Alexa Smart Home System without Coding
How to make IoT-based Smart Home Automation with Tasmota Alexa and ESP8266 NodeMCU to control 4 relays from switches &amp; Amazon Alexa app.

I have shown how to make IoT-based Smart Home Automation Using Tasmota Amazon Alexa & ESP8266 NodeMCU to control 4 home appliances from the manual switch & Amazon Alexa Appin this IoT project. If the internet is not available, then you can control the home appliances from manual switches.

During the article, I have shown all the steps to make this smart home system. You don't need any coding skills to make this project, so anyone can make it.

# Tutorial Video Link on Tasmota ESP8266 and Alexa control Relays
https://youtu.be/mJIUUSyBHUs

This Tasmota ESP8266 smart home system has the following features:

1. Control home appliances with voice command using Alexa.
2. Control home appliances with manual switches.
3. Monitor real-time feedback in the Alexa App.
4. Control home appliances manually without internet.

So, you can easily make this home automation project at home just by using a NodeMCU and relay module. Or you can also use a custom-designed PCB for this project.

# Required Components:
1. ESP8266 NodeMCU 1.0 board
2. 4-channel SPDT 5V Relay Module
3. Push Buttons or Switch
4. Alexa Echo Dot

You can make this project just by using NodeMCU and 4-channel relay module. But if you use PCB then you need the following components.

# Required Components for the PCB
1. Relays 5v (SPDT) (4 no)
2. BC547 Transistors (4 no)
3. PC817 Optocuplors (4 no)
4. 510-ohm 0.25-watt Resistor (4 no) (R1 - R4)
5. 1k 0.25-watt Resistors (5 no) (R5 - R9)
6. LED 5-mm (5 no)
7. 1N4007 Diodes (5 no) (D1 - D5)
8. Push Buttons (4 no)
9. Terminal Connectors
10. 5V DC supply

# Required Software:
1. Tasmotizer.exe
2. Amazon Alexa App

# Circuit Diagram of the NodeMCU Home Automation Project
This is the complete circuit diagram for this home automation project. I have explained the circuit in the tutorial video.

The circuit is very simple, I have used the GPIO pins D1, D2, D5 & D6 to control the 4 relays.

And the GPIO pins SD3, D3, D7 & RX are connected with push buttons to control the 4 relays manually.

I have used the INPUT_PULLUP function in Arduino IDE instead of using the pull-up resistors.

I have used a 5V mobile charger to supply the smart relay module.

Here, the D3 pin should not be connected with GND during the booting process of NodeMCU.

# Alexa Control Relay Using NodeMCU
If the NodeMCU is connected with the WiFi, then you can control the home appliances from Amazon Alexa App and also from the manual switches.

You can control, monitor the real-time status of the relays in the Alexa App from anywhere in the world.

You need an Amazon ECHO device for this home automation project.

# Control Relays Manually With Switches
You can also control the relays from the switches or pushbuttons.

You can monitor the real-time feedback in the Tasmota dashboard or Alexa App.

Please refer to the circuit diagram to connect the pushbuttons or switches.

# Design the PCB for This Smart Home System
To make the circuit compact and give a professional look, I have designed the PCB after testing all the features of the smart relay module.

Download the PCB Gerber File

# Order the PCB from JLCPCB
After downloading the Garber file you can easily order the PCB

1. Visit https://jlcpcb.com/RAB and Sign in / Sign up
2. Click on the QUOTE NOW button.
3. Click on the "Add gerber file" button. Then browse and select the Gerber file you have downloaded.
4. Set the required parameter like Quantity, PCB masking color, etc.
5. After selecting all the Parameters for PCB click on SAVE TO CART button.
6. Type the Shipping Address.
7. Select the Shipping Method suitable for you.
8. Submit the order and proceed with the payment.

You can also track your order from the JLCPCB.com

My PCBs took 2 days to get manufactured and arrived within a week using the DHL delivery option.
PCBs were well packed and the quality was really good at this affordable price.

# Solder All the Components on PCB
After that, I have soldered all the components as per the circuit diagram.
Then connect the NodeMCU board with the PCB.

# Download the Tasmota Firmware to Flash ESP8266
You need to download only two files to flash the ESP8266 NodeMCU

Download the Tasmota firmware tasmota.bin from https://ota.tasmota.com/tasmota/release/

Download the flashing tool Tasmotizer.exe from https://github.com/tasmota/tasmotizer/releases/


# Steps to flash the ESP8266 with tasmota.bin firmware

1. Connect the NodeMCU with the laptop
2. Open the Tasmotizer.exe
3. Select the proper port.
4. Select the BIN file, browse and open the tasmota.bin file
5. Check the Self-resetting and Erase before flashing.
6. Click on Tasmotize.

After the flashing completes, you will get a successful message.

# Update the WiFi Credentials
To update the WiFi credentials,

1. Click on "Send Config"
2. Enter the WiFi Name and WiFi password.
3. Click on Save. After that, you have to wait for 5-10 seconds.
4. Get the IP to Access the Tasmota Dashboard
5. Now, click on the Get IP.
6. Copy the IP address.
7. Go to any browser and enter the IP to access the Tasmota dashboard. The WiFi network should be the same.

# Configure the ESP8266 Module (GPIO)
Steps to configure the ESP8266 in Tasmota

1. Click on Configuration.
2. Click on Configure Module.
3. select the module type "Generic (0)"
4. Click on Save and go to Main Menu.
5. Now, again click on Configuration and then click on Configure Module.
6. Then map all the GPIO pins connected with Relays and Switches. (Refer to the picture)
7. Then click on the Save and go to "Main Menu".
8. Now, you can control the relays from the Tasmota dashboard.

I have selected "Relay_i" as I have used the active LOW relay module, otherwise, you can select Only "Relay".

If you use pushbutton/momentary switch select "Button", otherwise select "Switch".


# Steps to configure the Tasmota for Amazon Alexa

1. Click on Configuration.
2. Click on Configure Module.
3. Enter a Friendly Name for each device.
4. Select Hue Bridge Emulation.
5. Click on Save and go to "Main Menu"
6. Alexa will identify the device with the Friendly Name of that device.

# Configure the Alexa App to Connect Tasmota Devices
Open Amazon Alexa App and follow the steps:

1. Tap on Devices. Then Tap on the "+" icon.
2. Tap on "Light", then select "Others".
3. Goto Alexa and tap on "DISCOVER DEVICES". It will take a minute to add devices. During this time the ESP8266, Echo Dot should be connected with the same WiFi.
4. Tap on "Devices", and tap on "Lights" to see all the devices.



# Finally!! the Tasmota Alexa Home Automation System Is Ready
Without writing a single line code, our Tasmota Alexa Home automation system is ready.

Now you can control the appliances from anywhere in the world from the Amazon Alexa app.

You can also control the appliances from switches and monitor the real-time feedback.

I hope you have liked this Alexa home automation project. I have shared all the required information for this project. I will really appreciate it if you share your valuable feedback.

Also if you have any query please write in the comment section.

Thank you & Happy Learning.
