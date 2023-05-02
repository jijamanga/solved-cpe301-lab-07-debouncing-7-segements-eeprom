Download Link: https://assignmentchef.com/product/solved-cpe301-lab-07-debouncing-7-segements-eeprom
<br>



<ol>

 <li>Demonstrate methods for debouncing GPIO input.</li>

 <li>Demonstrate methods for driving parallel output.</li>

 <li>Demonstrate methods for storing non-volatile data in EEPROM memory.</li>

</ol>

<u>Required Equipment:</u>

<ol>

 <li>Arduino Mega 2560</li>

 <li>USB programming cable</li>

 <li>Laptop or Lab PC with Arduino IDE installed</li>

 <li>330 Ohm DIP Resistor</li>

 <li>7-Segment LED</li>

 <li>Push-button</li>

 <li>8-Bit Buffer (74LS373 or 74LS240 or 74LS244)</li>

 <li>Breadboard</li>

 <li>Jumper Kit</li>

</ol>

<strong><u>BEFORE THE LAB</u></strong>: Read the section on AVR memory in the 2560 datasheet starting on page 20.

<u>Procedure:</u>

<ol>

 <li>Connect a push-button and a 7-segment LED to you Arduino Mega 2560.

  <ol>

   <li>Wire the push button to be active low using the internal pullup resistor.</li>

   <li>Wire the 7-segment to a single GPIO port such that writing an 8 bit value to the port will result in a particular character being displayed on the 7-segment. Don’t forget to use a buffer chip to protect the GPIO port of your Arduino.</li>

   <li>Include in your report a table showing the 16 hex characters and the 16 byte values necessary to display the hex characters on the display as you wired it.</li>

   <li>Include in your report a circuit diagram showing how you wired your circuit.</li>

  </ol></li>

 <li>Write a program to increment your 7-segment display by one character each time the button is pressed.

  <ol>

   <li>Write the program such that it rolls-over from F back to 0.</li>

   <li>Make sure your program properly debounces the signal such that the display only increments once for each button press.</li>

   <li>The code should not contain 16 if statements or switch statements. Write your code with efficiency and maintainability in mind, refer to the timer lab for hints.</li>

   <li>Write your program to use the 2560’s onboard EEPROM memory to retain the previous display position after a power cycle.</li>

   <li>For example, if the 7-segment is displaying ‘4’ before a power cycle, it should display ‘4’ when you power it back up.</li>

  </ol></li>

</ol>

1

CPE 301 Lab #7 – Debouncing, 7-Segements, EEPROM ii. The program only needs to store one byte at a chosen address, and then read that byte back when the program starts.

iii. Write a function which stores a byte at an address, and a function which returns a byte from an address.

<ol>

 <li>Include your program in the lab report following the code submission guidelines listed below.</li>

 <li>In your lab report, detail how your program works and what steps you took to build the circuit, write the program, and test each step along the way. This description should be written like a tutorial for someone else who wishes to build a similar system.</li>

</ol>