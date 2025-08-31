# Arithmetic-operation-using-8086
# 8086 Assembly Language Programs for Arithmetic Operations

## AIM

To write and execute Assembly Language Programs to perform arithmetic operations for the 8086 microprocessor.

---

## APPARATUS REQUIRED

* Personal Computer with MASM Software

---

## 1. ADDITION

#### Algorithm

1. Initialize memory location in HL register.
2. Store 1st data.
3. Increment HL to enter 2nd data.
4. Move 2nd number to accumulator.
5. Decrement HL.
6. Add value in memory with accumulator.
7. Store result.
8. Stop.


## FLOW CHART
<img width="707" height="1024" alt="image" src="https://github.com/user-attachments/assets/b5a7062d-e294-47cd-9683-a40de25e82de" />


#### Program

c

#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|  1200h                  |   1204h                  |
|  1201h                  |   1205h                  |
|  1202h                  |   1206h                  |
|  1203h                  |   -                      |

#### Manual Calculations

-![WhatsApp Image 2025-08-24 at 19 35 59_62582549](https://github.com/user-attachments/assets/68fd6627-76c7-48e1-b1ff-adad70e59a3a)
--

## OUTPUT IMAGE FROM MASM SOFTWARE
![WhatsApp Image 2025-08-24 at 22 03 22_1eb5cea3](https://github.com/user-attachments/assets/fedd32fd-7c10-4c21-bc27-1e750efa2d74)
![WhatsApp Image 2025-08-24 at 22 03 16_b25a7881](https://github.com/user-attachments/assets/71cdef92-8ef4-4ef6-b723-1cbb6a2ceeb4)



## 2. SUBTRACTION

#### Algorithm

1. Initialize memory and store 1st data.
2. Increment to get 2nd data.
3. Move 2nd data to accumulator.
4. Subtract memory content.
5. Store result.

## FLOWCHART

<img width="578" height="797" alt="image" src="https://github.com/user-attachments/assets/564c3c7a-33ce-4a1c-8920-beb5c24b9b47" />


#### Program
```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV CL,00H
MOV AX,[SI]
MOV BX,[SI+02H]
SUB AX,BX
JNC L1
INC CL
L1:
MOV [SI+04H],AX
MOV [SI+06H],CL
MOV AH,4CH
INT 21H
CODE ENDS
END
```


#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
| 1200h                   | 1204h                    |
| 1201h                   | 1205h                    |
| 1202h                   | 1206h                    |
| 1203h                   | -                        |

#### Manual Calculations

![WhatsApp Image 2025-08-24 at 22 24 32_53a08d4c](https://github.com/user-attachments/assets/3b3ad349-b542-4ec6-b272-acced53d4c1c)
---


## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="640" height="480" alt="Screenshot (42)" src="https://github.com/user-attachments/assets/f8ca23cd-0dca-44f5-8266-610aa9dcac9b" />
<img width="640" height="480" alt="Screenshot (41)" src="https://github.com/user-attachments/assets/05c5be7d-0572-4137-bbaa-b394e4967ff7" />


## 3. MULTIPLICATION

#### Algorithm

1. Initialize memory and store operands.
2. Move operands to registers.
3. Multiply.
4. Store result.

##FLOWCHART

<img width="569" height="906" alt="image" src="https://github.com/user-attachments/assets/88be88ff-2896-4a88-b73d-84ccffd2fcf9" />



#### Program

```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV DX,0000H
MOV AX,[SI]
MOV BX,[SI+02H]
MUL BX
MOV [SI+04H],AX
MOV [SI+06H],DX
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|   1200h                  |   1204h                 |
|   1201h                  |   1205h                 |    |
|   1202h                  |   1206h                 |
|   1203h                  |   1207h                 |
#### Manual Calculations


![WhatsApp Image 2025-08-24 at 23 05 26_80511084](https://github.com/user-attachments/assets/642c537f-f5fd-4960-849d-fc030333ac4f)

---

## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="640" height="480" alt="Screenshot (43)" src="https://github.com/user-attachments/assets/7fc3acc2-fd95-4d5c-acf6-381fe7e3f406" />

<img width="640" height="480" alt="Screenshot (44)" src="https://github.com/user-attachments/assets/08c547c2-3ac3-45e1-b3d1-be41629cf92f" />

## 4. DIVISION

#### Algorithm

1. Load memory location of operands.
2. Perform division.
3. Store result.

   ## FLOWCHART
<img width="1065" height="802" alt="image" src="https://github.com/user-attachments/assets/25b4a483-0d42-494b-8639-1af3ea17191b" />


#### Program

```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV DX,0000H
MOV AX,[SI]
MOV BX,[SI+02H]
DIV BX
MOV [SI+04H],AX
MOV [SI+06H],DX
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|  1200h                  |   1204h                 |
|  1201h                  |   1205h                 |
|  1202h                  |   1206h                 |
|  1203h                  |   1207h                 |
#### Manual Calculations

![WhatsApp Image 2025-08-24 at 23 44 43_13224b42](https://github.com/user-attachments/assets/c1a72e79-993e-46b5-bd46-2025fd1a482e)


---
## OUTPUT FROM MASM SOFTWARE
<img width="640" height="480" alt="Screenshot (46)" src="https://github.com/user-attachments/assets/39196e16-074e-45c5-b8ee-9618e8705e2e" />

<img width="640" height="480" alt="Screenshot (45)" src="https://github.com/user-attachments/assets/363a173c-b462-48cb-9616-f70e8bd1f911" />

## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.
