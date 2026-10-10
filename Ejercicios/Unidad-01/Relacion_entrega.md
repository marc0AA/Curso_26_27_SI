# Relacion de Ejercicios de Binario y de Puertas Logicas

>TODO CALCULO QUE NO SE VEA REPRESENTADO EN ESTE MD, ESTA HECHO A MANO EN PAPEL (AUNQUE SIEMPRE INTENTO ESCRIBIRLO TODO AUNQUE SEA EN PALABRAS)

>EL APARTADO "D" DEL EJERCICIO 10 ESTA HECHO A MANO Y ESTA SUBIDO AL PROPIO REPOSITORIO DE GIT 

> @autor: Marco

## Relacion 05

### Ejercicio 1

- Apartado a: 245,3 en base 6 es 101,5 en decimal. Cada cifra se multiplica por 6 elevado a su posición:

  - 2 x 6 al cuadrado = 2 x 36 = 72
  - 4 x 6 = 24
  - 5 x 1 = 5
  - 3 x 6 a la menos 1 = 3 / 6 = 0,5

  Sumo todo: 72 + 24 + 5 + 0,5 = 101,5

- Apartado b: 1001111,001 en base 2 es 79,125 en decimal. Cada cifra se multiplica por 2 elevado a su posición. Las cifras que valen 0 no suman nada, así que solo cuento los unos:

  - 1 x 64 = 64
  - 1 x 8 = 8
  - 1 x 4 = 4
  - 1 x 2 = 2
  - 1 x 1 = 1
  - 1 x 0,125 = 0,125

  Sumo todo: 64 + 8 + 4 + 2 + 1 + 0,125 = 79,125

### Ejercicio 2

- Apartado a: 228,5625 en binario es 11100100,1001, en octal 344,44 y en hexadecimal E4,9.

  El metodo de las bombillas consiste en tener una fila de bombillas, cada una con su peso (una potencia de 2). Una bombilla encendida vale 1 y una apagada vale 0. Voy de izquierda a derecha y, si el peso de la bombilla cabe en lo que me queda por representar, la enciendo y se lo resto. Si no cabe, la dejo apagada.

  Parte entera (228), con 8 bombillas:

  - 128: cabe en 228, la enciendo. Quedan 228 - 128 = 100
  - 64: cabe en 100, la enciendo. Quedan 100 - 64 = 36
  - 32: cabe en 36, la enciendo. Quedan 36 - 32 = 4
  - 16: no cabe en 4, apagada
  - 8: no cabe en 4, apagada
  - 4: cabe en 4, la enciendo. Quedan 4 - 4 = 0
  - 2: apagada
  - 1: apagada

  Las bombillas, de 128 a 1, quedan: encendida, encendida, encendida, apagada, apagada, encendida, apagada, apagada. Es decir, 1 1 1 0 0 1 0 0, que es 11100100.

  Parte fraccionaria (0,5625), con 4 bombillas de pesos fraccionarios:

  - 0,5: cabe en 0,5625, la enciendo. Quedan 0,5625 - 0,5 = 0,0625
  - 0,25: no cabe en 0,0625, apagada
  - 0,125: no cabe en 0,0625, apagada
  - 0,0625: cabe en 0,0625, la enciendo. Quedan 0

  Las bombillas, de 0,5 a 0,0625, quedan: encendida, apagada, apagada, encendida. Es decir, 1 0 0 1

  Resultado en binario: 11100100,1001

  Para pasarlo a octal agrupo de 3 en 3 desde la coma, completando con ceros: 011 100 100 , 100 100. Cada grupo es una cifra octal (3, 4, 4 , 4, 4), así que en octal es 344,44.

  Para pasarlo a hexadecimal agrupo de 4 en 4 desde la coma: 1110 0100 , 1001. Cada grupo es una cifra hexadecimal (E, 4 , 9), así que en hexadecimal es E4,9.

- Apartado b: 23,6 en binario con 6 bits fraccionarios es 10111,100110. No es exacto, y el error es 0,0062

  Parte entera: 23 = 16 + 4 + 2 + 1, que en binario es 10111

  Parte fraccionaria: multiplico por 2 y me quedo con la parte entera de cada resultado

  - 0,6 x 2 = 1,2, bit 1
  - 0,2 x 2 = 0,4, bit 0
  - 0,4 x 2 = 0,8, bit 0
  - 0,8 x 2 = 1,6, bit 1
  - 0,6 x 2 = 1,2, bit 1
  - 0,2 x 2 = 0,4, bit 0

  Los bits son 100110, así que el resultado es 10111,100110

  No es exacto porque el 0,6 en binario se repite sin fin (0,1001 1001 1001...) y con 6 bits solo se puede aproximar. El valor que realmente se guarda es 100110 en binario = 32 + 4 + 2 = 38, y 38 / 64 = 0,59375, es decir 23,59375. El error es 23,6 - 23,59375 = 0,00625.

### Ejercicio 3

