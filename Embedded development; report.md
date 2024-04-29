Embedded development;

## Challenge 1.
1) Make a 3 bit full adder using 8x1 mux and Arduino (Arduino should be used to adjust the select lines).

First i made an 8x1 mux using 7- 2x1 mux(there was no direct way to impelement 8x1 in WOKWI.com). Then i connected 8 input and 3 select lines to the Arduino. Then, i took the ouutputs from the truth table of full adder and pre set the vlaues of inputs which bear an output value of 1. Thus full adder is obtained from mux.For the carry, you have to change the values of inputs according to the truth table  of the carry.

[project link](https://wokwi.com/projects/394438977301562369)


## Challenge 5.
5) Make a Caesar Cipher decoder simulation using Arduino. (encoded data should be sent through serial).

 For this task i took two arduinos connected the transmitter and reciever ports of them for serial communication(0,1 pins respectively), then connected them to a common ground. Then i created a character variable for inputiing the text to be encoded. Even though we add text as a string, arduino ide will Compile it as character by character, hence in the loop section i directly added the amount of shift i required in my text. Therefrore my text will get encoded and encoded text will be printed on the serial monitor. Then on my reciver arduino i do the same thing except add the negative value of shift that i have given in the encoder. Hence my encoded text will be decoded in the recievr arduino and it will be printed in the serial monitor.

 [project link](https://www.tinkercad.com/things/5TJy9A5oKBb-shiny-allis-hango/editel)

 // For the reciever arduino there are some garbage values printed on the serial monited before my required values are printed(dont know the reason. T_T)

## Challenge 3.
3)  Collect the data printed into the serial using an Arduino, and then send that data over to another Arduino which is connected to a 16x2 lcd and print the received data into the lcd display. Use the UART communication protocol to send the message over.

For this task i took 2 arduinos and connected it through seial communication. Then for the transmitter arduino, i creatted a character variable and store its value as Seial.read() and printed the same value on serial monitor. Then at the reciever end i check if any value is available in serial monitor through seril.available() command. And if there is any vlaue available, store it into a variable. On the receiver side i initialized the lcd display pins and usig lcd.print(), printed the received data into the lcd.    

[project link](https://www.tinkercad.com/things/9fhaL8M3EhR-bodacious-krunk-wluff/editel?tenant=circuits)

## Challenge 4

4)Make a secure lock with an Arduino and a keypad. Enter an 8 digit pin(the pin shouldn't be stored in plaintext, use encryption) on the keypad. If the pin matches, a servo will turn and the status of the door should be displayed on an OLED screen. The servo should turn back to it's original position after around 5-10 seconds.

For this task i connected arduino with a keypad, servo motor and an oled display. I included the library <Keypad.h> for the keypad and initialized all the values coorespoding to each  keys on the keypad. Then i defined the pins connecting the keypad to the arduino. Then set the length of password as 8. After that i create to an array to store the values entered by the user.The values entered by the user were printed as '*' for encryption. After that i created an array and stored the password. Then using a foor loop iterated through each values of both array to check
if both are same, if same it will rotate the servo motor 180 degrees and status of door will be displayed on the oled screen. For oled screen i connected the two data pins to analog A4 and A5 for I2c communication. If wrong password is entered Serial monitor will display wrong passowrd. A delay seconf of 6 seconds is defined to close the door after opening and the oled screen will display closed and servo will return to its original position.

[project link](https://wokwi.com/projects/396301889925358593)
   
## Challenge 2
2)  On this challenge ddrxn was defined as a data direction bit(0x24), portx was defined as a port (0x25)and pinx is definde as a pin(0x23). in the setup section ddrxn is set value by (1<<5) which is a bitwise shift operator  and its  its output will set the fifth bit to high, ie: set pin number 13 as output. ddrxn &= ~(1<<4); this will set fifth bit to low ie: set pinnumber 12 as input. portx |= (1<<4); this will set the 12 th pin to high.
In the loop section if command will check weathe value at pin number 12 is low or not, as it is set to high else condition will satisfy at it will set a low volatage to pin number 12. For the simulation used a pull up resitor using a push button and set the value at 12 to high always, when push button is pressed value at 12 becommes zero and pin 13 is set to high which turns on the in-built led.

[project link](https://www.tinkercad.com/things/bWEp4oGHIhZ-super-krunk-bombul/editel?sharecode=i5OBrx5EOMEgSww6ixSSEMW8FsxPUzPoBiga9rx7fKQ)
