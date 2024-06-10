# Variables
Las variables son un concepto fundamental en la programación, ya que nos permiten almacenar y manipular datos. Entender cómo funcionan es crucial para escribir programas efectivos.
## Declaración de Variables

Declarar una variable significa decirle al programa que queremos reservar un espacio en la memoria para almacenar un dato de un tipo específico. Para declarar una variable en C++, seguimos esta estructura:

```cpp

tipo_de_dato nombre_de_variable;
```
Ejemplos:
```cpp

int edad;      // Declara una variable de tipo entero llamada "edad"
float altura;  // Declara una variable de tipo flotante llamada "altura"
double peso;   // Declara una variable de tipo doble llamada "peso"
char inicial;  // Declara una variable de tipo carácter llamada "inicial"
string nombre; // Declara una variable de tipo cadena de caracteres llamada "nombre"
bool esEstudiante; // Declara una variable de tipo booleano llamada "esEstudiante"
int a, b;      // Declara dos variables del mismo tipo en una misma linea
```
## Asignación de Variables

Asignar una variable significa darle un valor inicial. Esto se hace usando el operador =:

```cpp

nombre_de_variable = valor;
```
Ejemplos:

```cpp

edad = 25;            // Asigna el valor 25 a la variable "edad"
altura = 1.75;        // Asigna el valor 1.75 a la variable "altura"
peso = 70.5;          // Asigna el valor 70.5 a la variable "peso"
inicial = 'J';        // Asigna el carácter 'J' a la variable "inicial"
nombre = "Juan";      // Asigna la cadena "Juan" a la variable "nombre"
esEstudiante = true;  // Asigna el valor true a la variable "esEstudiante"
```
## Declaración y Asignación Simultáneas

Podemos declarar y asignar una variable al mismo tiempo. Esto es muy común y hace el código más conciso:

```cpp

int edad = 25;            // Declara y asigna 25 a "edad"
float altura = 1.75;      // Declara y asigna 1.75 a "altura"
double peso = 70.5;       // Declara y asigna 70.5 a "peso"
char inicial = 'J';       // Declara y asigna 'J' a "inicial"
string nombre = "Juan";   // Declara y asigna "Juan" a "nombre"
bool esEstudiante = true; // Declara y asigna true a "esEstudiante"
int a, b=10;              // Declara dos variables del mismo tipo en una misma linea y asigna el 10 a "b"
int c=2, d=4;             // Declara y asigna 2 y 4 a "c" y "d" respectivamente

```
## Tipos de datos
 Los tipos de datos son fundamentales en la programación, ya que determinan qué tipo de valores pueden almacenarse y qué operaciones se pueden realizar con ellos.
### 1. Tipos de Datos Primitivos
#### Enteros (int, short, long, long long)

Los enteros son números sin decimales. Pueden ser positivos o negativos.

* int: Un entero estándar. Ocupa generalmente 4 bytes en la memoria.
* short: Un entero corto. Ocupa generalmente 2 bytes en la memoria.
* long: Un entero largo. Ocupa generalmente 4 bytes, pero puede variar dependiendo del sistema.
* long long: Un entero muy largo. Ocupa generalmente 8 bytes.

Ejemplo:

```cpp

#include <bits/stdc++.h>
using namespace std;

int main() {
    int numero = 42;
    short numeroCorto = 123;
    long numeroLargo = 123456789L;
    long long numeroMuyLargo = 123456789012345LL;

    cout << "int: " << numero << endl;
    cout << "short: " << numeroCorto << endl;
    cout << "long: " << numeroLargo << endl;
    cout << "long long: " << numeroMuyLargo << endl;

    return 0;
}
```
#### Flotantes (float, double, long double)

Los números flotantes son números con decimales.

* float: Números de punto flotante de precisión simple. Ocupa generalmente 4 bytes.
* double: Números de punto flotante de doble precisión. Ocupa generalmente 8 bytes.
* long double: Números de punto flotante de precisión extendida. Ocupa generalmente 12 o 16 bytes, dependiendo del sistema.

Ejemplo:

```cpp

#include <bits/stdc++.h>
using namespace std;

int main() {
    float numeroFlotante = 3.14f;
    double numeroDoble = 2.718281828;
    long double numeroLargoDoble = 1.618033988749894L;

    cout << "float: " << numeroFlotante << endl;
    cout << "double: " << numeroDoble << endl;
    cout << "long double: " << numeroLargoDoble << endl;

    return 0;
}
```

#### Caracteres (char)

Los caracteres son símbolos individuales, como letras o dígitos.

* char: Representa un solo carácter. Ocupa generalmente 1 byte.

