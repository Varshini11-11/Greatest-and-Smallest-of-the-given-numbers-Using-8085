# Greatest-and-Smallest-of-the-given-numbers-Using-8085

## Aim:

To write 8085 microprocessor programs to find the greatest and smallest number from the given 8-bit numbers.

## Apparatus Required:

•	Laptop with an internet connection

## Finding the Greatest Number

## Algorithm:

1.	Load the count of numbers from memory location 4200H into register C.
2.	Load the first number from 4201H into register A (Assume it as the greatest).
3.	Load the next number and compare it with A.
4.	If the new number is greater, update A.
5.	Repeat the process for all numbers.
6.	Store the greatest number in 4300H.

## Program:
```
CMC
LDA 4200H
MOV C,A
LXI H,4201H
MOV A,M
INX H
DCR C
LOOP: CMP M
JNC NEXT
MOV A,M
NEXT: INX H
DCR C
JNZ LOOP
STA 4300H
HLT
```
## Output:
<img width="1920" height="1140" alt="image" src="https://github.com/user-attachments/assets/ef356f24-0f44-47ec-8614-a55e01babad3" />
<img width="298" height="373" alt="image" src="https://github.com/user-attachments/assets/26193c08-1290-4d09-b3e0-6754983a462d" />

## Finding the Smallest Number

## Algorithm:

1.	Load the count of numbers from memory location 4200H into register C.
2.	Load the first number from 4201H into register A (Assume it as the smallest).
3.	Load the next number and compare it with A.
4.	If the new number is smaller, update A.
5.	Repeat the process for all numbers.
6.	Store the smallest number in 4301H.

## Program:
```
CMC
LDA 4200H;
MOV C,A ;
LXI H,4201H;
MOV A,M ;
INX H;
DCR C ;
LOOP: CMP M;
JC NEXT;
MOV A,M ;
NEXT:INX H;
DCR C ;
JNZ LOOP;
STA 4301H;
HLT;
```

## Output:
<img width="1920" height="1140" alt="image" src="https://github.com/user-attachments/assets/834a766b-6dc2-40ee-bb87-6f5f0e998d17" />
<img width="306" height="380" alt="image" src="https://github.com/user-attachments/assets/b0f8373f-aa67-4641-87ae-68ac28b2eb61" />


## Result:

The 8085 microprocessor successfully finds the greatest and smallest numbers from multiple inputs and stores them in memory.
