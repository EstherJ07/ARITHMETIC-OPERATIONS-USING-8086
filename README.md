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

```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV CL,00H
MOV AX,[SI]
MOV BX,[SI+02H]
ADD AX,BX
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
| 2000 = 12               | 2004 = 24                |
| 2001 = 34               | 2005 = 68                |
| 2002 = 12               |                          |
| 2003 = 34               |                          |

#### Manual Calculations

![manual1](https://github.com/user-attachments/assets/882c6b7b-b8cb-4cf0-ba25-3345401e8e98)

## OUTPUT IMAGE FROM MASM SOFTWARE
![output1](https://github.com/user-attachments/assets/5c33a9bf-e979-478d-afc6-cad7a1dcd89a)

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
| 2000 = 56               | 2004 = 44                |
| 2001 = 78               | 2005 = 31                |
| 2002 = 25               |                          |
| 2003 = 34               |                          |

#### Manual Calculations
![manual2](https://github.com/user-attachments/assets/ac1160ef-7797-4ce3-977c-b6e1be8a0c42)

## OUTPUT SCREEN FROM MASM SOFTWARE
![output2](https://github.com/user-attachments/assets/40c71495-452b-4c21-a00a-039162e90c2c)

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
|  2000 = 12              | 2004 = 90                |
|  2001 = 34              | 2005 = 5A                |
|  2002 = 12              |                          |
|  2003 = 34              |                          |

#### Manual Calculations
![manual3](https://github.com/user-attachments/assets/7eb595fb-8d60-4fc8-9eba-7696cd1e4529)

## OUTPUT SCREEN FROM MASM SOFTWARE
![output3](https://github.com/user-attachments/assets/067bc4c4-c4d8-4a44-8f91-1c271c30a242)

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
| 2000 = 68               | 2004 = 02                |
| 2001 = 24               | 2005 = 00                |
| 2002 = 34               |                          |
| 2003 = 11               |                          |

#### Manual Calculations
![manual4](https://github.com/user-attachments/assets/a97c86b6-7e30-4180-93f4-c8fcf20f6fc2)

## OUTPUT FROM MASM SOFTWARE
![output4](https://github.com/user-attachments/assets/6129a359-27e4-4727-8376-735c41d8d1ff)


## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.

