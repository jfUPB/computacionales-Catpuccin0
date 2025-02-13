#### Actividad 1: Análisis de ciclo Fetch-Decode-Execute y modificación del programa en lenguaje ensamblador

### **Descripción del ejercicio**

En esta actividad se exploró el ciclo de ejecución Fetch-Decode-Execute de un programa ensamblador en el computador Hack, un entorno de simulación diseñado para fines educativos. El objetivo fue entender cómo la CPU ejecuta las instrucciones de un programa y cómo se pueden modificar dichas instrucciones para realizar operaciones aritméticas y controlar el flujo de ejecución.

### **Código Original:**
```assembly
@1 
D=A 
@2 
D=D+A 
@16 
M=D 
@6 
0;JMP
```

#### **Explicación del Código Original:**

1. **`@1`**: Carga la constante 1 en el registro de dirección A.
2. **`D=A`**: Copia el valor del registro A (1) en el registro D.
3. **`@2`**: Carga la constante 2 en el registro de dirección A.
4. **`D=D+A`**: Realiza la suma entre los valores de los registros D y A. En este caso, D = 1 y A = 2, por lo que el resultado de la suma será 3.
5. **`@16`**: Carga la dirección 16 en el registro A.
6. **`M=D`**: Almacena el valor de D (3) en la posición de memoria 16.
7. **`@6`**: Carga la dirección 6 en el registro A.
8. **`0;JMP`**: Realiza un salto incondicional a la dirección 6, lo que provoca que el programa se repita de forma indefinida.

#### **Funcionamiento del programa original:**
El programa suma los valores almacenados en las direcciones de memoria 1 y 2, y guarda el resultado en la dirección 16. Después, realiza un salto a la dirección 6, lo que genera un bucle infinito.

---

### **Modificación del programa:**

#### **Objetivo de la modificación:**
El objetivo es modificar el programa para que realice una suma entre los valores 60 y 9, almacene el resultado en la posición de memoria 6 y luego reinicie la ejecución del programa desde la posición 0.

#### **Código modificado:**
```assembly
@60       // Carga el valor 60 en el registro A
D=A       // Copia el valor de A (60) en D
@9        // Carga el valor 9 en el registro A
D=D+A     // Suma el valor de D (60) con A (9), ahora D = 69
@6        // Carga la dirección 6 en el registro A
M=D       // Almacena el valor de D (69) en la posición 6 de la memoria
@0        // Carga la dirección 0 en el registro A
0;JMP     // Saltar incondicionalmente a la dirección 0 (reiniciar el programa)
```

#### **Explicación de la modificación:**

1. **Carga de valores 60 y 9:**
   - La primera modificación consiste en reemplazar las direcciones `@1` y `@2` con las constantes `@60` y `@9` respectivamente, ya que los valores a sumar son ahora 60 y 9.
   
2. **Operación aritmética:**
   - Se mantiene la instrucción `D=D+A`, pero ahora suma 60 (almacenado en el registro D) con 9 (almacenado en el registro A). El resultado de la suma es 69.

3. **Almacenamiento en la memoria:**
   - El resultado de la suma (69) se almacena en la dirección de memoria 6 (`@6` y `M=D`).

4. **Reinicio del programa:**
   - Finalmente, para que el programa se repita de forma indefinida, se utiliza `@0` para cargar la dirección 0 en el registro A y luego un salto incondicional `0;JMP` a dicha dirección. Esto provoca que el programa reinicie su ejecución desde la posición 0.

#### **Impacto de los cambios:**
El programa modificado realiza correctamente la suma de los valores 60 y 9, almacena el resultado en la posición de memoria 6 y, después de almacenar el valor, reinicia el ciclo de ejecución del programa desde la posición 0. Esto genera un ciclo infinito en el cual la CPU ejecuta las instrucciones de forma continua, sumando siempre los valores 60 y 9 y almacenando el resultado de forma constante en la dirección 6.

---

**Notas Adicionales:**

1. **Ciclo Fetch-Decode-Execute:** Este ciclo es el fundamento de la ejecución de cualquier programa en una computadora. La CPU obtiene las instrucciones de memoria (Fetch), las interpreta (Decode) y luego las ejecuta (Execute).
   
2. **Lenguaje Ensamblador y el computador Hack:** Hack es un computador didáctico cuyo lenguaje ensamblador se utiliza para enseñar los fundamentos de la arquitectura de computadoras. Es un sistema simplificado pero efectivo para entender la lógica subyacente en la ejecución de programas.

3. **Ciclo infinito:** El salto a la posición 0 genera un ciclo infinito, lo cual es una forma común de reiniciar un programa o mantenerlo en ejecución hasta que se detenga manualmente.

---
