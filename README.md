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

|                         MEMORY LOCATION (INPUT)                                                                                  |                                    MEMORY LOCATION (OUTPUT) |
| ---------------------------------------------------------------------------------------------------------------------------------|------------------------ |
|![WhatsApp Image 2025-09-01 at 22 33 51_0a7be4e3](https://github.com/user-attachments/assets/98f3c1f3-bac6-4ed8-a463-63d6daeef7b6)| ![WhatsApp Image 2025-09-01 at 22 33 51_db4574a8](https://github.com/user-attachments/assets/872e2c18-7382-47e8-818a-65111630a428)
           |

#### Manual Calculations

![WhatsApp Image 2025-09-01 at 22 35 16_98938c53](https://github.com/user-attachments/assets/1ea82ada-b6ca-4073-9722-b810841c3f9f)

---

## OUTPUT IMAGE FROM MASM SOFTWARE

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



#### Output Table

|                                MEMORY LOCATION (INPUT)                                                                            |                                         MEMORY LOCATION (OUTPUT) |
| ----------------------------------------------------------------------------------------------------------------------------------| ---------------------------------------------------------------- |
| ![WhatsApp Image 2025-09-01 at 22 34 14_1ea544d0](https://github.com/user-attachments/assets/d597bc1d-37cc-49af-a351-c527e3de02b1)|       ![WhatsApp Image 2025-09-01 at 22 34 15_4deb80a9](https://github.com/user-attachments/assets/2ffd8c0d-7992-48bb-a9ce-6b52de401cae)|

#### Manual Calculations

![WhatsApp Image 2025-09-01 at 22 35 16_2dd8d7e1](https://github.com/user-attachments/assets/e73807cf-b4cd-4b81-ba81-384ccf2d5ac3)

---


## OUTPUT SCREEN FROM MASM SOFTWARE

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
|            ![WhatsApp Image 2025-09-01 at 22 34 35_b9cfc232](https://github.com/user-attachments/assets/b66fb3e6-174c-458b-9010-83bc6289afaf)|             ![WhatsApp Image 2025-09-01 at 22 34 35_349d060f](https://github.com/user-attachments/assets/54e48886-5fc7-4cdb-a1b5-1bdb7edd09a6)
             |

#### Manual Calculations

![WhatsApp Image 2025-09-01 at 22 35 16_c2878ece](https://github.com/user-attachments/assets/d6ae8882-bf56-4521-bd08-61883a2f2667)

---

## OUTPUT SCREEN FROM MASM SOFTWARE

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
|             ![WhatsApp Image 2025-09-01 at 22 35 02_6f24adc3](https://github.com/user-attachments/assets/643e92bb-460a-4e74-8ba5-719f176a7424)|              ![WhatsApp Image 2025-09-01 at 22 35 03_1146f5c4](https://github.com/user-attachments/assets/df29203e-855d-4738-9d2d-4cea84ffd248)|

#### Manual Calculations

![WhatsApp Image 2025-09-01 at 22 35 15_fbc19295](https://github.com/user-attachments/assets/4cf2a840-7ea0-4d58-b772-8e5f504f3bb7)

## OUTPUT FROM MASM SOFTWARE

## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.
