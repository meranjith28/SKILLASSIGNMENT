SKILL ASSIGNMENT-2

PROGRAM:
Write an assembly language program in 8051 to generate a 5 ms delay using Timer 1 in Mode 1 and toggle an LED connected to Port 1.7 continuously.

APPARATUS REQUIRED:

Laptop with Keil Software

PROGRAM:
```
ORG 0000H
MAIN:  
    MOV TMOD, #10H
    CLR P1.7
LOOP:
    ACALL DELAY_5MS
    CPL P1.7
    SJMP LOOP
DELAY_5MS:
    MOV TH1, #0xEC
    MOV TL1, #0x78
    SETB TR1
WAIT:
    JNB TF1, WAIT
    CLR TR1
    CLR TF1
    RET
END
```
OUTPUT:
![WhatsApp Image 2025-11-03 at 18 16 14_2432e573](https://github.com/user-attachments/assets/1824cd77-4df6-49ad-9026-91e6649ebe15)

![WhatsApp Image 2025-11-03 at 18 16 51_6d893024](https://github.com/user-attachments/assets/b4476463-45dd-4d86-ba1a-c39016db90c5)




RESULT:
Thus the assembly language program in 8051 to generate a 5 ms delay using Timer 1 in Mode 1 and toggle an LED connected to Port 1.7 continuously is executed.




