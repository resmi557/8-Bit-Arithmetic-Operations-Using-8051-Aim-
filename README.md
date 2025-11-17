# 8-Bit-Arithmetic-Operations-Using-8051

## Aim:
To perform 8-bit arithmetic operations such as addition, subtraction, multiplication, and division using the 8051 microcontroller.

## Apparatus Required:

•	Laptop with Keil uVision software

## Algorithm:

## For Addition:
1.	Load the first number from memory location 30H into register A.
2.	Load the second number from memory location 31H into register B.
3.	Add the contents of registers A and B.
4.	Store the result in memory location 40H.
5.	Store the carry (if any) in 41H.

## Program:
```
ORG 0000H
MOV A, 30H     
ADD A, 31H    
MOV 40H, A 
JNC NEXT 
MOV 41H, #01H
SJMP END_PROGRAM
NEXT: MOV 41H, #00H
END_PROGRAM: NOP
END
```


## Output:
<img width="1919" height="1140" alt="image" src="https://github.com/user-attachments/assets/37e639ce-8748-4876-bbd9-279a7bf6088a" />
<img width="1919" height="1139" alt="image" src="https://github.com/user-attachments/assets/6b712024-f443-4cbf-bb82-8477f37e25ff" />


   
## For Subtraction:
1.	Load the first number from memory location 30H into register A.
2.	Load the second number from memory location 31H into register B.
3.	Subtract B from A.
4.	Store the result in memory location 40H.

## Program:
```
ORG 0000H
MOV A, 30H
SUBB A, 31H
MOV 40H, A
JNC NEXT
MOV 41H, #01H
SJMP END_PROGRAM
NEXT: MOV 41H, #00H
END_PROGRAM: NOP
END
```


## Output:
<img width="1919" height="1140" alt="image" src="https://github.com/user-attachments/assets/48e3079c-38a0-4a07-ae1d-c0630a1c01c6" />
<img width="1919" height="1139" alt="image" src="https://github.com/user-attachments/assets/5867b1b5-edb5-416a-baa6-96c22c304d57" />



## For Multiplication:
1.	Load the first number from memory location 30H into register A.
2.	Load the second number from memory location 31H into register B.
3.	Multiply A and B.
4.	Store the lower byte of the result in memory location 40H.
5.	Store the higher byte of the result in memory location 41H.

## Program:
```
ORG 0000H
MOV A, 30H 
MOV B, 31H
MUL AB
MOV 40H, A 
MOV 41H, B
END
```


## Output:
<img width="1918" height="1137" alt="image" src="https://github.com/user-attachments/assets/803501b2-f9c2-4e8e-b985-cc71508d9c02" />
<img width="1919" height="1137" alt="image" src="https://github.com/user-attachments/assets/8afbf9b8-690d-4919-839f-9846abe75d3a" />


## For Division:
1.	Load the dividend from memory location 30H into register A.
2.	Load the divisor from memory location 31H into register B.
3.	Divide A by B.
4.	Store the quotient in memory location 40H.
5.	Store the remainder in memory location 41H.


## Program:
```
ORG 0000H
MOV A, 30H
MOV B, 31H
DIV AB
MOV 40H, A
MOV 41H, B 
END
```



## Output:
<img width="1918" height="1135" alt="image" src="https://github.com/user-attachments/assets/f3516d43-4b97-4c3a-b8cf-d0d6505ee863" />
<img width="1915" height="1135" alt="image" src="https://github.com/user-attachments/assets/9be63997-ba60-45aa-be4d-fa1e88f673c8" />




## Result:

The 8-bit arithmetic operations using the 8051 microcontroller have been successfully executed and verified using Keil software.



