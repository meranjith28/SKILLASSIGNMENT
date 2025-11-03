SKILL ASSIGNMENT-1

PROGRAM:
Write an assembly language program in 8051 to generate the Fibonacci series up to N terms and store the sequence in memory.


APPARATUS REQUIRED:

Laptop with Keil Software

PROGRAM:
```
ORG 0000H
MOV R0, #30H      
MOV R1, #0AH      
MOV A, #00H       
MOV B, #01H    
MOV @R0, A      
INC R0
MOV @R0, B      
DEC R1           
DEC R1
NEXT_TERM:
        MOV A, B        
        MOV R5, A        
        DEC R0         
        MOV A, @R0     
        INC R0         
        ADD A, R5       
        INC R0         
        MOV @R0, A     
        MOV B, A       
        DJNZ R1, NEXT_TERM
HERE:   SJMP HERE         
        END
```
OUTPUT:
![WhatsApp Image 2025-11-03 at 18 07 27_1b5f31bf](https://github.com/user-attachments/assets/1a347f07-8914-47fa-a098-7e278cb4c346)

![WhatsApp Image 2025-11-03 at 18 06 38_0633f919](https://github.com/user-attachments/assets/21708def-7ff4-4eb0-86d9-2e8d83a34e45)



RESULT:
Thus the assembly language program in 8051 to generate the Fibonacci series up to N terms and store the sequence in memory is executed.