- Apartado a: 9A9,D en hexadecimal es 4651,64 en octal

  Primero a binario, cada cifra hexadecimal son 4 bits: 9 = 1001, A = 1010, 9 = 1001 y D = 1101. Queda 100110101001,1101

  Ahora agrupo de 3 en 3 desde la coma: 100 110 101 001 , 110 100. Cada grupo es una cifra octal (4, 6, 5, 1 , 6, 4), así que el resultado es 4651,64

- Apartado b: 1706 en octal es 3C6 en hexadecimal

  Primero a binario, cada cifra octal son 3 bits: 1 = 001, 7 = 111, 0 = 000 y 6 = 110. Queda 001111000110, que es 1111000110

  Ahora agrupo de 4 en 4 desde la derecha: 0011 1100 0110. Cada grupo es una cifra hexadecimal (3, C, 6), así que el resultado es 3C6

### Ejercicio 4

- Apartado a: 100001,01 + 111010,01 = 1011011,10

  Voy sumando de derecha a izquierda:

  - 1 + 1 = 0, llevo 1
  - 0 + 0 + 1 = 1
  - 1 + 0 = 1
  - 0 + 1 = 1
  - 0 + 0 = 0
  - 0 + 1 = 1
  - 0 + 1 = 1
  - 1 + 1 = 0, llevo 1
  - La llevada final es 1

  Comprobación en decimal: 33,25 + 58,25 = 91,5, y 1011011,1 es 64 + 16 + 8 + 2 + 1 + 0,5 = 91,5. Correcto

- Apartado b: 1010101,1 - 1010,001 = 1001011,011

  Igualo el número de decimales: 1010101,100 - 0001010,001 = 1001011,011

  En los decimales, 100 - 001 hay que pedir prestado al bit de la izquierda y sale 011. En la parte entera hay que pedir prestado en los bits de las posiciones 1 y 3

  Comprobación en decimal: 85,5 - 10,125 = 75,375, y 1001011,011 es 75 + 0,375 = 75,375. Correcto

### Ejercicio 5

- Apartado a: -72 en 8 bits es 11001000 en signo y magnitud, 10110111 en complemento a 1 y 10111000 en complemento a 2

  72 en binario con 8 bits es 01001000

  - Signo y magnitud: 11001000 (bit de signo 1 y la magnitud 72)
  - Complemento a 1: 10110111 (invierto todos los bits de 72)
  - Complemento a 2: 10111000 (complemento a 1 más 1)

- Apartado b: 106 - 107 = -1 (resultado 11111111 en complemento a 2)

  106 = 01101010 y 107 = 01101011

  Complemento a 2 de 107: invierto (10010100) y sumo 1, queda 10010101

  Ahora sumo: 01101010 + 10010101 = 11111111

  El resultado empieza por 1, así que es negativo. Para ver su valor hago el complemento a 2 otra vez: invierto 00000000 y sumo 1 y sale 00000001, es decir 1. Por tanto el resultado es -1, que coincide con 106 - 107

- Apartado c: 44 + 28 = 72 (resultado 01001000). No hay desbordamiento

  44 = 00101100 y 28 = 00011100

  Sumo: 00101100 + 00011100 = 01001000

  Sumo dos números positivos y el resultado también es positivo (empieza por 0). Además 72 cabe en 8 bits, porque el rango en complemento a 2 va de -128 a 127

- Apartado d: (-106) + 107 = +1 (resultado 00000001 en signo y magnitud)

  -106 = 11101010 y 107 = 01101011

  Regla: cuando los signos son distintos, se restan las magnitudes (la mayor menos la menor) y el resultado lleva el signo del número que tiene mayor magnitud

  107 - 106 = 1. El de mayor magnitud es 107, que es positivo, así que el resultado es positivo: 00000001

### Ejercicio 6

- Solución: 2,25 - 3,25 = 1111,0000, que es -1. Con 8 bits en complemento a 2, 4 para la parte entera y 4 para la fraccionaria

  2,25 = 0010,0100 y 3,25 = 0011,0100

  Complemento a 2 del sustraendo (3,25): invierto y sumo 1 en el último bit

  - 0011,0100 invertido = 1100,1011
  - 1100,1011 + 0000,0001 = 1100,1100

  Ahora sumo: 0010,0100 + 1100,1100 = 1111,0000

  Empieza por 1, así que es negativo. Hago el complemento a 2 para ver el valor: invierto (0000,1111) y sumo 1 (0001,0000), que es 1. Por tanto el resultado es -1

  Comprobación: 2,25 - 3,25 = -1. Correcto

### Ejercicio 7

- Apartado a: 11010 x 101 = 10000010, que es 130

  El multiplicador 101 tiene un 1 en la posición 2 y otro en la posición 0. Por cada 1 desplazo el multiplicando y luego sumo

  - 11010 desplazado 2 posiciones = 1101000
  - 11010 sin desplazar = 0011010

  Sumo: 1101000 + 0011010 = 10000010

  Comprobación: 26 x 5 = 130. Correcto

