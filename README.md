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
|  1200                   |     32                   |
|  1201                   |     67                   |
|  1202                   |     15                   |
|  1203                   |     27                   |
|  1204                   |     47                   |
|  1205                   |     8E                   |
|1206|00|
#### Manual Calculations

![WhatsApp Image 2025-09-17 at 21 44 46_708d1e8a](https://github.com/user-attachments/assets/3b945fdd-d501-48d6-b65c-dcf6301b7d2d)




---

## OUTPUT IMAGE FROM MASM SOFTWARE


<img width="638" height="416" alt="Screenshot 2025-10-23 130006" src="https://github.com/user-attachments/assets/ca8b90d0-7d9c-449b-ad76-ca043893e2d5" />



<img width="633" height="414" alt="Screenshot 2025-10-23 130247" src="https://github.com/user-attachments/assets/07123e68-6a06-47b4-947b-064a5aac3dff" />

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
|  1200                   |  45                      |
|  1201                    |67|
| 1202|31|
|1203|23|
|1204|14|
|1205|44|
|1206|00|

#### Manual Calculations

![WhatsApp Image 2025-09-17 at 21 49 48_70216624](https://github.com/user-attachments/assets/941ac0f8-9568-4e9c-ab52-8c61ef3f2cb7)

---


## OUTPUT SCREEN FROM MASM SOFTWARE




<img width="643" height="419" alt="Screenshot 2025-10-23 130540" src="https://github.com/user-attachments/assets/ab61a531-5c0b-410c-b65e-1819e5bfe01c" />

<img width="640" height="416" alt="Screenshot 2025-10-23 130512" src="https://github.com/user-attachments/assets/4f8ec413-4aef-4f90-81af-411325cdc8e4" />

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
|    1200                     |    12                      |
|1201|34|
|1202|12|
|1203|34|
|1204|44|
|1205|51|
|1206|97|
|1207|0A|

#### Manual Calculations

![WhatsApp Image 2025-09-17 at 22 07 20_c7059d49](https://github.com/user-attachments/assets/102f7bc5-5447-4e91-9fe0-c0bbfd5e078f)



---

## OUTPUT SCREEN FROM MASM SOFTWARE



<img width="634" height="415" alt="Screenshot 2025-10-23 131107" src="https://github.com/user-attachments/assets/cc24c97a-6bd7-4e15-b6de-2a95cb5e9edb" />


<img width="646" height="423" alt="Screenshot 2025-10-23 131039" src="https://github.com/user-attachments/assets/7ced7096-4fd9-49cc-8c5a-d6e8949313c7" />


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
|   1200                      |              12            |
|1201|34|
|1202|12|
|1203|34|
|1204|01|
|1205|00|
|1206|00|
|1207|00|
#### Manual Calculations

![WhatsApp Image 2025-09-17 at 22 12 57_8dbbe35f](https://github.com/user-attachments/assets/660bdc37-179d-47a5-ae0b-37973f0eae6d)


---
## OUTPUT FROM MASM SOFTWARE

<img width="637" height="420" alt="Screenshot 2025-10-23 131344" src="https://github.com/user-attachments/assets/3a99bd4d-4a8c-4084-92b9-736dc6dd2fdc" />


<img width="637" height="414" alt="Screenshot 2025-10-23 131321" src="https://github.com/user-attachments/assets/638e8381-0cd4-43f1-bf6e-d94664372c08" />

## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.

