# Smart-Door-Lock-in-Arduino

RFID tag and Keypad based Smart Door Lock using Arduino

## Introduction

In this project we created an Arduino UNO, RFID reader door lock. To open the door the user will first scan the right tag and then he will have to enter the correct password on numeric keypad. On scanning the wrong tag or entering the wrong password the system will deny access and a buzzer alarm will sound. A servo motor will be used to represent the door lock and an I2C LCD will be used to display appropriate prompts.

## Components

* Arduino Uno
* I2C LCD
* MFRC522 RFID reader
* SG90 Servo Motor
* 4x4 Keypad
* LED x3
* Resistor 220 ohm x3
* Buzzer
* 6 to 12V Power Supply
* Wires

## Working
1. Firstly, there will be a blue LED lit all the time to show that the circuit is working and the I2C LCD will be displaying a message saying “Door Lock! Scan Your Tag”.
2. Following the message, the user will scan his card on the RFID Tag reader RC522. LCD will display “Tag matched” message and green LED will be on for 3 seconds. 
3. If the card he is scanning is an authorized card, the system will go to next state in which a four digit numeric password will asked and the LCD will display “Enter Password:”. Upon entering the correct password, again the green LED will be on for 3 seconds and LCD will display “Pass accepted” messaged. 
4. SG90 Servo motor will rotate 90 degrees portraying that the door has been unlocked and after 10 seconds, the door will again be locked. 
5. If the user has entered the wrong password, “Wrong password” will be shown on the LCD and red LED will be on for 3 seconds and simultaneously the buzzer will ring for 3 seconds duration. 
6. Also, if during card scanning, the user has scanned the wrong card, “Access denied” message will be shown on the LCD, and red LED and buzzer will ring for 3 seconds. 