- Apartado b: 1110,11 x 101 = 1001001,11

  Multiplico sin tener en cuenta la coma: 111011 x 101. Hay 2 decimales en total

  - 111011 desplazado 2 posiciones = 11101100
  - 111011 sin desplazar = 00111011

  Sumo: 11101100 + 00111011 = 100100111

  Coloco la coma dejando 2 decimales: 1001001,11

  Comprobación: 14,75 x 5 = 73,75, y 1001001,11 es 64 + 8 + 1 + 0,75 = 73,75. Correcto

- Apartado c: 10110101 desplazado 2 a la izquierda (10 bits) es 1011010100, y desplazado 3 a la derecha es 00010110

  Lo trato como un número sin signo, que vale 181

  Desplazar 2 posiciones a la izquierda con 10 bits: 0010110101 pasa a 1011010100. Equivale a multiplicar por 4 (2 al cuadrado). 181 x 4 = 724 y 1011010100 vale 724. No se pierde nada porque caben los 10 bits

  Desplazar 3 posiciones a la derecha: 10110101 pasa a 00010110. Equivale a dividir entre 8 (2 al cubo) quedándome solo con la parte entera. 181 / 8 = 22,625, y el resultado es 22 (10110). Se pierden los 3 bits de la derecha (101, que es 5), que correspondían a la parte decimal 0,625

### Ejercicio 8

- Solución: Windows muestra unos 465,66 GB, la diferencia es del 6,87 % y caben 310 vídeos de 1,5 GiB

  Los fabricantes usan GB decimales (1 GB = 1.000.000.000 bytes), pero Windows calcula en GiB (1 GiB = 1.073.741.824 bytes) y los muestra como GB

  - Capacidad que muestra Windows: 500.000.000.000 / 1.073.741.824 = 465,66
  - Diferencia: 500 - 465,66 = 34,34, y 34,34 / 500 = 0,0687, es decir 6,87 %
  - Vídeos de 1,5 GiB: 465,66 / 1,5 = 310,44, caben 310

### Ejercicio 9

- Solución: S = NOT (A OR B) OR NOT C, y vale 1 en las combinaciones ABC = 000, 001, 010, 100 y 110

  El circuito tiene tres puertas en dos niveles:

  - Primer nivel, arriba: una puerta NOR (OR con círculo en la salida) con entradas A y B. Su salida la llamo P
  - Primer nivel, abajo: una puerta NOT con entrada C. Su salida la llamo Q
  - Segundo nivel: una puerta OR con entradas P y Q. Su salida es S

  Es decir, P = NOT (A OR B), Q = NOT C y S = P OR Q. También se puede escribir como (NOT A AND NOT B) OR NOT C

  Tabla de verdad con las salidas intermedias, una línea por combinación de A, B y C:

  - A=0, B=0, C=0: P=1, Q=1, S=1
  - A=0, B=0, C=1: P=1, Q=0, S=1
  - A=0, B=1, C=0: P=0, Q=1, S=1
  - A=0, B=1, C=1: P=0, Q=0, S=0
  - A=1, B=0, C=0: P=0, Q=1, S=1
  - A=1, B=0, C=1: P=0, Q=0, S=0
  - A=1, B=1, C=0: P=0, Q=1, S=1
  - A=1, B=1, C=1: P=0, Q=0, S=0

### Ejercicio 10

- Apartado a: tabla de verdad, S vale 1 solo en las combinaciones 1, 2, 3, 4 y 5

  - Combinación 0 (A=0, B=0, C=0): S=0
  - Combinación 1 (A=0, B=0, C=1): S=1
  - Combinación 2 (A=0, B=1, C=0): S=1
  - Combinación 3 (A=0, B=1, C=1): S=1
  - Combinación 4 (A=1, B=0, C=0): S=1
  - Combinación 5 (A=1, B=0, C=1): S=1
  - Combinación 6 (A=1, B=1, C=0): S=0
  - Combinación 7 (A=1, B=1, C=1): S=0

- Apartado b: expresión canónica (suma de productos), un término por cada combinación en la que S vale 1

  S = (NOT A AND NOT B AND C) OR (NOT A AND B AND NOT C) OR (NOT A AND B AND C) OR (A AND NOT B AND NOT C) OR (A AND NOT B AND C)

- Apartado c: simplificada, S = (NOT A AND B) OR (A AND NOT B) OR (NOT A AND C)

  Mapa de Karnaugh de 2 filas (A) por 4 columnas (BC en orden 00, 01, 11, 10). La fila A=0 vale 0, 1, 1, 1 y la fila A=1 vale 1, 1, 0, 0

  Agrupaciones:

  - Casillas 2 y 3 (A=0 y B=1): da NOT A AND B. Es obligatoria porque la casilla 2 solo se puede cubrir así
  - Casillas 4 y 5 (A=1 y B=0): da A AND NOT B. Es obligatoria porque la casilla 4 solo se puede cubrir así
  - Falta la casilla 1 (001). La cubro con las casillas 1 y 3 (A=0 y C=1): da NOT A AND C

  Comprobación: en 000, 110 y 111 ninguno de los tres términos vale 1, así que S vale 0. Correcto


### Fecha

09/10/2026


