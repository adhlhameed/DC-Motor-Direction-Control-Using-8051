# DC Motor Direction Control Using 8051
## Aim:
To implement a DC Motor Direction Control Using 8051 
## Apparatus Required:
Laptop with Keil uVision software
<br>Proteus Design Suite
## Algorithm:
1. Start the program.
2. Open C program text file.
3. Type the program.
4. Select the hex file creation before building the program.
5.Build/compile the program.
6. Start debugging.
7. Open Proteus Software & design circuit as per circuit diagram.
8. Copy the hex file to 8051 controller.
9.Simulate the circuit in Proteus software.
## Program :
#include <reg51.h>


sbit mp = P1^0; // P1.0

sbit mn = P1^1; // P1.1


void main(void)

{

volatile unsigned int a; // volatile prevents some compilers from optimizing the delay away


mp = 0;

mn = 0;


while (1)

{

mp = 1;

mn = 0;

for (a = 1; a < 40000; a++) {

; // empty delay loop

}


mp = 0;

mn = 1;

for (a = 1; a < 40000; a++) {

; // empty delay loop

}

}

}
## Output :
<img width="715" height="551" alt="image" src="https://github.com/user-attachments/assets/95905c5c-de49-4bdc-a06f-04513c00b78f" />

## Result:
The DC Motor direction control using 8051 microcontroller has been successfully implemented and simulated using Keil and Proteus.
