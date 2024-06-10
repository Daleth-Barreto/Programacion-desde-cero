# Operador Ternario

El operador ternario es una alternativa más corta para las declaraciones if-else. Se utiliza para evaluar una expresión y devolver un valor basado en esa evaluación. La sintaxis del operador ternario es la siguiente:

``` cpp

condicion ? expresion_si_verdadero : expresion_si_falso;
```
Aquí:

- condicion es la expresión que se evalúa. Si es verdadera (true), se ejecuta expresion_si_verdadero.
- Si condicion es falsa (false), se ejecuta expresion_si_falso.

Ejemplo Básico

Veamos un ejemplo simple para entender cómo funciona:

```cpp

#include <bits/stdc++.h>
using namespace std;

int main() {
    int a = 5;
    int b = 10;
    
    // Usando el operador ternario para encontrar el mayor número
    int mayor = (a > b) ? a : b;

    cout << "El mayor número es: " << mayor << endl;

    return 0;
}
```
En este ejemplo:

* (a > b): Esta es la condición que se evalúa. Aquí, a es 5 y b es 10, por lo que la condición es falsa.
* a: Esta es la expresión que se ejecuta si la condición es verdadera.
* b: Esta es la expresión que se ejecuta si la condición es falsa.

Dado que a no es mayor que b, la condición es falsa y mayor se asigna a b, que es 10.
Uso del Operador Ternario

El operador ternario se puede usar para cualquier expresión simple donde se necesite una comparación y asignación rápida. Sin embargo, es mejor no abusar de él en situaciones complejas, ya que puede hacer que el código sea difícil de leer.
Ejemplos Adicionales

* Determinación de Par o Impar:

```cpp

#include <bits/stdc++.h>
using namespace std;

int main() {
    int numero;
    cout << "Introduce un número: ";
    cin >> numero;

    string resultado = (numero % 2 == 0) ? "par" : "impar";

    cout << "El número es " << resultado << "." << endl;

    return 0;
}
```
En este ejemplo, (numero % 2 == 0) es la condición. Si es verdadera, la variable resultado se asigna a "par". Si es falsa, se asigna a "impar".

* Evaluación de Edad:

```cpp

#include <bits/stdc++.h>
using namespace std;

int main() {
    int edad;
    cout << "Introduce tu edad: ";
    cin >> edad;

    string categoria = (edad >= 18) ? "Adulto" : "Menor de edad";

    cout << "Eres un " << categoria << "." << endl;

    return 0;
}
```
En este caso, (edad >= 18) es la condición. Si es verdadera, la variable categoria se asigna a "Adulto". Si es falsa, se asigna a "Menor de edad".
## Ejercicios

Ahora, vamos a practicar con algunos ejercicios:
### Ejercicio 1: Determinar el Mayor de Tres Números

```cpp

#include <bits/stdc++.h>
using namespace std;

int main() {
    int x, y, z;
    cout << "Introduce tres números: ";
    cin >> x >> y >> z;

    int mayor = (x > y) ? ((x > z) ? x : z) : ((y > z) ? y : z);

    cout << "El mayor de los tres números es: " << mayor << endl;

    return 0;
}
```
En este ejercicio, estamos utilizando el operador ternario dos veces. Primero comparamos x con y. Si x es mayor, entonces comparamos x con z. Si x es mayor que ambos, mayor se asigna a x, de lo contrario a z. Si y es mayor que x, entonces comparamos y con z. Si y es mayor que ambos, mayor se asigna a y, de lo contrario a z.
### Ejercicio 2: Clasificación de Calificaciones

```cpp

#include <bits/stdc++.h>
using namespace std;

int main() {
    int calificacion;
    cout << "Introduce tu calificación: ";
    cin >> calificacion;

    string resultado = (calificacion >= 90) ? "A" :
                       (calificacion >= 80) ? "B" :
                       (calificacion >= 70) ? "C" :
                       (calificacion >= 60) ? "D" : "F";

    cout << "Tu calificación es: " << resultado << endl;

    return 0;
}
```
En este ejercicio, evaluamos la calificación y asignamos una letra basada en el rango en el que cae. Usamos el operador ternario en cascada para manejar múltiples condiciones.