Embedded development;

## Challenge 1.
1) Make a 3 bit full adder using 8x1 mux and Arduino (Arduino should be used to adjust the select lines).

First i made an 8x1 mux using 7- 2x1 mux(there was no direct way to impelement 8x1 in WOKWI.com). Then i connected 8 input and 3 select lines to the Arduino. Then, i took the ouutputs from the truth table of full adder and pre set the vlaues of inputs which bear an output value of 1. Thus full adder is obtained from mux.For the carry, you have to change the values of inputs according to the truth table  of the carry.

[project link](https://wokwi.com/projects/394438977301562369)


## Challenge 5.
5) Make a Caesar Cipher decoder simulation using Arduino. (encoded data should be sent through serial).

 For this task i took two arduinos connected the transmitter and reciever ports of them for serial communication(0,1 pins respectively), then connected them to a common ground. Then i created a character variable for inputiing the text to be encoded. Even though we add text as a string, arduino ide will Compile it as character by character, hence in the loop section i directly added the amount of shift i required in my text. Therefrore my text will get encoded and encoded text will be printed on the serial monitor. Then on my reciver arduino i do the same thing except add the negative value of shift that i have given in the encoder. Hence my encoded text will be decoded in the recievr arduino and it will be printed in the serial monitor.
