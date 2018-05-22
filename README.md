# 8085Kaleidoscope
This contains files 8085 
Made by 
Priyanshu Pandey 130/EC/15
Nishant Arora 110/EC/15

# ORG 0000
	   JMP 1000
# ORG 1000
	   MVI B,07
	   MVI C,C0
	   MVI A,FF
	   OUT 84
	   OUT 85

LOOP:	   MVI A,C3
	   OUT 80
	   IN 83
	   ANI 07
	   CMP B
	   JZ LOOP
           MVI D,FFH
DELAY:     MVI E,FFH
DELAY1:    DCR E
           JNZ DELAY1
           DCR D
           JNZ DELAY            
	   MOV B,A
	   MVI A,43
	   OUT 80
	   IN 84
	   RLC
	   RLC
	   RLC
	   OUT 81
	   IN 85
	   OUT 82
	   MVI A,C3
	   OUT 80
	   JMP LOOP
	   HLT
