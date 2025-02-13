## **1. Componentes Principales de la Arquitectura Hack**

La arquitectura Hack es una representación simplificada y didáctica del funcionamiento de una computadora. Su propósito principal es proporcionar un entendimiento claro de cómo interactúan los componentes básicos en una máquina computacional. A continuación, se detallan los elementos más relevantes de esta arquitectura.

---

## **2. CPU: Partes Principales**

La **Unidad Central de Procesamiento (CPU)** de Hack es la encargada de ejecutar las instrucciones del programa. Su estructura incluye los siguientes componentes clave:

- **ALU (Unidad Aritmético-Lógica):**  
  La ALU es responsable de realizar operaciones aritméticas (como suma y resta) y lógicas (como AND, OR y desplazamientos de bits). Su papel es fundamental, ya que ejecuta las operaciones sobre los datos almacenados en los registros.

- **Registros A y D:**
  - **Registro A:**  
    El registro A tiene la función de almacenar direcciones de memoria o valores inmediatos que son utilizados en las instrucciones de la CPU. Es un registro de dirección, permitiendo que el sistema localice datos en la memoria RAM o ROM.
  - **Registro D:**  
    El registro D es usado para almacenar datos temporales o los resultados de operaciones realizadas por la ALU. A diferencia del registro A, que se enfoca en direcciones, el registro D se utiliza para contener los valores manipulados directamente.

- **PC (Contador de Programa):**  
  El **PC** guarda la dirección de la siguiente instrucción a ejecutar. Su papel es esencial en el ciclo **Fetch-Decode-Execute**, pues indica a la CPU cuál será la próxima instrucción que se cargará y ejecutará. Tras ejecutar una instrucción, el PC se incrementa, a menos que se indique un salto en el flujo de ejecución.

---

## **3. Memoria: Organización en Hack**

La memoria en Hack está compuesta por dos segmentos principales: **RAM** y **ROM**. Cada uno tiene una función específica dentro del sistema:

- **RAM (Memoria de Acceso Aleatorio):**  
  La **RAM** en Hack tiene 32,768 direcciones, numeradas del 0 al 32,767. Esta memoria es volátil, es decir, su contenido se pierde cuando el sistema se apaga. Se utiliza para almacenar datos dinámicos como resultados intermedios, variables y valores temporales.

- **ROM (Memoria de Solo Lectura):**  
  La **ROM**, también con 32,768 direcciones (de 0 a 32,767), almacena el código del programa a ejecutar. A diferencia de la RAM, la ROM es de solo lectura y contiene las instrucciones que la CPU sigue para ejecutar el programa.

**Mapa de Memoria:**  
El mapa de memoria en Hack está dividido en dos segmentos:
- **RAM:** Direcciones de 0 a 31,767.
- **ROM:** Direcciones de 32,768 a 65,535.

---

## **4. Registros A y D: Función y Diferencias**

Ambos registros, A y D, son cruciales para el funcionamiento de la CPU, aunque desempeñan funciones diferenciadas:

- **Registro A:**  
  Se utiliza principalmente para almacenar direcciones de memoria o valores inmediatos. Este registro permite a la CPU acceder a la memoria de manera eficiente y es esencial para la lectura y escritura de datos.

- **Registro D:**  
  El registro D se utiliza para almacenar datos temporales y resultados de operaciones aritméticas o lógicas. Es importante en el procesamiento intermedio de datos dentro de la CPU.

**Diferencia entre A y D:**  
La principal diferencia es que el **registro A** maneja direcciones de memoria, mientras que el **registro D** está orientado al almacenamiento de datos y resultados intermedios de operaciones.

---

## **5. Contador de Programa (PC): Función en el Ciclo Fetch-Decode-Execute**

El **PC** es un componente esencial en el ciclo de ejecución de instrucciones de la CPU. Su rol es proporcionar la dirección de la siguiente instrucción a ejecutar. Este ciclo se desglosa de la siguiente manera:

- **Ciclo Fetch:**  
  Durante este ciclo, el **PC** apunta a la dirección de la próxima instrucción en memoria, que luego es cargada por la CPU.

- **Ciclo Decode:**  
  La instrucción cargada es decodificada por la CPU para determinar qué operación se debe realizar.

- **Ciclo Execute:**  
  La CPU ejecuta la operación determinada, que puede involucrar la ALU, los registros o el acceso a memoria.

---

## **6. Diagrama de la Arquitectura Hack**

Para facilitar la comprensión de la interacción entre los diferentes componentes, se recomienda crear un diagrama en herramientas como **draw.io**. Este diagrama debe incluir:

- **CPU:**  
  Mostrar los componentes como la **ALU**, los **Registros A y D**, y el **PC**. 
  - El flujo de datos entre los registros y la ALU debe estar claramente representado.
  - El **PC** debe indicar su relación con el ciclo **Fetch-Decode-Execute**.

- **Memoria:**  
  La memoria debe estar dividida en **RAM** y **ROM**, y mostrar cómo la CPU accede a ambas.

- **Ciclo Fetch-Decode-Execute:**  
  Representar cómo la instrucción es recuperada, decodificada y ejecutada, con especial énfasis en cómo el **PC** incrementa la dirección tras cada operación.

---

Este análisis proporciona una descripción estructurada de los componentes principales de la arquitectura Hack, facilitando su comprensión para la programación y optimización de sistemas computacionales en un contexto educativo.
