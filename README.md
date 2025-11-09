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
| 2000:34                 |2000:67                   |
| 2001:12                 |2005:24                   |
| 2002:33                 |2006:00                   |
| 2003:12                 |                          |

#### Manual Calculations

![add out](https://github.com/user-attachments/assets/a751eda2-a1c0-44d4-9615-0a4351e6e521)

---

<img width="629" height="418" alt="ADD" src="https://github.com/user-attachments/assets/112c147b-7d15-4071-abf0-f1b1e7d6ec90" />

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
| 2000:46                 |2000:01                   |
| 2001:AD                 |2005:6C                   |
| 2002:45                 |2006:00                   |
| 2003:41                 |                          |

#### Manual Calculations

![sub out](https://github.com/user-attachments/assets/7bfbf98d-162d-42a3-a5ac-14da27ca3b9a)

---


<img width="624" height="418" alt="SUB" src="https://github.com/user-attachments/assets/90e68dbe-e0c6-4a8f-92cc-3dd1414c92a2" />

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
| 2000:22                 |2000:C6                   |
| 2001:22                 |2005:92                   |
| 2002:33                 |2006:D3                   |
| 2003:33                 |2007:06                   |

#### Manual Calculations

![mul out](https://github.com/user-attachments/assets/3fdd8148-ce96-4803-9a73-0b3ebf6f8a99)

---

<img width="629" height="419" alt="MUL" src="https://github.com/user-attachments/assets/ae08b577-9290-4cef-97c5-fef2291e4e34" />

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
| 2000:26                 |2000:02                   |
| 2001:72                 |2005:00                   |
| 2002:13                 |2006:00                   |
| 2003:36                 |2007:00                   |

#### Manual Calculations

![div out](https://github.com/user-attachments/assets/755d0b3f-7e60-4191-a57b-31e4b6140e4b)

---
<img width="626" height="420" alt="DIV" src="https://github.com/user-attachments/assets/67480c92-c579-4e80-abb9-6e4a0e8862ee" />



## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.

