#### **1. Componentes Principales de la Arquitectura Hack**

La arquitectura Hack, aunque simplificada, está diseñada con el objetivo de comprender los fundamentos de cómo interactúan los componentes básicos de un sistema computacional. A continuación se describen los componentes más importantes de esta arquitectura.

---

#### **2. CPU: Partes Principales**

La **CPU (Unidad Central de Procesamiento)** de Hack es responsable de ejecutar las instrucciones del programa, y consta de varios elementos clave que facilitan su funcionamiento:

- **ALU (Unidad Aritmético-Lógica):**  
  La ALU es la encargada de realizar las operaciones fundamentales de procesamiento. Esta unidad realiza operaciones aritméticas como suma y resta, y operaciones lógicas como AND, OR y desplazamientos de bits. La ALU es el núcleo de las operaciones de datos en el computador.

- **Registros A y D:**  
  - **Registro A:** Este registro almacena direcciones de memoria o valores inmediatos. En otras palabras, el registro A es un registro de dirección que se utiliza para señalar dónde se encuentran los datos en la memoria RAM o ROM, o para almacenar un valor que será utilizado en una operación. El contenido del registro A puede ser utilizado directamente en la ALU.
  - **Registro D:** Este registro almacena valores temporales, resultados de operaciones o el contenido de una dirección de memoria. El registro D se utiliza principalmente para almacenar los resultados intermedios de las operaciones aritméticas o lógicas realizadas por la ALU.

- **PC (Contador de Programa):**  
  El **PC** es el componente que mantiene la dirección de la próxima instrucción que debe ser ejecutada. Durante el ciclo **Fetch-Decode-Execute**, el PC apunta a la dirección de memoria donde se encuentra la siguiente instrucción, la cual es recuperada y ejecutada por la CPU. Al finalizar cada instrucción, el PC se incrementa automáticamente para apuntar a la siguiente instrucción en memoria, excepto cuando se realiza un salto condicional o incondicional.

---

#### **3. Memoria: Organización en Hack**

La memoria en la arquitectura Hack se organiza en dos segmentos clave: **RAM** y **ROM**. A continuación se describen sus características y la importancia de su organización:

- **RAM (Memoria de Acceso Aleatorio):**  
  La **RAM** es donde se almacenan los datos dinámicos de la ejecución del programa, como las variables y los resultados intermedios. En Hack, la RAM está organizada en 32,768 direcciones, numeradas del 0 al 32,767. Esta memoria es accesible tanto para leer como para escribir, y es volátil, es decir, pierde su contenido cuando el sistema se apaga.

- **ROM (Memoria de Solo Lectura):**  
  La **ROM** es una memoria de solo lectura que contiene el código del programa a ejecutar. A diferencia de la RAM, la ROM no puede modificarse durante la ejecución, solo puede ser leída. En la arquitectura Hack, la ROM también consta de 32,768 direcciones (del 0 al 32,767). Es en este segmento donde residen las instrucciones de la máquina que la CPU debe ejecutar.

**Mapa de Memoria:**  
En Hack, las direcciones de memoria se dividen de la siguiente manera:
- **Direcciones 0 a 31,767:** Corresponden a la **RAM**.
- **Direcciones 32,768 a 65,535:** Corresponden a la **ROM**.

Este mapa de memoria es fundamental para entender cómo se organiza la información y cómo la CPU accede a los datos y las instrucciones durante su ejecución.

---

#### **4. Registros A y D: Función y Diferencias**

Los registros **A** y **D** juegan roles complementarios dentro de la CPU de Hack, pero tienen funciones distintas:

- **Registro A:**  
  El registro A se utiliza principalmente para almacenar direcciones de memoria o valores inmediatos. Este registro sirve de referencia para indicar la ubicación en la memoria desde donde se deben leer o escribir los datos. Es crucial para las instrucciones de acceso a memoria (tanto de lectura como de escritura) y para las operaciones de salto (donde se modifican las direcciones de ejecución).

- **Registro D:**  
  El registro D se utiliza para almacenar los resultados de operaciones intermedias o temporales. Por ejemplo, si la ALU realiza una operación entre dos valores, el resultado de esta operación será almacenado en el registro D. A diferencia del registro A, que se utiliza para direcciones de memoria, el registro D es usado para contener datos directamente manipulados por la CPU.

**Diferencia:**  
La diferencia principal entre los registros A y D radica en su función: el **A** está orientado a la manipulación de direcciones, mientras que el **D** maneja datos temporales y resultados de operaciones.

---

#### **5. Contador de Programa (PC): Función en el Ciclo Fetch-Decode-Execute**

El **Contador de Programa (PC)** tiene un papel central en el ciclo de ejecución de la CPU, también conocido como **Fetch-Decode-Execute**. Su función principal es mantener la dirección de la siguiente instrucción que debe ser ejecutada por la CPU.

- **Ciclo Fetch:** En este ciclo, el **PC** apunta a la dirección de memoria donde se encuentra la siguiente instrucción. Esta instrucción es "recuperada" por la CPU.
  
- **Ciclo Decode:** Luego, la instrucción recuperada es decodificada por la CPU para determinar qué operación debe realizarse.

- **Ciclo Execute:** En este ciclo, la CPU ejecuta la operación correspondiente, que puede involucrar la ALU, los registros A y D, o el acceso a la memoria.

El PC se incrementa automáticamente después de cada instrucción, a menos que una instrucción de salto o modificación de flujo de control (como un **JMP**) cambie su valor. Esto permite que el proceso de ejecución siga un flujo secuencial de manera eficiente.

---

#### **6. Diagrama de la Arquitectura Hack**

Para ilustrar la interacción entre estos componentes, a continuación se proporciona una guía para crear un diagrama de la arquitectura Hack en herramientas como **draw.io**:

- **CPU:**
  - Incluye la **ALU**, los **Registros A y D**, y el **PC**.
  - Muestra cómo los registros A y D interactúan con la ALU para realizar operaciones, y cómo el PC gestiona la dirección de la próxima instrucción.

- **Memoria:**
  - Divide la memoria en **RAM** y **ROM**, y conecta la CPU a ambas para mostrar cómo la CPU accede a los datos y las instrucciones desde estas memorias.

- **Ciclo Fetch-Decode-Execute:**
  - Representa el ciclo de ejecución de instrucciones, mostrando cómo el PC se incrementa y cómo se realiza el flujo de ejecución entre los componentes.