Ejemplo:

``` cpp

#include <bits/stdc++.h>
using namespace std;

int main() {
    char letra = 'A';
    char digito = '7';

    cout << "char letra: " << letra << endl;
    cout << "char digito: " << digito << endl;

    return 0;
}
```
#### Booleanos (bool)

Los booleanos representan valores de verdad: verdadero o falso.

* bool: Representa un valor booleano. Ocupa generalmente 1 byte.

Ejemplo:

```cpp

#include <bits/stdc++.h>
using namespace std;

int main() {
    bool esVerdadero = true;
    bool esFalso = false;

    cout << "bool esVerdadero: " << esVerdadero << endl;
    cout << "bool esFalso: " << esFalso << endl;

    return 0;
}
```
**Nota:** A partir de aquí es opcional la lectura, las bases ya fueron mostradas   
### 2. Tipos de Datos Derivados
#### Arrays (Arreglos)

Un array es una colección de elementos del mismo tipo.

* Declaración de un array: tipo nombreArray[tamaño];

Ejemplo:

```cpp

#include <bits/stdc++.h>
using namespace std;

int main() {
    int numeros[5] = {1, 2, 3, 4, 5}; // Array de 5 enteros

    for (int i = 0; i < 5; i++) {
        cout << "numeros[" << i << "]: " << numeros[i] << endl;
    }

    return 0;
}
```
#### Strings (Cadenas de caracteres)

En C++, una cadena de caracteres puede ser representada por un array de char o por la clase string.

* Array de char:
```cpp

#include <bits/stdc++.h>
using namespace std;

int main() {
    char saludo[] = "Hola";

    cout << "Saludo: " << saludo << endl;

    return 0;
}
```
* Clase string:

```cpp

#include <bits/stdc++.h>
using namespace std;

int main() {
    string saludo = "Hola";

    cout << "Saludo: " << saludo << endl;

    return 0;
}
```
**Punteros**

Un puntero es una variable que almacena la dirección de memoria de otra variable.

    Declaración de un puntero: tipo *nombrePuntero;

Ejemplo:

```cpp

#include <bits/stdc++.h>
using namespace std;

int main() {
    int numero = 10;
    int *puntero = &numero; // El puntero almacena la dirección de la variable numero

    cout << "Valor de numero: " << numero << endl;
    cout << "Dirección de numero: " << &numero << endl;
    cout << "Valor del puntero: " << puntero << endl;
    cout << "Valor al que apunta el puntero: " << *puntero << endl;

    return 0;
}
```
### 3. Modificadores de Tipo

Los modificadores de tipo cambian las propiedades de los tipos de datos primitivos. Los más comunes son:

* signed: Indica que una variable puede tener valores negativos o positivos. Es el comportamiento por defecto para int.
* unsigned: Indica que una variable solo puede tener valores positivos.

Ejemplo:
```cpp

#include <bits/stdc++.h>
using namespace std;

int main() {
    unsigned int positivo = 123;
    signed int negativo = -123;

    cout << "unsigned int: " << positivo << endl;
    cout << "signed int: " << negativo << endl;

    return 0;
}
```
### 4. Tipos de Datos Definidos por el Usuario
#### Estructuras (struct)

Una estructura es una colección de variables de diferentes tipos bajo un mismo nombre.

Ejemplo:

```cpp

#include <bits/stdc++.h>
using namespace std;

struct Persona {
    string nombre;
    int edad;
    float altura;
};

int main() {
    Persona persona1;
    persona1.nombre = "Juan";
    persona1.edad = 30;
    persona1.altura = 1.75f;

    cout << "Nombre: " << persona1.nombre << endl;
    cout << "Edad: " << persona1.edad << endl;
    cout << "Altura: " << persona1.altura << endl;

    return 0;
}
```

#### Uniones (union)

Una unión es similar a una estructura, pero solo puede almacenar un valor a la vez.

Ejemplo:

```cpp

#include <bits/stdc++.h>
using namespace std;

union Numero {
    int entero;
    float flotante;
};

int main() {
    Numero numero;
    numero.entero = 10;

    cout << "Número entero: " << numero.entero << endl;

    numero.flotante = 3.14f;
    cout << "Número flotante: " << numero.flotante << endl;

    return 0;
}
```
#### Enumeraciones (enum)

Una enumeración es un conjunto de constantes enteras.

Ejemplo:

```cpp

#include <bits/stdc++.h>
using namespace std;

enum Color {Rojo, Verde, Azul};

int main() {
    Color colorFavorito = Azul;

    cout << "Color favorito: " << colorFavorito << endl;

    return 0;
}
```