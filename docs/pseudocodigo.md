# 4. Pseudocódigo: Hablando como un programador

## 4.1. ¿Qué es el Pseudocódigo?
El **pseudocódigo** es un **lenguaje de programación falso** (de ahí el prefijo *pseudo*). No es código real que el ordenador pueda ejecutar, sino una forma de escribir los pasos del algoritmo utilizando nuestro propio idioma (español) pero siguiendo una estructura rígida.

**¿Para qué sirve?**

* Permite centrarse en la lógica sin preocuparse de si falta un punto o una coma.
* Es mucho más rápido de escribir que dibujar un diagrama de flujo.
* Facilita la traducción final a cualquier lenguaje como Python o Java.

---

## 4.2. Las Variables: El almacén de datos
Como vimos anteriormente, una computadora necesita guardar información para trabajar con ella. Para ello utiliza **Variables**.

Imagina una variable como una **caja con una etiqueta**.

* La **etiqueta** es el nombre de la variable (ej. `precio`, `edad`, `usuario`).
* El **contenido** es el valor que guardamos dentro (ej. `10.5`, `15`, `"Juan"`).

### 4.2.1. Declaración de Variables
La forma de declarar una variable en pseudocódigo es la siguiente:

```pseudocode
DEFINIR nombre_variable COMO TipoDeDato
```

Ejemplo:
```text
DEFINIR edad COMO Entero
DEFINIR nombre COMO Cadena
DEFINIR precio COMO Real
```
### 4.2.2. Asignación de Valores
Una vez declarada la variable, podemos asignarle un valor usando el operador `=`. En algunos, la asignación se hace con el operador `<-`, pero en este curso usaremos el `=` para simplificar.:

```pseudocode
nombre_variable = valor
```
Ejemplo:
```text
edad = 14
nombre = "Carlos"
precio = 9.99
``` 


### Reglas para nombrar variables:
1.  Deben ser nombres descriptivos (mejor `base` que simplemente `b`).
2.  No pueden tener espacios (se usa `puntos_jugador` o `puntosJugador`).
3.  No pueden empezar por números.

---

## 4.3. Tipos de Datos
No todas las cajas son iguales. En programación, debemos decirle al ordenador qué tipo de información vamos a guardar:

* **Enteros (Integer):** Números sin decimales (ej. `edad = 14`).  
* **Reales/Flotantes (Float):** Números con decimales (ej. `nota = 8.5`).  
* **Cadenas (String):** Texto entre comillas (ej. `nombre = "Carlos"`).  
* **Booleanos:** Valores que solo pueden ser **Verdadero** o **Falso** (ej. `esta_lloviendo = Verdadero`).  

---

## 4.4. Operadores: Trabajando con los datos
Para que el algoritmo haga algo útil, necesitamos operar con las variables:

* **Aritméticos:** `+`, `-`, `*`, `/` (suma, resta, multiplicación, división).
* **De comparación:** `>`, `<`, `==` (igual a), `!=` (distinto de). Se usan mucho en los rombos de decisión
* **De asignación:** `=` (se usa para meter un valor en la caja: `puntos = 10`).

---

## 4.5. Ejemplo Completo: Del diagrama al pseudocódigo
Vamos a traducir el ejemplo de tus archivos sobre **sumar dos números** a pseudocódigo técnico:

> Importante: Las líneas que llevan `//` es un comentario, es decir, una explicación que no se ejecuta. En algunos lenguajes de programación real se usan `//` para los comentarios de una sola línea, pero en pseudocódigo no hay una regla fija. Aquí lo usamos solo para aclarar cada paso.

**Algoritmo: SumarDosNumeros**
```text
INICIO
    // Definición de variables
    DEFINIR num1, num2, resultado COMO Entero
    
    // Entrada de datos
    ESCRIBIR "Por favor, introduce el primer número:"
    LEER num1
    ESCRIBIR "Introduce el segundo número:"
    LEER num2
    
    // Proceso
    resultado = num1 + num2
    
    // Salida
    ESCRIBIR "La suma de los dos números es: "
    ESCRIBIR resultado
FIN
```

---

## 4.6. Estructuras Condicionales en Pseudocódigo
Cuando en el diagrama de flujo usamos un rombo, en pseudocódigo usamos la estructura **SI... ENTONCES... SINO**:

```text
SI (condición) ENTONCES
    Instrucciones si es verdad
SINO
    Instrucciones si es falso
FIN SI
```

**Ejemplo (Cálculo de la mitad de un número positivo):**
```text
ESCRIBIR "Introduce un número:"
LEER x
SI x > 0 ENTONCES
    resultado = x / 2
    ESCRIBIR resultado
SINO
    ESCRIBIR "Error: El número debe ser positivo"
FIN SI
```