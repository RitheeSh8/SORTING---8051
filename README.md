
# SORTING---8051

**AIM:**

To write and execute Assembly language Program for sorting of data using 8051 keil.

**APPARATUS REQUIRED: Personal computer with Keil software**

**(i) Descending order ALGORITHM:**

1.	Initialize the register r7 with count.
2.	Get first two elements in two registers.
3.	Compare the two elements of data. If value of R0 register is low, then exchange A & R0 data else increment pointer and decrement register R7.
4.	Check R7 is zero, and then move the register R0 & A.
5.	Again increment pointer and decrement R7,
6.	Check R7 is zero. If no repeat the process from step 2.
7.	Otherwise stop the program.

**PROGRAM:**
```
ORG 0000H 
MOV R7,#4
LOOP1:MOV R0,#40H 
MOV R6,#04
LOOP: MOV A,@R0 
INC R0
MOV 50H,@R0 
CJNE A,50H,NEXT 
SJMP DOWN 
NEXT:JNC DOWN 
MOV @R0,A
DEC R0
MOV @R0,50H 
DOWN:DJNZ R6,LOOP 
DJNZ R7,LOOP1
END
```

**OUTPUT:**

![IMG-20251024-WA0038 1](https://github.com/user-attachments/assets/2d17eb37-40ec-4603-980f-33ba4bc89932)


**MEMORY WINDOW:**

Before execution: D:0x40H:

![075a0e9cc79249d4b9317a2e7707f800 1](https://github.com/user-attachments/assets/53d9df1f-0ccc-47e0-8029-5b92a71f26b2)

After execution: D:0x40H:

![3e33ffc396994d4f9c91dcc76104ddb5 1](https://github.com/user-attachments/assets/0d3424b5-1d28-4549-bae8-16477e27e2cf)


**(ii)	Ascending order**
 
**ALGORITHM:**

1.	Initialize the register r7 with count.
2.	Get first two elements in two registers.
3.	Compare the two elements of data. If value of R0 register is high then exchange A & R0 data else increment pointer and decrement register R7.
4.	Check R7 is zero, and then move the register R0 & A.
5.	Again increment pointer and decrement R7,
6.	Check R7 is zero. If no repeat the process from step 2.
7.	Otherwise stop the program.

**PROGRAM:**

```
ORG 0000H 
MOV R7,#4
LOOP1:MOV R0,#40H
MOV R6,#04
LOOP: MOV A,@R0
INC R0
MOV 50H,@R0 
CJNE A,50H,NEXT
SJMP DOWN 
NEXT:JC DOWN
MOV @R0,A
DEC R0
MOV @R0,50H 
DOWN:DJNZ R6,LOOP 
DJNZ R7,LOOP1
END
```

**OUTPUT:**

![IMG-20251024-WA0036 1](https://github.com/user-attachments/assets/4d4f27e6-af36-490f-af15-3b70f5690a13)

**MEMORY WINDOW:** 

**Before execution:**
D:0x40H:
![76fee0fbf01449159755aee532cf2a49 1](https://github.com/user-attachments/assets/37b0ca37-3560-4636-b9b7-55b2b7c196a2)
After execution:
D:0x40H:
![46865637e288449186dd3d0b9442a690 1](https://github.com/user-attachments/assets/f565d1b3-8f8a-4950-825b-e189bc7d8a6e)

**Result:**

Thus the sorting of given data was done using 8051 keil and shown the output.

