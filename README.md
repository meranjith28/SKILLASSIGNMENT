SKILL ASSIGNMENT-1

PROGRAM:
Write an assembly language program in 8051 to find the largest number from a given set of N numbers stored in memory. Display the result in AL register.

APPARATUS REQUIRED:

Laptop with Keil Software

PROGRAM:
```
ORG 0000H
MOV R0, #30H
MOV R1, #05H
MOV A, @R0
INC R0
DEC R1
LOOP: MOV B, @R0
      CJNE A, B, CHECK
      SJMP NEXT
CHECK: JNC NEXT     
       MOV A, B     
NEXT: INC R0
      DJNZ R1, LOOP
MOV P1, A           
HERE: SJMP HERE
END
```
OUTPUT:

<img width="1919" height="1145" alt="image" src="https://github.com/user-attachments/assets/1fdbfc5a-8647-4d82-81ca-14ed74c214dd" />


RESULT:
Thus the assembly language program in 8051 to find the largest number from a given set of N numbers stored in memory is executed and displayed the largest in AL register.



