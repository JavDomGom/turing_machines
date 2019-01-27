# Turing Machines
Turing Machines for education
Una máquina de Turing es un dispositivo de cálculo lógico que utiliza un input en una o varias cintas que se van moviendo en función de la instrucción que tenga el estado de un autómata, para finalmente obtener un output mediante la reescritura de los datos en la misma cinta. La máquina tiene un cabezal de lectura y este lee el dato que se encuentra en la posición de la cinta. Por buscar una similitud lo mas parecido sería un casette de música, que se rebobina o se adelanta según la canción que nos interese, en la cual podremos borrar o grabar otra canción donde queramos. En el caso de una máquina de Turing de una cinta se define dicha máquina como una 7-tupla de la siguiente manera:

M=(Q,Σ,Γ,s,_,F,δ)

Cada función de transición se escribe así:

δ(q0,0)=(X,R,q1)

Y se interpreta de la siguiente manera:

1. La máquina se encuentra en el estado q0
2. Lee un 0
3. Sobreescribe el 0 con una X
4. El cabezal se mueve en la cinta una posición a la derecha (Right)
5. Finalmente se cambia al estado q1

Teniendo claros los conceptos mínimos de los que se compone una máquina de Turing se puede diseñar una para saber si una cadena de entrada cumple una expresión lógico-matemática determinada. A continuación algunos ejemplos.

## Cadenas con un numero de 'x' seguidas del mismo número de 'y'
La notación de este Lenguaje Independiente del Contexto (LIC) o expresión regular es:

x^ny^n|n⩾0

Esta notación representa cualquier cadena compuesta de un número de caracteres x seguido del mismo número de caracteres y, y que el número de veces que aparecen estos caracteres sea mayor o igual que 0. Cualquiera de las siguientes cadenas de entrada sería válida:

(cadena vacia) \
xy \
xxyy \
xxxyyy \
xxxxyyyy \
⋮

Y las siguientes serían cadenas no válidas o no aceptadas:

x \
yx \
xyxy \
xxxyy \
xyyx \
⋮

Donde x e y pueden ser otros símbolos. Para este ejemplo se van a usar los símbolos pertenecientes al conjunto binario, o sea 0 y 1, y n valdrá 3. Así pues, estos son los datos que conforman la máquina de Turing:

Γ→{0,1} \
Σ→000111 \
Q→{q0,q1,q2,q3} \
s→q0 \
F→q3

Las funciones de transición serán las siguientes:

δ(q0,0)=(X,R,q1) \
δ(q0,Y)=(Y,R,q3) \
δ(q0,_)=(_,STOP,q4) \
δ(q1,0)=(0,R,q1) \
δ(q1,1)=(Y,L,q2) \
δ(q1,Y)=(Y,R,q1) \
δ(q2,0)=(0,L,q2) \
δ(q2,1)=(1,L,q2) \
δ(q2,X)=(X,R,q0) \
δ(q2,Y)=(Y,L,q2) \
δ(q3,Y)=(Y,R,q3) \
δ(q3,_)=(_,STOP,q4)
