# Python-Parser-and-Compiler

Wrote a grammar that recognizes the statements described below and generated its lexical analyzer and parser. 
After obtaining the lexical analyzer and the parser, all the action routines needed to evaluate a given python code were written.

# Tools
1-ASM, to write the grammar.

2-Java, to write the action routines.

3-Eclipse

# Note
Please find the document file in the project for a better description of the project

# Input-Example-Of-The-Grammar
L1 = ['hello', 'everybody', 'from', 'aub']	print(L1)  

L2 = ['hello', 55, 'from', L1]			print(L2)

L2[2] = 'to'				print(L2)

L3 = ['333', 33, 3]				print(L3)

L4 = ['444', 44, 4]				print(L4)

L3 = L1 + L2				print(L3)

L5 = L1 + L2 + L3 + L4			print(L5)

L6 = L5[3:7]				print(L6)

L7 = L5[:6]				print(L7)

L8 = L5[3:]				print(L8)

L9 = [1, 2, 3, 4, 5, 6, 7, 8, 9]

c1=[for x in L9 	if (x > 4)]			print(c1)

c2=[for x in L9 	if (5 == 2)]		print(c2)

c3=[for x in L9 	if (5 > x)]			print(c3)

c4=[for x in L9 	if (x == x)]		print(c4)

c5=[for x in L9 	if not (x == 4)]		print(c5)

c6=[for x in L9 	if (x != 4)]		print(c6)

c7=[for y in L9 	if (x != 4)]		print(c7)

c8=[for x in L9 	if (7 != y)]		print(c8)

c10=[for x in L9 if ( ( ((x > 2) and (7 > x)) or (x == 9) ) and (x > 5) )] 		print(c10)

c11=[for x in L9 if ( ( ((x > 2) and (7 > x)) or not(x == 9) ) and (x > 5) )] 		print(c11)

c12=[for x in L9 if ( ( not ((x > 2) and (7 > x)) or not(x == 9) ) and (x > 5) ) ] 	print(c12)

# Output-Example-of-the-input-above-and-the-action-routines\
L1 is ['hello', 'everybody', 'from', 'aub']

L2 is ['hello', 55, 'from', L1]

L2 is ['hello', 55, 'to', L1]

L3 is ['333', 33, 3]

L4 is ['444', 44, 4]

L3 is ['hello', 'everybody', 'from', 'aub', 'hello', 55, 'to', L1]

L5 is ['hello', 'everybody', 'from', 'aub', 'hello', 55, 'to', L1, 'hello', 'everybody', 'from', 'aub', 'hello', 55, 'to', L1, '444', 44, 4]

L6 is ['aub', 'hello', 55, 'to']

L7 is ['hello', 'everybody', 'from', 'aub', 'hello', 55]

L8 is ['aub', 'hello', 55, 'to', L1, 'hello', 'everybody', 'from', 'aub', 'hello', 55, 'to', L1, '444', 44]

c1 is [5, 6, 7, 8, 9]

c2 is []

c3 is [1, 2, 3, 4]

c4 is [1, 2, 3, 4, 5, 6, 7, 8, 9]

c5 is [1, 2, 3, 5, 6, 7, 8, 9]

c6 is [1, 2, 3, 5, 6, 7, 8, 9]

Unknown variable x. Did you mean y

Unknown variable x. Did you mean y

Unknown variable x. Did you mean y

Unknown variable x. Did you mean y

Unknown variable x. Did you mean y

Unknown variable x. Did you mean y

Unknown variable x. Did you mean y

Unknown variable x. Did you mean y

Unknown variable x. Did you mean y

c7 is []

Unknown variable y. Did you mean x

Unknown variable y. Did you mean x

Unknown variable y. Did you mean x

Unknown variable y. Did you mean x

Unknown variable y. Did you mean x

Unknown variable y. Did you mean x

Unknown variable y. Did you mean x

Unknown variable y. Did you mean x

Unknown variable y. Did you mean x

c8 is []

c10 is [6, 9]

c11 is [6, 7, 8]

c12 is [6, 7, 8, 9]
