SKILL ASSIGNMENT-2

PROGRAM:
Write an assembly language program in 8051 to generate a 200 µs delay using Timer 0 in Mode 1 and toggle Port 0.1.


APPARATUS REQUIRED:

Laptop with Keil Software

PROGRAM:
```
ORG 0000H

MAIN:
    MOV TMOD, #01H       
    MOV P0, #00H        

HERE:
    ACALL DELAY_200US  
    CPL P0.1           
    SJMP HERE        

DELAY_200US:
    MOV TH0, #0FFH        
    MOV TL0, #038H       
    SETB TR0          

WAIT_T0:
    JNB TF0, WAIT_T0     
    CLR TR0            
    CLR TF0             
    RET                

END
```
OUTPUT:

<img width="1911" height="1139" alt="image" src="https://github.com/user-attachments/assets/61621525-94c7-40d2-8e2f-75aa10ee8439" />


<img width="1919" height="1139" alt="image" src="https://github.com/user-attachments/assets/51fa21dc-c585-47b2-b481-0d2a386ad63b" />


RESULT:

Therefore the assembly language program in 8051 to generate a 200 µs delay using Timer 0 in Mode 1 and toggle Port 0.1 is executed.
