Estos son las diferentes cosas en la que nos tenemos que fijar para empezar a programar ensamblador:

+ Registros (palabra de proc)
+ Mapa de direcciones memoria I/O
	+ compartido. chip-set
	+ separado
+ Arquitectura:
	+ Harvad (2 memorias)
	+ Von newman (1 memoria)
+ Memoria:
	+ direcciones fisica.
	+ Direcciones lógicas:
		+ Segmentación 
		+ Paginación 
+ Instrucciones y modos de direccionamiento (En donde o como vamos a manejar o recuperar los datos):
	+ Inmediato (Instruciones):
		- MOV AX, 10  \[asignar datos (a un registro)]
	- Registro
	- Directo a memoria:
		- MOV \[100], AX \[asigna un valor a un espacio de memoria (lógica)]
	- Indirecto a memoria:
		- MOV BX, 100
		- MOV \[BX], AX
	- Base + desplazamiento:
		- MOV BX, 100
		- MOV \[BX + 20], AX
		- En C -> x\[i] = 10; => \*(x + i) = 10;
	- Base + indice:
		- MOV BX, 100
		- MOV \[BX + SI], AX
	-  Base + indice + desplazamiento:
		- MOV BX, 100
		- MOV \[BX + SI + 20], AX
	- Implicito:
		- OUT DX, AH
		

### Instrucciones
+ ARITMETICAS:
	+ ADD
	+ SUB
	+ MUL
	+ DIV
+ LOGICAS
	+ AND
	+ OR
	+ NOT
	+ XOR
+ DESPLAZAMIENTO
	+ ROL
	+ ROR
	+ SHL
	+ SHR
+ TRANSFERENCIA
	+ MOV
	+ IN
	+ OUT

## proceso cero

http://libio.cua.uam.mx/~luis/Codigo/AC23I/ 





| Módulo/Bloque     | Descripción/Operaciones                                                                                                                                           |
| ----------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Unidad de Registros. |  Al menos 8 registros de N = 8 bits. |
| Unidad Aritmética | Suma y resta sobre A y B.  <br>Incremento y decremento en una unidad, y transferencia, tanto para A como para B.                                                  |
| Unidad Lógica     | Operaciones lógicas AND, OR, XOR, NAND, NOR y XNOR sobre A y B.  <br>Operación NOT tanto para A como para B.                                                      |
| Shifter           | Desplazamiento derecha (SHR), desplazamiento izquierda (SHL), rotación derecha (ROR) y rotación izquierda (ROL) de A o de B. Todas las operaciones son de un bit. 


| Operacion       | s2  | s1  | s2  | a   | b   | cin |
| --------------- | --- | --- | --- | --- | --- | --- |
| suma            | 0   | 0   | 0   | a   | b   | 0   |
| resta           | 0   | 0   | 1   | a   | b'  | 1   |
| incremento a    | 0   | 1   | 0   | a   | 0   | 1   |
| incremento b    | 0   | 1   | 1   | 0   | b   | 1   |
| decremento a    | 1   | 0   | 0   | a   | 1   | 0   |
| decremento b    | 1   | 0   | 1   | 1   | b   | 0   |
| transferencia a | 1   | 1   | 0   | a   | 0   | 0   |
| transferencia b | 1   | 1   | 1   | 0   | b   | 0   | 
