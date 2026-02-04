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
MOV CL,00H
MOV AX,1234H
MOV BX,124H
ADD AX,BX
JNC L1
INC CL
L1:MOV SI,1200H
MOV [SI], AX
MOV [SI+2], CL
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|       1200🔢
|                          |

#### Manual Calculations
<img width="1541" height="969" alt="image" src="https://github.com/user-attachments/assets/78602c1d-a50f-4130-9662-d5f94f3e8381" />


---

## OUTPUT IMAGE FROM MASM SOFTWARE
<img width="639" height="186" alt="image" src="https://github.com/user-attachments/assets/7ee81ba9-272b-4abf-8430-2fa4bfeee6bc" />


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
MOV CL,00H
MOV AX,1234H
MOV BX,124H
SUB AX,BX
JNC L1
INC CL
L1:MOV SI,1200H
MOV [SI], AX
MOV [SI+2], CL
MOV AH,4CH
INT 21H
CODE ENDS
END
```


#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|                         |                          |

#### Manual Calculations

<img width="1600" height="1075" alt="image" src="https://github.com/user-attachments/assets/11e28e3c-c8ff-49cb-9ef4-a070648c3c20" />


---


## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="635" height="148" alt="image" src="https://github.com/user-attachments/assets/c0ff4366-8297-48b0-883a-8e7390b0673b" />


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
|         1201:34         |      68:1205             |
|         1202:12         |      00:1206
|         1203:34         |      c4:1207
#### Manual Calculations
<img width="1009" height="567" alt="image" src="https://github.com/user-attachments/assets/dff2b353-08fc-474f-93e3-f138cfdc9337" />


---

## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="639" height="176" alt="image" src="https://github.com/user-attachments/assets/f137b518-73ff-49e9-9103-d05d3b878037" />


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
|         1201:34         |      68:1205             |
|         1202:12         |      00:1206
|         1203:34         |      c4:1207
#### Manual Calculations
<img width="1027" height="560" alt="image" src="https://github.com/user-attachments/assets/11656504-6710-416f-9bd0-40dd3c2a74fd" />



---
## OUTPUT FROM MASM SOFTWARE
<img width="635" height="172" alt="image" src="https://github.com/user-attachments/assets/fbdcf968-220e-42ce-9352-f023ef90e17a" />




## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.

