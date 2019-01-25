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
